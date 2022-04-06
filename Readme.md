
# Steps to setup Prettier, ESLint and Husky 

- Install eslint and prettier plugins in VSCode
- Copy .eslintrc.json, .prettierrc and .prettierignore to the root of the repo
### Please run the following commands :
  - `npm install --save-dev prettier pretty-quick eslint husky eslint-config-airbnb eslint-config-prettier eslint-plugin-prettier eslint-plugin-react`

- `npx husky install`

- `npm set-script lint "npx eslint src --ext .js,.jsx,.ts,.tsx"`

- `npm set-script lint:fix "npx eslint src --ext .js,.jsx,.ts,.tsx --fix"`

- `npm set-script prepare "husky install"`

- `npx husky add .husky/pre-commit "npx pretty-quick --staged && npm run lint"`

## Points to Note

- Run prepare script when using the repo after cloning so as to enable the git hooks
  
        npm run prepare

- While committing, husky will automatically run prettier and eslint.If any errors are enocuntered for eslint or prettier, the commit will be aborted.
- Lookup the error messages.
- Use the lint:fix script to fix the errors. (which are common errors)

        npm run lint:fix

- If you notice any out of the ordinary eslint errors report to me (Frederic).
We will look into it and make respective fixes or rule changes.    