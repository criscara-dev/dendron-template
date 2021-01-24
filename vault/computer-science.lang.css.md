---
id: 257c2c3e-624d-4ddd-86af-679e32953da5
title: CSS
desc: ''
updated: 1611517437007
created: 1611517407007
---

# CSS notes:

- Uncommon CSS

  - element:first-child
  - element:last-child
  - :hover

- To target siblings:
  - #id h4+p (any paragraph that is a direct sibling of h4 give...)

---

## Guidelines for my CSS

Define the scope of the var

```javascript
:root {
--black: #333
}

// Use the style
h1 {
color:var(--black)
}

// use the style as var in the media
@media only screen and(max-width:600px){
body {
  --black: magenta;
}
}
```

---

/_ CSS SYSTEM _/

/_ Root variables - Use variables as backbone _/

```css
:root {
  /* Always use variables for any color, typography, spacing and your entire site can be updated or configured in one fett swoop. Don't worry about creating unique components if they are att using custom properties . */
  /* Colors */
  --black: #000;
  --white: white;
  --gray: #757575;
  --red: #e50914;
  --blue: rgb(25, 103, 175);
  --transparent-layer: rgba(0, 0, 0, 0.7);
  --transparent-layer--mobile: rgba(0, 0, 0, 0.6);
  /* Define colors intentions */
  --bgColor: var(--black);
  --textColor: var(--white);
  /* Types */
  --roboto: "Roboto", sans-serif;
  /* https://type-scale.com/ */
  --size-1250rem: 1.25rem;
  --size-1625rem: 1.625rem;
  --size-175rem: 1.75rem;
  --size-180rem: 1.8rem;
  --size-10px: 10px;
  --size-12px: 12px;
  --size-18: 18px;
  --size-26: 26px;
  --smallerSize: 0.8rem;
  --smallSize: 1rem;
  --smallMediumSize: 1.2rem;
  --mediumSize: 1.5rem;
  --largeSize: 2rem;
  --mediumlargeSize: 2.5rem;
  --largerSize: 3rem;
  /* Spacing */
  /* margins stinks! - use padding and only margin-bottom if... */
  /* Characters */
  /* Elevation */
  /* Elements - Simple, obvious, hard to break, extendable */
  /* Design reference: https://www.designsystems.com/ */
}
```

## add title Icon: `<link rel="icon" href="icon_path" type="image/icon type">`
