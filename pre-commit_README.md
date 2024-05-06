![alt text](image.png)


### Intialize eslint file
    - npm init @eslint/config

### Install packages as dev dependencies
    - husky
    - lint-staged
    - prettier
    - eslint-config-prettier

### Add .eslintignore, .prettierignore and .prettierrc.yml

### Initialize husky pre-commit script
    - npx husky-init

### Add the following to package.json at root level

        "lint-staged": {
            "*.{js, jsx,ts,tsx}": [
            "eslint --quiet --fix"
            ],
            "*.{json,js,ts,jsx,tsx,html}": [
            "prettier --write --ignore-unknown"
            ]
        },

### Update command in .husky/pre-commit
    - npx lint-staged