# Vite-Sass
![enter image description here](https://mlemwlkcej9o.i.optimole.com/cb:cSka.4f299/w:1200/h:627/q:mauto/f:best/https://martagonzalez.dev/wp-content/uploads/2023/01/proyecto-con-vite-vanillajs-y-sass-linkedin.jpg)
# Componentes para el desarrollo

## Autoprefixer
Es una buena idea incluir autoprefixer para agregar automáticamente prefijos de navegador a tus estilos. Esto ayuda a garantizar una mayor compatibilidad entre navegadores.

 **Instalacion:**
*npm install --save-dev autoprefixer*

Asegúrate de configurar tu archivo postcss.config.js para incluir autoprefixer.
**CONFIGURACION**: Crea un archivo llamado ***postcss.config.js*** en la raíz de tu proyecto y agrégale el siguiente contenido:

    module.exports = {plugins: {autoprefixer: {}  },};
    
## Prettier
Prettier es una herramienta de formateo de código que puede ayudar a mantener un estilo de código consistente en tu proyecto. Puedes configurarlo según tus preferencias y asegurarte de que tu código se vea limpio y bien formateado.

 **Instalacion:**
*npm install --save-dev prettier*

Además de instalarlo, es común crear un archivo de configuración ***.prettierrc*** para personalizar las reglas de formateo.

**EXPLICACION DE LOS COMANDOS DE PRETTIER EN .prettierrc**

| CLAVE | DEFINICION |
|--|--|
| "semi": false, | No añadir punto y coma al final de las sentencias |
| "singleQuote": true, | Utilizar comillas simples en lugar de dobles |
| "tabWidth": 2, |  Utilizar espacios en lugar de tabulaciones |
| "useTabs": false, | Tamaño de la sangría con espacios |
| "printWidth": 80, | Longitud máxima de la línea |
| "endOfLine": "auto", |  Utilizar el formato de fin de línea del sistema operativo |
| "trailingComma": "es5", |  Añadir coma al final de las listas si es posible (excepto en funciones) |
| "arrowParens": "always" |   Añadir paréntesis alrededor de los parámetros de las funciones de flecha siempre |

## Eslint:
Eslint es útil para mantener la consistencia en tu código JavaScript. Puedes configurarlo para que funcione junto con prettier para garantizar un código limpio y bien formateado.

 **Instalacion:**
*npm install --save-dev eslint*
**Inicializar eslint:**
*npx eslint --init*

Al igual que con prettier, puedes configurar tu archivo de configuración .eslintrc para adaptarlo a tus necesidades. Esto te guiará a través de un proceso de configuración interactivo. Puedes elegir reglas recomendadas o configurarlas según tus necesidades.

**REGLAS COMUNES A CONSIDERAR EN EL ARCHIVO .eslintrc.json**

**1 reglas para la indentación**:

    "indent": ["error", 2],

Esta regla especifica que la sangría (o indentación) debe ser de 2 espacios. Asegura que el código sea fácil de leer y consistente en cuanto a la sangría.

**2 reglas para punto y coma:**

    "semi": ["error", "never"],

Esta regla indica que no se deben usar punto y coma al final de las sentencias en JavaScript. Algunos desarrolladores prefieren esta convención.

**3 reglas para comillas:**

    "quotes": ["error", "single"],

Esta regla especifica que debes usar comillas simples en lugar de comillas dobles para las cadenas de texto.

**4 reglas para espaciado después de palabras clave:**

    "keyword-spacing": ["error", { "before": true, "after": true }],

Esta regla asegura que haya espacios antes y después de las palabras clave en el código, mejorando la legibilidad.

**5 reglas para espaciado dentro de bloques:**

    "block-spacing": ["error", "always"],

Esta regla asegura que siempre haya espacios dentro de bloques de código, lo que también contribuye a la legibilidad del código.

**6 reglas para la longitud máxima de línea:**

    "max-len": ["error", { "code": 80 }],

Esta regla limita la longitud de una línea de código a 80 caracteres. Ayuda a mantener líneas de código más cortas y fomenta la legibilidad.

**7 reglas para el uso de console:**

    "no-console": "warn",

Esta regla emite una advertencia (warn) si encuentras alguna declaración de console.log() en tu código. Puede ser útil para evitar olvidos de declaraciones de console en el código de producción.

**CONFIGURACION DEL .slintrc.json**

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
        // Puedes agregar más reglas según tus preferencias
      }
    }
