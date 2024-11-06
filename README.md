# Intro to Tailwindcss 
> **Note:** This is a tutorial about the basics of tailwindcss and how to use it

## Step 1: Edit `tailwind.config.js`
> **Important:** [Reference to tailwind.css documentation](https://tailwindcss.com/docs/installation)
This file by default contains the following code: 
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [],      // content: ['./build/*.html'],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

+ Important steps that need to be taken
  1. Update the `content`
     + `content: ['./build/*.html]`
     + Need to include the directory to the `index.html` file
  
## Step 2: Create and add code to `./src/input.css`
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

+ Input the `input.css` file then output `style.css` file to **css** the folder. 
`npx tailwindcss -i ./src/input.css -o ./build/css/style.css`
+ The output `style.css` will contain the tailwind style

1. `npx tailwindcss -i ./src/input.css -o ./build/css/style.css --watch`
   + watches any changes made: classes added to html etc. 
   + will then recompile the css file 
   + Open **Live Server** to see changes made

## No Styling in tailwind
> **Note:** If a certain styling doesn't exist in tailwindcss then you would need to define it in the `input.css` file

Example: 
```css
/* If not in the tailwind.css, define it here */
.radial-blue{
 background: radial-gradient(white, black);   
}
```