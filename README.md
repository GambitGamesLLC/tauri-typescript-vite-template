# Tauri + Typescript + Vite application template
Clone this template to easily get started creating a new application using [Tauri](https://tauri.app/) as the build tool and uses [Typescript](https://www.typescriptlang.org/docs/) for coding and [Vite](https://vitejs.dev/) as the bundler tool.

New to front-end web development? Check out our [Web Developer Guide](https://gambitgames.gitbook.io/web-dev-guide/) for the basics on each tool.

Use this template to create your main repository for your application. 

We heavily recommend seperating most of your application code into different packages for simplicity, testing, and documentation benefits using the [ESM Package](https://nodejs.org/api/esm.html) system.

---------------------------
HOW TO CLONE
---------------------------
- Visit this package on [Github](https://github.com/GambitGamesLLC/tauri-typescript-vite-template), press the "Use This Template" button at the top right.

- Fill out the details for your new project like normal

- Open the ```package.json``` file and change the ```"name"``` to be the same as what you named your repository.

- Open your VSCode terminal and run ```pnpm install``` to install the necessary packages to your node_modules folder (this is not uploaded to your github repository)

---------------------------
HOW TO USE THIS TEMPLATE
---------------------------
- This template uses [Typescript](https://www.typescriptlang.org/docs/), a superset of the Javascript language.

- Typescript allows you to add type definitions for a better debugging and intellisense experience for anyone reading code. If your unfamiliar with Typescript, you can still write normal Javascript in a .ts (Typescript) file, but we recommend switching to Typescript completely. 

- When making builds, your typescript code will become Javascript, so don't worry about compatability.

- Your application's entry point for logic is the ```./src/main.ts``` file. Write your application logic starting from that file.

- The ```./index.html``` file at the project root is only used as the main entry point and should remain untouched for most if not all of your apps development.

---------------------------
HOW TO RENAME YOUR APPLICATION
---------------------------
- Open ```index.html``` and change the ```<title>tauri-typescript-vite-template</title>``` to your project's name

- Open ```package.json``` and change the ```"name": "tauri-typescript-vite-template",``` line to your project's name

- Open ```src-tauri/tauri.conf.json``` and change the ```productName```, ```identifier```, and ```title``` fields to your project's name

- Open ```src-tauri/Cargo.toml``` and change the ```name``` and ```default-run``` fields to your project's name. You should also consider changing the ```description``` and ```authors``` fields to your project's specific information

---------------------------
HOW TO UPDATE YOUR WEBSITE FAVICON
---------------------------
- Within the root folder, replace the ```favicon.ico``` file with your own .ico image file

---------------------------
HOW TO UPDATE YOUR APPLICATION ICONS
---------------------------
- Open ```src-tauri/icons``` folder with your windows explorer, and replace the provided image files with your own variations

---------------------------
HOW TO TEST YOUR PROJECT AS AN WEBSITE
---------------------------
- To test your project as a website, we can skip using Tauri as a build step and just use Vite to bundle our code and serve it via local server. To do this, open the VSCode terminal and run the ```pnpm run dev``` command to compile your current local files and then hold ```Ctrl + Left Click``` on the link that Vite generates to open your browser to your ```index.html``` file running within a local server.

- Any changes you make to your code will automatically compile and run in the browser link that Vite generated for you.

- Please note that hot module replacement may not function properly depending on what other dependencies your project uses. This is most common with WebGL engines like Babylonjs. Your code is still testable, but the state of your variables will refresh from scratch everytime you save a file.

---------------------------
HOW TO TEST YOUR PROJECT AS AN APPLICATION
---------------------------
- To test your project as an application, open the VSCode terminal and run the ```pnpm tauri dev``` command to compile your current local files for a development build and have the application window start automatically and begin viewing the ```index.html``` file at your project root.

- Any changes you make to your code will automatically compile and run in the development application window that Tauri and Vite generated for you.

- Please note that hot module replacement may not function properly depending on what other dependencies your project uses. This is most common with WebGL engines like Babylonjs. Your code is still testable, but the state of your variables will refresh from scratch everytime you save a file.

---------------------------
HOW TO BUILD YOUR APPLICATION
---------------------------
- To build your project for distribution as an application, open the VSCode terminal and run the ```pnpm tauri build``` command. 

- This will generate a ```dist``` folder containing a Windows executable application installer.

- By default, the path to the installer will be at ```tauri-typescript-vite-template\src-tauri\target\release\bundle/msi/tauri-typescript-vite-template_1.0.0_x64_en-US.msi```

- We do not recommend including your application's ```dist``` folder as part of your Github repo, and as such the ```dist``` folder has been added to the ```.gitignore``` file in your project's root directory.

