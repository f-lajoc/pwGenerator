# passwordGenerator
Generates, Saves and Clears Passwords based on user requirement 


## Table of contents
  - [Overview](#overview)
    - [The Features](#the-features)
    - [Video](#video)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [Thoughts and troubles](#thoughts-and-troubles)
    - [What I learned and used](#what-i-learned-and-used)
      - [Tailwind CSS Dark Mode](#tailwind-css-dark-mode)
      - [Chrome extension](#chrome-extension)
      - [SVG Icon](#svg-icon)
      - [GIT CLI](#git-cli)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)
  - [Author](#author)

## Overview

### The Features

- Dark and Light mode
- Chrome extension
- Save and Clear Generated passwords
- 10 - 15 password length option
- Number, Alphabeth and Symbol toggle 

### Video 

link will be generated by github

### Links

- Solution URL: [https://github.com/f-lajoc/passwordGenerator] 
- Live Site URL: [https://password-generat00r.netlify.app/]
- Extension: []

## My process

### Built with
- Tailwind CSS
- Javascript localStorage
- HTML input type
- manifest.json

### Thoughts and troubles
- I had issues while wriring the conditionals(No, Alp & Symb) for the password to generate, i initially used array methods like slice() but it still didn't work the expected way, i ended up figuring out i could use concat() method.
- External link does not work on manifest.json for chrome extension which gave me headache as the dark mode feature is linked to font awesome external icon. I resolved this by using the svg instead of font awesome link.
- The link to my github at the footer wont work because of manifest, but i resolved it by adding target to my footer link.
- Tried out Javascript localStorage, i wanted to choose which to use between removeItem() and clear(), i couldn't get any article that focuses on differentiating them, i think i'll write an article on it

### What I learned and used

#### Tailwind CSS Dark Mode
- In tailwind.config.js file, add **darkMode: "class"** at the base root such as 'content and theme', e.g
  ```js
  module.exports = {
	content: ["./**/*.{html,js}"],
	darkMode: "class",
	theme: {
		extend: {
			},
	},
	plugins: [],
   };
  ```

- Add whatever class-name you chose, for the dark mode toggle in your html file, e.g
  ```html
  <p class="toggle-dark" alt="toggle for light and dark mode">🌓</p>
  ```

- Use this function in script.js file, querySelector value must be the same with class-name used in html file
  ```js
  /* SELF INVOKING FUNCTION FOR LIGHT & DARK MODE*/
  (function () {
	const darkToggle = document.querySelector(".toggle-dark");

	// eventListener
	darkToggle.addEventListener("click", (event) => {
		event.preventDefault();
		document.documentElement.classList.toggle("dark");
	});
	
    })();
  ```
- Then style HTML using **dark:**, e.g Header is given margin of 8px when in light-mode and 12px when in dark-mode
  ```html
  <h1 class="m-2 dark:m-3">
  ```

#### Chrome extension
- Create manifest.json file which is used to make extension, input the following
  ```json
  {
  "manifest_version": 3,
  "version": "1.0",
  "name": "",
  "description": "",
  "action": {
    "default_popup": "index.html",
    "default_icon": {
      "16": "",
      "32": "",
      "48":  "",
      "128": "",
    }
  },
  "permissions": [
    "activeTab"
  ]
  }
  ```
- To add external link, like a social link to your extension, add **target** to open the link on a new page.
  ```html
  <a target="_blank" href="">Lajoc_devs</a>
  ```

#### SVG Icon
- Download the desired font awesome icon as svg, open it, change the **svg fill** value to your desired color
`<svg fill="#ECFDF5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M448 256c0-106-86-192-192-192V448c106 0 192-86 192-192zM0 256a256 256 0 1 1 512 0A256 256 0 1 1 0 256z"/></svg>
`

#### GIT CLI
- To remove existing linkage of local workspace and a repository
  ```
  git remote rm origin
  ```
- To bring work from repositories to local workspace
  ```
  git pull
  ```
- To put work from local workspace to repositories
  ```
  git push
  ``` 
### Continued development

- Git Version Control
- Javascript
- Technical Writing

### Useful resources
- [Tailwind dark mode](https://youtu.be/hGHk5eS5MkA?si=SpyKzBrVnTHus9oh)
- [Chrome extension](https://scrimba.com/playlist/pPD7Kt4)
- [Manifest external link](https://groups.google.com/a/chromium.org/g/chromium-apps/c/bkSOQKYMUmw?pli=1)
- [Tailwind documentation](https://v2.tailwindcss.com/docs)

## Author
- Twitter - [@lajoc__](https://www.twitter.com/lajoc__)
- Instagram - [@lajoc_devs](https://www.instagram.com/lajoc_devs)
- Codepen - [@lajoc__](https://codepen.io/lajoc__/pen/bGvYWjR)
- Github - [f-lajoc ](https://github.com/f-lajoc)
- LinkedIn - [bolaji funmilola](https://www.linkedin.com/in/funmilola-b-b4044b13b)
- Medium - [Funmi Lajoc](https://medium.com/@lajoc_)
