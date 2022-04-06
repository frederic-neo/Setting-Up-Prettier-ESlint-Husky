
# Steps to setup Prettier, ESLint and Husky 

- Install eslint and prettier plugins in VSCode.
- Go to the repo.
### Please run the following commands :
  -     curl -O https://raw.githubusercontent.com/frederic-neo/Setting-Up-Prettier-ESlint-Husky/main/.eslintrc.json -O https://raw.githubusercontent.com/frederic-neo/Setting-Up-Prettier-ESlint-Husky/main/.prettierignore -O https://raw.githubusercontent.com/frederic-neo/Setting-Up-Prettier-ESlint-Husky/main/.prettierrc
  -     npm i --save-dev prettier pretty-quick eslint husky eslint-config-airbnb eslint-config-prettier eslint-plugin-prettier eslint-plugin-react
  -     npx husky install
  -     npm set-script lint "npx eslint src --ext .js,.jsx,.ts,.tsx"
  -     npm set-script lint:fix "npx eslint src --ext .js,.jsx,.ts,.tsx --fix"
  -     npm set-script prepare "husky install"
  -     npx husky add .husky/pre-commit "npx pretty-quick --staged && npm run lint"

### To Run the commands synchronously (Alternative Method):
  -     curl -O https://raw.githubusercontent.com/frederic-neo/Setting-Up-Prettier-ESlint-Husky/main/.eslintrc.json -O https://raw.githubusercontent.com/frederic-neo/Setting-Up-Prettier-ESlint-Husky/main/.prettierignore -O https://raw.githubusercontent.com/frederic-neo/Setting-Up-Prettier-ESlint-Husky/main/.prettierrc && npm i --save-dev prettier pretty-quick eslint husky eslint-config-airbnb eslint-config-prettier eslint-plugin-prettier eslint-plugin-react && npx husky install && npm set-script lint "npx eslint src --ext .js,.jsx,.ts,.tsx" && npm set-script lint:fix "npx eslint src --ext .js,.jsx,.ts,.tsx --fix" && npm set-script prepare "husky install" && npx husky add .husky/pre-commit "npx pretty-quick --staged && npm run lint"

Voila!!🔥😁 You have just setup Prettier, ESLint and Husky. Just go ahead and try commiting 😋.

## Points to Note

- Run prepare script when using the repo after cloning so as to enable the git hooks
  
        npm run prepare

- While committing, husky will automatically run prettier and eslint.
- If any errors are enocuntered for eslint or prettier, the commit will be aborted.
- Lookup the error messages.
- Use the lint:fix script to fix the errors. (which are common errors)

        npm run lint:fix
        
- Fix rest of the errors manually.
- If you notice any out of the ordinary eslint errors report to @frederic-neo . We will look into it and make respective fixes or rule changes.    
