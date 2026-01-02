# NFT Preview Card Component

My solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). A clean, responsive NFT card with subtle hover interactions — great practice for mobile-first design, CSS custom properties, and interactive overlay effects!

## Live Demo

[View Live Site](https://marc-techdev.github.io/nft-preview-card-component-main/)

## Built With

- Semantic HTML5 markup
- CSS custom properties (variables) for colors and typography
- Flexbox for layout alignment
- Mobile-first responsive workflow
- Outfit font from Google Fonts
- Pure CSS hover effects (no JavaScript)

## Key Features

- Fully centered card on a dark background with subtle shadow
- Responsive main image with rounded corners
- Interactive hover state on the main image: semi-transparent cyan overlay with centered view icon
- Hover effects on title and creator name (color changes to cyan)
- Clean price/time row using flexbox
- Circular avatar with white border
- Pixel-perfect match to the design on mobile (layout remains identical on desktop)

## What I Learned

### Creating a Smooth Image Hover Overlay
Used an absolutely positioned overlay div that appears on hover:

```css
.card-wrapper {
  position: relative;
  overflow: hidden;
  border-radius: 1rem;
}

.overlay {
  position: absolute;
  inset: 0;
  background-color: hsla(178, 100%, 50%, 0.4);
  display: grid;
  place-items: center;
  opacity: 0;
  transition: opacity 0.35s ease;
}

.card-wrapper:hover .overlay {
  opacity: 1;
}