# Frontend Mentor - Tip calculator app solution

This is a solution to the [Tip calculator app challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/tip-calculator-app-ugJNGbJUX). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size for the preview components
- See hover and focus states for interactive elements

### Screenshot

Mobile

![](./public/design/expense-mobile.png)

Desktop

![](./public/design/expense-desktop.png)

### Links

- Live Site URL: [Tip Calculator](https://master--effulgent-daifuku-376ef4.netlify.app/)

## Built with

- Typescript
- React
- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

- To make a grid with equal columns, use the minmax to set the template columns

```css
.grid-template-columns: repeat(2, minmax(0, 1fr));
```

- To set the disabled css in html

```css
button:disabled,
button[disabled] {
  background-color: var(--cyan-disabled);
  color: #666666;
  pointer-events: none;
}
```

- I had to use the html value property to display the perecentage. An alternative to storing data in the html element was to use data-attribute.
```html
<input data-value="5">
```
```js
Number(e.currentTarget.getAttribute("data-value"))
```


- To convert numbers in decimals efficiently:
```ts
const round = (num: number | "") => {
  if (typeof num === "number") {
    return new Intl.NumberFormat("en-US", {
      minimumFractionDigits: 2,
      maximumFractionDigits: 2,
    }).format(num);
  }
};
```

## Author

- Website - [Ebuka Nwabueze](https://www.ebukanwabueze.com)
- Frontend Mentor - [@ebuka-nwabueze](https://www.frontendmentor.io/profile/ebuka-nwabueze)
- Twitter - [@ebukaGN](https://www.twitter.com/ebukaGN)
