## 🚅 Quick start

1.  **Create the application.**

    Use [degit](https://github.com/Rich-Harris/degit) to get this template.

    ```shell
    # Clone the template
    npx degit chromaui/intro-storybook-angular-template taskbox
    ```

1.  **Install the dependencies.**

    Navigate into your new site’s directory and install the necessary dependencies.

    ```shell
    # Navigate to the directory
    cd taskbox/

    # Install the dependencies
    npm install
    ```

1.  **Open the source code and start editing!**

    Open the `taskbox` directory in your code editor of choice and building your first component!

1.  **Browse your stories!**

    Run `npm run storybook` to see your component's stories at `http://localhost:6006`.

## 🔎 What's inside?

A quick look at the top-level files and directories included with this template.

    .
    ├── .storybook
    ├── node_modules
    ├── src
    ├── .editorconfig
    ├── .gitignore
    ├── angular.json
    ├── LICENSE
    ├── package-lock.json
    ├── package.json
    ├── tsconfig.app.json
    ├── tsconfig.json
    ├── tsconfig.spec.json
    ├── tslint.json
    └── README.md

1.  **`.storybook`**: This directory contains Storybook's [configuration](https://storybook.js.org/docs/react/configure/overview) files.

2.  **`node_modules`**: This directory contains all of the modules of code that your project depends on (npm packages).

3.  **`src`**: This directory will contain all of the code related to what you will see on your application.

4.  **`.editorconfig`**: This file contains the configurations for [EditorConfig](https://editorconfig.org/).

5.  **`.gitignore`**: This file tells git which files it should not track or maintain during the development process of your project.

6.  **`angular.json`**: This file contains all the configurations required for your Angular project.

7.  **`LICENSE`**: The template is licensed under the MIT licence.

8.  **`package-lock.json`**: This is an automatically generated file based on the exact versions of your npm dependencies that were installed for your project. **(Do not change it manually).**

9.  **`package.json`**: Standard manifest file for Node.js projects, which typically includes project specific metadata (such as the project's name, the author among other information). It's based on this file that npm will know which packages are necessary to the project.

10. **`tsconfig.app.json`**: This file contains auxiliary configurations for your Angular project.

11. **`tsconfig.json`**: This file contains configurations the required configurations for TypeScript.

12. **`tsconfig.spec.json`**: This is a TypeScript configuration file aimed for application testing.

<h2>Definitions:</h2>
1. <b>Pure Component</b>: a Component that handle the props it recieve only example(pure-task-list.ts).<br/>
2. <b>Interactions</b>: a Way to simulate real actions that user will make on the UI (click, hover, etc...).<br/>
3. <b>Addons</b>: a tool that can enhance the developer experience (controls, actions, interactions testing, accessbility testing).

<br />

<h2>Storybook Path Configuration:</h2>
<p>go to <b>directory .storybook/main.ts</b> to configure the path for including <b>stories and addons</b></p>

<h2>Container Elements Example and Nesting</h2>
<p>We can not use <b>pure-inbox-screen component</b> in the storybook<br/>
because it contains <b>task-list component</b> which needs data from the (ngxs store/NgRx store) <br />
in this case we supply the store in the <b>pure-inbox-screen.stories.ts with:
<code>
<pre>
applicationConfig({
      providers: [Store, importProvidersFrom(NgxsModule.forRoot([TasksState]))],
})
</pre>
</code>
<br/>
and we need to supply the modules it use with:
<code>
<pre>
moduleMetadata({
      imports: [CommonModule, TaskModule],
})
</pre>
</code>
The Above will make the screen live and make it work like working in the real application
</br></p>
