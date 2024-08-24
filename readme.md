## VSCode + Typescript + ESLint template
This template aims to have a simple but purely strict TypeScript environment, with ESLint configured to follow best practices.

### How to use
Using it is very simple, just download the template and run ``npm install`` to install the dependencies. The configured environment is agnostic despite having already installed ``@types/node``, if you are going to use it on the web you will need to configure ``tsconfig.json`` for this.

In package.json the project was configured to be of the ``module`` type and 4 scripts were created:
- ``npm run lint`` - Lint but does not format the code, it just shows errors and warnings.
- ``npm run format`` - Lint and format the code, try to fix errors and warnings if possible.
- ``npm run build`` - Will run ``format`` and then build with ``tsc`` compiler.
- ``npm start`` - Will run ``build`` and then start the project with ``node dist/index.js``.

### Recommendations
Use a node version equal to or greater than v20.12.0. Install the official ``ESLint`` extension in VSCode.

:warning: DON'T forget to copy the ``.vscode`` folder along! It's important to enable ESLint as a formatter in VSCode, so you won't always need to use ``npm run lint`` to get style or formatting errors.