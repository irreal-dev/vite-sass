# Vite-Sass
![enter image description here](https://mlemwlkcej9o.i.optimole.com/cb:cSka.4f299/w:1200/h:627/q:mauto/f:best/https://martagonzalez.dev/wp-content/uploads/2023/01/proyecto-con-vite-vanillajs-y-sass-linkedin.jpg)
# Why Vite?
**[Vite](https://vitejs.dev/) is a fast and efficient development environment designed for web  and application projects.**

Vite offers **quick startup times**, meaning faster compilation and reloading. It stands out for its **speed during development**. It is **compatible with various frameworks and libraries** (React, Vue, Vanilla JS) and supports languages like *TypeScript, JavaScript,* and preprocessors like *Sass*. Vite uses **fast and selective reloading,** refreshing only the modules that have been modified, this significantly **enhances performance during development**, particularly in large projects.

 - With **minimal configuration to get started**, it makes **project setup easy.**
 - It provides an interactive development experience with **real-time updates** and immediate **browser reloading.**
 - It integrates **popular tools** like **ESLint** and **Prettier** for code linting and formatting.
 - It allows organizing the project into independent components, **facilitating scalability.**

In conclusion, Vite is a solid choice for web projects seeking a **fast, efficient, and flexible** development environment with a modern development experience and **innovative features** like selective reloading.

# Development Components

## Autoprefixer

Including [autoprefixer](https://autoprefixer.github.io/) to add browser prefixes automatically to our styles is a good idea. This helps to guarantee better compatibility across browsers.

 **Installation:**

    npm install --save-dev autoprefixer

Make sure to configure your **postcss.config.js** file to include autoprefixer.
**CONFIGURATION**: Create a file called **postcss.config.js** in the root of your project and add the folowing content:

 

      module.exports = {
      plugins: {
        autoprefixer: {},
      },
    };
    
## Prettier

[Prettier](https://prettier.io/) is a code formatting tool that can help you maintain a consistent coding style in your project. You can configure it according to your preferences to ensure your code is clean and well-formatted.

 **Installation:**

    npm install --save-dev prettier

In addition to install it, it is usal to create a configuration file called ***.prettierrc*** to customize formatting rules.


**EXPLANATION OF THE PRETTIER COMMANDS IN .prettierrc**

| KEY | DEFINITION |
|--|--|
| "semi": false, | Do not add a period and comma at the end of the sentences |
| "singleQuote": true, | Use single quotes instead of doble quotes |
| "tabWidth": 2, |  Use spaces instead of tabs |
| "useTabs": false, | Indentation size with spaces |
| "printWidth": 80, | Maximun lenght of code line |
| "endOfLine": "auto", |  Use the operating system's end-of-line format. |
| "trailingComma": "es5", |  If possible, add a comma at the end of the lists (except for functions) |
| "arrowParens": "always" |   Always add parentheses around the parameters of arrow functions |

## ESLint:
[ESLint](https://eslint.org/) is useful for maintaining consistency in your JavaScript code. You can configure it to work in conjunction with Prettier to guarantee clean and well-formatted code.

 **Installation:**

    npm install --save-dev eslint

**Inicializar eslint:**

    npx eslint --init
**INITIALIZATION QUIZ FOR PROJECT  SETUP**
This appears when you execute  `npx eslint --init`. Refer to the oficial documentation for more info.

    √ How would you like to use ESLint? · problems    
    √ What type of modules does your project use? · esm
    √ Which framework does your project use? · none
    √ Does your project use TypeScript? · No / Yes
    √ Where does your code run? · browser
    √ What format do you want your config file to be in? · JSON
   
Just like with Prettier, you can configure your configuration file **.eslintrc** to adjust to your needs. This guide takes you through an interactive configuration process. Choose the recommended rules or configure them according to your requirements.
 
**COMMONS RULES TO CONSIDER IN THE .eslintrc.json FILE**

**1 Indentation rule**:

    "indent": ["error", 2],
This rule spicifies two-space indentation. Ensure that the code is easy to read and maintains consistency regard to indentation
-   `"error"` indicates that it's a rule, and if not followed, it will result in an error.
-   `2` specifies the desired level of indentation, in this case, 2 spaces.

**2 Semicolon rule:**

    "semi": ["error", "never"],

This rule indicates that semicolons should not be used at the end of statements in JavaScript. Some developers prefer this convention. If you prefer to use them, you just have to replace `"never"` with `"always"`.


**3 Single quotes rule:**

    "quotes": ["error", "single"],
This rule specifies that you should use single quotes instead of double quotes for text strings.

**4 Spacing rule after keywords:**

    "keyword-spacing": ["error", { "before": true, "after": true }],
 
This rule ensures spacing before and after keywords in the code, improving readability.".

**5 Spacing rules within blocks:**

    "block-spacing": ["error", "always"],

This rule ensures the existence of spaces within code blocks, contributing to code readability.

**6 Maximum line length rule:**

    "max-len": ["error", { "code": 80 }],
This rule limits the maximum line code length to 80 characters. It helps maintain shorter code lines and promotes the readability.

**7 Console use rule:**

    "no-console": "warn",
This rule emits warnings if it finds any `console.log()` statements in your code. It can be useful to avoid oversights in production code with console declarations.

 - "no-console": "warn"` means that the use of `console` statements in
   your code will generate a warning instead of an error during ESLint's
   execution.
 - In ESLint, configuration levels are generally `"off"` (off), `"warn"`
   (warning), or `"error"` (error). In this case, `"warn"` indicates
   that ESLint will display a warning in the console if it detects the
   use of `console` statements, but it won't prevent the code from
   running.
   
  Make sure to configure your **.slintrc.json** according to your preferences.

** .slintrc.json CONFIGURATION**

    {
      "env": {
        "browser": true,
        "es2021": true
      },
      "extends": "eslint:recommended",
      "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module"
      },
      "rules": {
        "indent": ["error", 2],
        "semi": ["error", "never"],
        "quotes": ["error", "single"],
        "keyword-spacing": ["error", { "before": true, "after": true }],
        "block-spacing": ["error", "always"],
        "max-len": ["error", { "code": 80 }],
        "no-console": "warn"
        // You can add more rules acording to your requirements
      }
    }
## Stylelint:
[Stylelint](https://stylelint.io/) is a CSS linting tool. It can help you maintain consistent and error-free CSS code.

**WHAT IS LINTING?**

Linting is a procces to find posibles errors, weaknesses and patterns in the source code of a program that can contribute to problems appearing at runtime. The tool that performs this test is called "linter" or "lint tool". This tools helps to maintain a solid code and identify possible problems befor execution.

Some tasks that a linter perfoms during linting includes:

**1 Code style checking:**
A linter can ensure that code follows a consistent code style. This includes indentation rules, the use of quotes, semicolons, etc.

**2 Detection of common errors:**
Linters can identify common errors, such as unused variables, duplicate declarations, or any other patterns that may lead to runtime problems.

**3 Security enhancements:**
Some linters can provide advice on unsafe practices, such as the use of obsolete functions or known vulnerabilities.

**4 Consent to standards:**
Development teams frequently set up coding satandards. A linter can ensure that the code stick to these standards.

**5 Code optimization:**
Some linters can provide suggestions for code optimization, such as deleting dead code or improving eficiency
Linting is an important pactice in software development because it helps us to maintain  clean, readable adn error-free code. Tools like ***ESLint para JavaScript, TSLint para TypeScript, y Stylelint para CSS*** are common examples of linters used in diferent development context.

**Installation:**

    npm install --save-dev stylelint stylelint-config-standard

Make sure to configure your **.stylelintrc** according to your preferences.
   
**.stylelintrc FILE CONFIGURATION**

    {
      "extends": "stylelint-config-standard"
    }
Stylelint is especially useful when you work with CSS or preprocessors like SCSS. It provides rules and guidelines to stylize your CSS code, helping you detect errors, maintain consistency, and improve code readability.   

When you are working whit SCSS, stylelint can be configured to analize both CSS and SCSS files. This is useful because SCSS ntroduces a richer and more complex syntax. Stylint helps you to maintain consistency and error-free whether you are using pure CSS or preprocessors like SCSS.

If you are using SCSS in your Vite project, I recommend including stylelint in your development configuration. You can config it to lint both your CSS and SCSS files. This can help to avoid problems and improve code quality as you work on the project.  

## 5 husky & lint-staged:

Husky and lint-staged are tools that allow you to run scripts (such as linters or code formatters) before committing your changes to Git, ensuring that your code complies with certain rules before sending it.

 **Installation:**

    npm install --save-dev husky lint-stagedt

Configure these in your package.json file to run specific scripts before each commit.

##  package.json Configuration and Explanation:

    {
      "name": "vite-sass",
      "private": true,
      "version": "0.0.0",
      "author":  "irreal-dev",   
	  "license":  "MIT",
      "type": "module",
      "scripts": {
        "lint": "eslint . --fix",
        "format": "prettier --write .",
        "stylelint": "stylelint '**/*.{css,scss}' --fix",
        "precommit": "lint-staged",
        "dev": "vite",
        "build": "vite build",
        "preview": "vite preview"
      },
      
      "husky": {
        "hooks": {
          "pre-commit": "npm run precommit"
        }
      },
      "lint-staged": {
        "*.{js,jsx,ts,tsx}": [
          "npm run lint",
          "npm run format"
        ],
        "*.{css,scss}": [
          "npm run stylelint"
        ]
      },
**1 Scripts:**

The scripts are commands that you can run using npm or yarn. In my case, I have defined several scripts in the 'scripts' section of my package.json. Some examples are:"

**"dev": "vite" -->  It's for local development** 
This script starts the Vite development server. When you run `npm run dev`, Vite will launch a development server that allows you to work on your application in a local environment. This development server provides ***hot module replacement*** and other features for an efficient development experience.

**"build": "vite build" -->  It's for building the application for production**
This script builds your aplication Vite for production. When you execute `npm run buid`, Vite creates an optimized version anda production-ready bundle of your application. The resulting are generally placed in a directory called **"dist"** or **"build"**, ready to be deployed in a web server. 

**"preview": "vite preview" --> It's to see how the built application will look in a local production environment before deploying it, that is, before running** `npm run build`
This script starts a production preview server for the built application. It's useful for reviewing how your application will look and behave in a local production environment before deploying it to a real server. You can run `npm run preview` after executing  `npm run build`.

**"lint": --> Executes ESLint to perform linting and automatic correction.** `npm run lint` 

**"format": --> Use Prettier to formant code.** `npm run format`

**-"stylelint": --> Run Stylelint to perform linting and automatic correction on CSS y SCSS  files.** `npm run stylelint`

**-"precommit": --> A script that executes lint-staged. It will be used as a pre-commit hook.**  `npm run precommit`  In other words, it allows performing actions, such as running linters, before committing changes, which helps maintain code quality in the repository."

**2 Husky:**
Husky is a tool that allows you to configure Git hooks to execute scripts in specific events, such as before committing, known as pre-commit. In this case Husky is configurates to be executed by `npm run precommit` before each commit. This ensures that lint-staged is executed before each commit

**3 Lint-staged:**

Lint-staged is a tool that allows you to run scripts only on files that have been modified in the Git staging area. In your lint-staged configuration, there are two sets of actions defined.:
    

 - `*".{js,jsx,ts,tsx}": to files JavaScript y TypeScript, execute scripts lint y format.`
 - 
       *".{css,scss}": to files CSS y SCSS, execute script stylelint.
These scripts are executed only on files that are about to be commited. This allow to make specific actions to be performance in those files before they are saved in the repository.. In summary, this configuration ensures that before each commit, the modified filesgo throug a specific linting and formatting process for each type of file, ensuring consistency and quality in your repository code.


## Gitignore:
  
The `.gitignore` file is used in a Git repository to specify files and folders that should be ignored by Git. This means that these files and folders will not be tracked or included in the version control of the repository. Some common patterns found in this Vite configuration in a `.gitignore` file, include:"

    // Logs  
    logs
    *.log
    npm-debug.log*
    yarn-debug.log*
    yarn-error.log*
    pnpm-debug.log*
    lerna-debug.log*
	
	.env      
    node_modules
    dist
    dist-ssr
    *.local
    
    // Editor directories and files
    .vscode/*
    !.vscode/extensions.json
    .idea
    .DS_Store
    *.suo
    *.ntvs*
    *.njsproj
    *.sln
    *.sw?

**LOGS**

The term "logs" in the context of a `.gitignore` file generally refers to directories where log files are stored. Log files contain information about specific events that occur during the execution of a program or system. These events could include debugging messages, errors, advisories, or any relevant information for tracking problems and troubleshooting.
  
The insertion of this entry in the `.gitignore` file helps prevent these log files from being accidentally added to version control and, therefore, the Git repository. This is useful for keeping the repository cleaner and avoiding unnecessary conflicts related to changes in log files.

To sum up, log files are valuable for diagnosing issues during development operations, but they are typically ignored in version control `.gitignore` due to the *possibility of containing sensitive information*. This keeps the repository clean and avoids unnecessary conflicts when collaborating on a project.

 - **npm-debug.log*:** Este archivo de registro es generado por npm (Node Package Manager) durante la instalación de paquetes y puede contener información detallada sobre cualquier problema que ocurra
   en la instalacion.

 - **yarn-debug.log y yarn-error.log*:** Si estas utilizando Yarn que  también es un administrador de paquetes para JavaScript. Estos archivos de registro se generan durante las operaciones de instalación o ejecución, es similar al anterior.
  
 - **pnpm-debug.log*:** Similar a npm y Yarn,  pnpm es otro administrador de paquetes para JavaScript. Este archivo de registro.
 
 - **lerna-debug.log*:** Lerna es una herramienta para administrar proyectos de monorepo (*práctica de almacenar múltiples proyectos o partes de un proyecto en un solo repositorio de control de versiones. En lugar de tener un repositorio separado para cada proyecto o componente, todos ellos se gestionan dentro de un único repositorio.*) en JavaScript. Este archivo de registro se genera durante operaciones con Lerna y contiene información dedepuración.
 
 Depending on the package manager you use, you can configure this "log" configuration to your necessities.  For example, if you are using Node, you may not need to include anything related to Yarn and PnP, in the `.gitignore` file

 - **.env :** They are commonly used to store environment variables that we don't want anyone to see due to they often contain sensitivecontent such as credentials, passwords, usernames, service configurations, etc.
   
 - **node_modules:** This line specifies that the `node_modules` folder, where project dependencies are usually stored, should be excluded from version control. Developers can reinstall them in any moment.    

 - **dist y dist-ssr:** The folders named `dist` and `dist-ssr` should not be included in version control. These folders typically contain the final version of the source code and can be regenerated at any time. 

 - ***.local**:  This pattern indicates that all files with the `.local` extension should not be included in version control. Files with this extension could be *local configuration files or temporary files* generated by development tools and *should not be shared among collaborators*.
    
These patterns are part of best practices when using Git and help keep the repository clean avoiding the inclusion of locally generated files and folders or generated during the build process.

## SUMMARY OF THIS CONFIGURATION:

A solid and well-balanced configuration for web development, especially if you are using Vite as your development environment. Here are some reasons why this configuration is good.

**1 Linting & Format:**
You have ESLint for  JavaScript/TypeScript linting, Prettier for autoformatic code formatting  and Stylelint for CSS/SCSS linting. This ensures sonsistency and quality in the code.

**2 Git Hooks with Husky and lint-staged**
The Husky and lint-staged configuration ensures that linting formatting and checks are automatically run before each commit, helping maintain a clean and consistent commit history.

**3 Development Environment with Vite**
Vite is a lightweight, fast, and efficient development tool for web proyects. The dev, build and preview scripts are configured to work perfectly with Vite, making development and deployment of your application easier.

**4 Development Dependencies Management:**
The development dependencies include tools such as Autoprefixer, Sass, ESLint, Prettier, Stylelint, and Vite. These tools are essential for modern web development and provide a robust set of tools for development, linting, and formatting.

To sum up, this configuratios is comprehensive and porvides a solid development enviroment. If this configuration fullfills your necesities and development preferences, is a great choice for working on web porjects.  Also, it is easily extendable if you need to add or adjust tools in the future according to your specific requirements. 

> Written with [StackEdit](https://stackedit.io/).
