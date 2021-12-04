## To create a project
>> vue create my-project-name


## For build work path add new file vui.config.js and add this property:
module.exports = {
  publicPath: process.env.NODE_ENV === 'production' ? './' : '/',
};


## Config Prettier
Create json file .prettierrc and add this property 
{
  "trailingComma": "none",
  "semi": true,
  "arrowParens": "always",
  "singleQuote": true
}

## To great TypeScrip functionally
//On VsCode global file settings.json add this property
{
  "vetur.format.defaultFormatter.js": "prettier",
  "vetur.format.defaultFormatter.html": "prettier"
}

//On VsCode local file add this: 
//First create folder .vscode and inside create settings.json file 
{
  "vetur.experimental.templateInterpolationService": true
}


## Install Normalize
//A modern, HTML5-ready alternative to CSS resets

>> npm install normalize.css

//Import normalize on main.vue:
import 'normalize.css';


## Install AXIOS
>> npm install axios
//create folder src/utils/axios.ts and export default axios.crete

import axios from "axios";

export default axios.create({
  baseURL: "http://localhost:3333",
});

## Install Font Awesome
>> npm install --save @fortawesome/fontawesome-free
// import on main.ts or in the specific component
import '@fortawesome/fontawesome-free/css/all.css';

## To personalized vue shortcut componente template
//Create folders vetur/snippets inside folder .vsconde end a file for template
Ex.: .vscode/vetur/snippets/v-kdev.vue end inside write the template
