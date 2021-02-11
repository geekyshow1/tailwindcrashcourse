# Tailwind CSS Crash Course
## Watch Tailwind CSS Crash Course https://youtu.be/mVzY256R9fs
# Using Tailwind CSS without PostCSS
<ol>
<br>
<li>Create <b>package.json</b> file with default options
  
```javascript
npm init –y
```
</li>

<li>Install Tailwind CSS
  
```javascript
npm install tailwindcss
```
</li>

<li>Install AutoPrefixer 
  
```javascript
npm install autoprefixer
```
</li>
<li>Create <b>public</b> Folder then inside <b>public</b> folder create <b>index.html.</b> public/index.html where you can write your html code.</li><br>
<li>Create <b>src</b> Folder then inside <b>src</b> folder create <b>tailwind.css</b> file (You can change file name). src/tailwind.css file is used to write tailwind directives and custom CSS. </li><br>
<li>Open <b>src/tailwind.css</b> file then write code

```css
@tailwind base;
@tailwind components;
/* Write Custom CSS */
@tailwind utilities;
```
</li><br>
<li>Create Build Script which will compile <b>src/tailwind.css</b> file to actual css file. To do this, Open <b>package.json</b> file then write code

```javascript
"scripts": {"build": "tailwindcss build ./src/tailwind.css -o ./public/tailwind.css"}
```
</li></br>
<li>Run the script
  
```javascript  
npm run build
```
This will generate a compiled <b>tailwind.css</b> file inside <b>public</b> folder. This <b>public/tailwind.css</b> file has actual tailwind css code. You should not modify this file.</li>
<li>Done</li></br>
</ol>

> Note - If we are working on a small project which doesn’t use any kind of framework then we should use “Tailwind CSS without PostCSS” process to install tailwind.

## Customize Tailwind CSS Configuration
<ol>
  <br>
<li>Create tailwind configuration file 
  
```javascript
npx tailwindcss init
```
This will generate <b>tailwind.config.js</b> file </li>

<li><b>tailwind.config.js</b> file is used to configure your own color palette, font, apply, purge etc.</li><br>
<li>Whenever you do changes in tailwind.config.js file you need to run 
  
```javascript
npm run build
```
</li><br>
</ol>

## Build for Production (Reduce File Size)

<ol>
 <br>
<li>Install NODE_ENV 
  
```javascript
npm install win-node-env
``` 
</li>

<li>Open <b>package.json</b> File then write below script
  
```javascript
"scripts": {"prod": "NODE_ENV=production npx tailwindcss build ./src/tailwind.css -o ./public/tailwind.css“},
```
</li>
<li>Include which file should be purged. Open <b>tailwind.config.js</b> file then write code
  
```javascript
purge:[‘./public/**/*.html’]
```
</li>
<li>Make your code Production Ready
  
```javascript
npm run prod
```
</li> <br>
</ol>

# Installing Tailwind CSS as a PostCSS Plugin
<ol>
<br>
<li>Create <b>package.json</b> file with default options
  
```javascript
npm init –y
```
</li>

<li>Install Tailwind CSS
  
```javascript
npm install tailwindcss
```
</li>

<li>Install AutoPrefixer 
  
```javascript
npm install autoprefixer
```
</li>
<li>Install PostCSS CLI 
  
```javascript
npm install postcss-cli
```
</li>

<li>Create Configuration files for Tailwind CSS and PostCSS 
  
```javascript
npx tailwindcss init -p
```
This will generate two files <b>tailwind.config.js</b> and <b>postcss.config.js</b>
</li>

<li>Create <b>public</b> Folder then inside <b>public</b> folder create <b>index.html.</b> public/index.html where you can write your html code.</li><br>
<li>Create <b>src</b> Folder then inside <b>src</b> folder create <b>tailwind.css</b> file (You can change file name). src/tailwind.css file is used to write tailwind directives and custom CSS. </li><br>
<li>Open <b>src/tailwind.css</b> file then write code

```css
@tailwind base;
@tailwind components;
/* Write Custom CSS */
@tailwind utilities;
```
</li><br>
<li>Create Build Script which will compile <b>src/tailwind.css</b> file to actual css file. To do this, Open <b>package.json</b> file then write code

```javascript
"scripts": {"build": "postcss ./src/tailwind.css -o ./public/tailwind.css"}
```
</li></br>
<li>Run the script
  
```javascript  
npm run build
```
This will generate a compiled <b>tailwind.css</b> file inside <b>public</b> folder. This <b>public/tailwind.css</b> file has actual tailwind css code. You should not modify this file.</li>
<li>Done</li></br>
</ol>

## Customize Tailwind CSS Configuration
<ol>
  <br>
<li><b>tailwind.config.js</b> file is used to configure your own color palette, font, apply, purge etc.</li><br>
<li>Whenever you do changes in tailwind.config.js file you need to run 
  
```javascript
npm run build
```
</li><br>
</ol>

## Build for Production (Reduce File Size)

<ol>
 <br>
<li>Install NODE_ENV 
  
```javascript
npm install win-node-env
``` 
</li>

<li>Open <b>package.json</b> File then write below script
  
```javascript
"scripts": {"prod": "NODE_ENV=production postcss ./src/tailwind.css -o ./public/tailwind.css“},
```
</li>
<li>Include which file should be purged. Open <b>tailwind.config.js</b> file then write code
  
```javascript
purge:[‘./public/**/*.html’]
```
</li>
<li>Make your code Production Ready
  
```javascript
npm run prod
```
</li> <br>
</ol>