## Stylelint:
Stylelint es una herramienta de linting para CSS. Puede ayudarte a mantener un código CSS consistente y libre de errores.

**QUE ES EL LINTING**
El linting es el proceso de analizar el código fuente de un programa para encontrar posibles errores, inconsistencias y patrones que pueden conducir a problemas en tiempo de ejecución. La herramienta que realiza este análisis se llama "linter" o "lint tool". Estas herramientas ayudan a mantener un código más consistente y a identificar posibles problemas antes de que se ejecuten.

Algunas de las tareas que un linter realiza durante el linting incluyen:

**1 Verificación de Estilo de Código:**
Un linter puede asegurarse de que el código sigue un estilo de codificación consistente. Esto incluye reglas sobre sangría, uso de comillas, punto y coma, etc.

**2 Detección de Errores Comunes:**
Los linters pueden identificar errores comunes, como variables no utilizadas, declaraciones duplicadas, o cualquier otro patrón que pueda conducir a problemas en tiempo de ejecución.

**3 Mejoras de Seguridad:**
Algunos linters también pueden advertir sobre prácticas inseguras, como el uso de funciones obsoletas o vulnerabilidades conocidas.

**4 Conformidad con Estándares:**
Los equipos de desarrollo a menudo establecen estándares de codificación. Un linter puede asegurarse de que el código cumpla con estos estándares.

**5 Optimización del Código:**
Algunos linters también pueden proporcionar sugerencias para optimizar el código, como eliminar código muerto o mejorar el rendimiento.

El linting es una práctica importante en el desarrollo de software porque ayuda a mantener un código más limpio, legible y libre de errores potenciales. Herramientas como ***ESLint para JavaScript, TSLint para TypeScript, y Stylelint para CSS*** son ejemplos comunes de linters utilizados en diferentes contextos de desarrollo.

**Instalacion:**
*npm install --save-dev stylelint stylelint-config-standard*

Asegúrate de configurar tu archivo **.stylelintrc** según tus preferencias.
   
**CONFIGURACION ARCHIVO .stylelintrc**

    {
      "extends": "stylelint-config-standard"
    }
    
Stylelint es especialmente útil cuando estás trabajando con CSS o preprocesadores como SCSS. Proporciona reglas y guías para el estilo de tu código CSS, y te ayuda a detectar errores, mantener consistencia y mejorar la legibilidad del código.

Cuando trabajas con SCSS, stylelint puede ser configurado para analizar tanto archivos CSS como archivos SCSS. Esto es beneficioso porque SCSS introduce una sintaxis más rica y compleja, y stylelint te ayuda a mantener un código consistente y libre de errores, independientemente de si estás utilizando CSS puro o un preprocesador como SCSS.

Si estás utilizando SCSS en tu proyecto Vite, te recomendaría incluir stylelint en tu configuración de desarrollo. Puedes configurarlo para que lintee tanto tus archivos CSS como tus archivos SCSS. Esto puede ayudar a evitar problemas y mejorar la calidad del código a medida que trabajas en tu proyecto.
## 5 husky y lint-staged:
Husky y lint-staged son herramientas que te permiten ejecutar scripts (como linters o formateadores de código) antes de confirmar tus cambios en Git, asegurando que tu código cumpla con ciertas reglas antes de enviarlo.

 **Instalacion:**
*npm install --save-dev husky lint-stagedt*

Configura estos en tu archivo package.json para ejecutar scripts específicos antes de cada confirmación.

## Configuración package.json y explicación:

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

Los scripts son comandos que puedes ejecutar utilizando npm o yarn. En tu caso, has definido varios scripts en la sección "scripts" de tu package.json. Algunos ejemplos son:

**- "dev": "vite" -->  es para el desarrollo local.**
Este script inicia el servidor de desarrollo de Vite. Cuando ejecutas ***npm run dev***, Vite lanzará un servidor de desarrollo que te permitirá trabajar en tu aplicación en un entorno local. Este servidor de desarrollo proporciona recarga en caliente (hot module replacement) y otras características para una experiencia de desarrollo eficiente.

