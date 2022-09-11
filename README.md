# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

Practice my flexbox and layout tecniques which I think are crutial for a good responsive web design.

```html
<body>
  <div class="container">
    <div class="background-container"></div>
    <div class="content-container">
      <h2>P E R F U M E</h2>
      <h1>  Gabrielle Essence Eau De Parfum
      </h1>
      <p>A floral, solar and voluptuous interpretation composed by Olivier Polge, 
        Perfumer-Creator for the House of CHANEL.</p>
      <div class="prices-container">
        <div class="actual-price">$149.99
        </div>
        <div class="original-price"><s>$169.99</s>
        </div>
      </div>
      <div id="add-to-cart">
        <i class="fa-solid fa-cart-shopping"></i>
        Add to Cart
      </div>
    </div>
  </div>
</body>
```

```css
body {
  background-color: hsl(30, 38%, 92%);
}

.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr;
  grid-template-areas: 'body1 body2';
  text-align: left;
  max-width: 60rem;
  min-height: 90vh;
  margin: 4rem auto;
  border: none;
  border-radius: 0.4em;
  overflow: hidden;
  background-color: white;
}

.background-container {
  grid-area: body1;
  background: url(images/image-product-desktop.jpg) center/cover no-repeat;
}
.content-container {
  display: flex;
  flex-direction: column;
  margin: 0 auto;
  padding: 2em 0;
  overflow: auto;
  grid-area: body2;
  height: 100%;
  width: 90%;
}


.content-container > h2 {
  font-family: 'Fraunces', serif;
  font-weight: 500;
  font-size: 1em;
  color: hsl(32, 6%, 59%);
}
.content-container > h1 {
  font-family: 'Fraunces', serif;
  font-size: 3.2em;
  margin-top: 0;
  margin-bottom: 0.2em;
}
.content-container > p {
  font-family: 'Montserrat', sans-serif;
  font-size: 1.3em;
  line-height: 1.4em;
  color: hsl(32, 6%, 59%);
  margin-bottom: 1em;
}
.prices-container {
  display: flex;
  align-items: center;
  margin-top: 1em;
  margin-bottom: 2em;
}
.prices-container > .actual-price {
  font-family: 'Fraunces', serif;
  font-size: 3em;
  color:hsl(158, 36%, 37%);
  margin-right: 0.6em;
}
.prices-container > .original-price {
  font-family: 'Montserrat', sans-serif;
  font-size: 1.1em;
  color: hsl(32, 6%, 59%);


}
#add-to-cart {
  font-family: 'Montserrat', sans-serif;
  font-weight: 700;
  font-size: 1em;
  padding: 1.4em;
  border: none;
  border-radius: 0.35em;
  text-align: center;
  color: white;
  background-color: hsl(158, 36%, 37%);
  margin-bottom: 1.5em;
}

  @media only screen and (max-width: 650px) {
    
  .container {
    grid-template-columns: 1fr;
    grid-template-rows: 0.7fr 1.3fr;
    grid-template-areas: 
      'body1'
      'body2';
  }
  .background-container {
    background: url(images/image-product-mobile.jpg) top/cover no-repeat;
  }
  }
```

