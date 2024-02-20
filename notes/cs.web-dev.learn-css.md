---
id: wa9eph42wnq6gen3ai82i86
title: Learn CSS
desc: ''
updated: 1708070402119
created: 1708067888379
---
## How to create variables in `css`

```css
:root {
  --heading-color-1: #FF5733; /* Change this to your desired color */
  --heading-color-2: #33FF57; /* Change this to your desired color */
  --heading-color-3: #5733FF; /* Change this to your desired color */
  
  --body-font: 'Recursive Mono Casual Static', monospace; /* Change 'Your Personal Font' to the name of your desired font */
  --heading-font: 'Recursive Mono Casual Static', monospace;
}

h1, h2, h3, h4, h5, h6 {
    font-family: var(--heading-font);
}

h1 {
  color: var(--heading-color-1);
}


```