**-"build": "vite build" -->  es para construir la aplicación para producción.**
Este script construye tu aplicación Vite para producción. Cuando ejecutas ***npm run build***, Vite generará una versión optimizada y lista para producción de tu aplicación. Los archivos resultantes se colocarán generalmente en un directorio como dist o build, listos para ser desplegados en un servidor web.

**-"preview": "vite preview" --> es para ver cómo se verá la aplicación construida en un entorno de producción local antes de desplegarla, es decir antes de npm run build.**
Este script inicia un servidor de vista previa de producción para la aplicación construida. Es útil para revisar cómo se verá y se comportará tu aplicación en un entorno de producción local antes de implementarla en un servidor real. Puedes ejecutar ***npm run preview*** después de ejecutar ***npm run build***.

**-"lint":** Ejecuta ESLint para realizar linting y corrección automática.

**-"format":** Utiliza Prettier para formatear el código.

**-"stylelint":** Ejecuta Stylelint para realizar linting y corrección automática en archivos CSS y SCSS.

**-"precommit":** Un script que ejecuta lint-staged. Se usará como gancho previo a la confirmación (pre-commit).

**2 Husky:**

Husky es una herramienta que te permite configurar ganchos de Git para ejecutar scripts en eventos específicos, como antes de confirmar (pre-commit). En tu caso, has configurado Husky para ejecutar ***npm run precommit*** antes de cada confirmación. Esto asegura que lint-staged se ejecute antes de cada commit.

**3 Lint-staged:**

Lint-staged es una herramienta que te permite ejecutar scripts solo en los archivos que han sido modificados en el área de preparación de Git (staging area). En tu configuración de lint-staged, estan definidos dos conjuntos de acciones:
    

 - `*".{js,jsx,ts,tsx}": Para archivos JavaScript y TypeScript, ejecuta los scripts lint y format.`
 - 
       *".{css,scss}": Para archivos CSS y SCSS, ejecuta el script stylelint.

Estos scripts se ejecutan solo en los archivos que están a punto de ser confirmados, lo que permite realizar acciones específicas en esos archivos antes de que se guarden en el repositorio.
En resumen, esta configuración asegura que antes de cada confirmación, los archivos modificados pasen por un proceso de linting y formateo específico para cada tipo de archivo, lo que garantiza la consistencia y calidad del código en tu repositorio.
## Gitignore:
  
El archivo `.gitignore` se utiliza en un repositorio de Git para especificar archivos y carpetas que deben ser ignorados por Git. Esto significa que estos archivos y carpetas no serán rastreados ni incluidos en el control de versiones del repositorio. Algunos de los patrones comunes que se encuentran en un archivo `.gitignore`, como los que has mostrado, son:


## RESUMEN DE ESTA CONFIGURACION:
Una configuración sólida y bien equilibrada para el desarrollo de páginas web, especialmente si estás utilizando Vite como tu entorno de desarrollo. Aquí hay algunas razones por las cuales esta configuración es buena:

**1 Linting y Formateo:**
Tienes ESLint para el linting de JavaScript/TypeScript, Prettier para el formateo automático del código y Stylelint para el linting de CSS/SCSS. Esto garantiza consistencia y calidad en el código.

**2 Ganchos de Git con Husky y lint-staged:**
La configuración de Husky y lint-staged garantiza que las verificaciones de linting y formateo se ejecuten automáticamente antes de cada confirmación, lo que ayuda a mantener un historial de confirmaciones limpio y consistente.

**3 Entorno de Desarrollo con Vite:**
Vite es una herramienta de desarrollo rápida y eficiente para proyectos web. Los scripts dev, build, y preview están configurados para trabajar con Vite, lo que facilita el desarrollo y la implementación de tu aplicación.

**4 Gestión de Dependencias de Desarrollo:**
Las dependencias de desarrollo incluyen herramientas como Autoprefixer, Sass, ESLint, Prettier, Stylelint, y Vite. Estas herramientas son fundamentales para el desarrollo moderno de páginas web y proporcionan un conjunto sólido de herramientas para el desarrollo, el linting y el formateo.

En resumen, La configuración es completa y proporciona un entorno de desarrollo sólido. Si esta configuración satisface tus necesidades y preferencias de desarrollo, es una excelente elección para trabajar en proyectos web. Además, es fácilmente ampliable si en el futuro decides agregar o ajustar herramientas según tus requerimientos específicos.
