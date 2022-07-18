# First Responsive Web (HTML & CSS only)

This project consist of the creation of my very first responsive web.
 

This was the first project I did during my Full Stack Development Bootcamp and technological stack used was:

- **HTML**
- **CSS**

The application has the following pages:

- **Home**: It consists of a landing page with different sections that integrates several HTML elements and CSS styling.
- **Board**: It consists of an interactive chess board that rotates 180 degrees based on your chess pieces color preference. 
- **Contact**: It consists of a contact form with different inputs and sections. It is set up to follow some rules to be able to submit it.


# Repository Structure

It only consists on the app client side.


# Front End

One of the remarkable implementations is the use of an input checkbox and its label to be able to open the hamburguer menu on the tablet and phone breakpoints using a @keyframes animation.

```html
<header>
        <section class="header__container">
            <img class="header__logo" src="./header-footer/html5css3.svg" alt="header-logo">
        </section>
        <nav class="nav nav__open__close">
            <label class="menu-display__label" for="MENU">
                <i class="fa-solid fa-bars"></i>
            </label>
            <input id="MENU" class="menu-display__checkbox" type="checkbox">
            <section class="nav__menu">
                <div>
                    <a class="nav__link" href="./index.html">Home</a>
                </div>
                <div>
                    <a class="nav__link" href="./chess-board/chess-board.html">Board</a>
                </div>
                <div>
                    <a class="nav__link" href="./formulario/contact-form.html">Contact</a>
                </div>
            </section>
            <section class="nav__social-media-container">
                <img id="nav__social-media-icon" src="./header-footer/facebook.png" alt="facebook">
                <img id="nav__social-media-icon" src="./header-footer/twitter.png" alt="twitter">
                <img id="nav__social-media-icon" src="./header-footer/youtube.png" alt="youtube">
                <img id="nav__social-media-icon" src="./header-footer/instagram.png" alt="instagram">
            </section>
        </nav>
    </header>
```

```css
...

    /* STYLE AND FUNCTION BURGUER BUTTON */

.menu-display__label {
    position: absolute;
    right: 0;
    margin-right: 30px;
    display: flex;
    justify-content: center;
}

.fa-solid {
    position: absolute;
    font-size: 1.5rem;

}

.fa-solid:active {
    transform: scale(0.9);
}

.nav__open__close:focus-within {
    animation: NavDisplay 0.4s 1 linear;
    transform-origin: top;
    visibility: visible;
}

    /* STYLE AND FUNCTION NAV MENU */

.menu-display__checkbox {
    visibility: visible;
    width: 1px;
    height: 1px;
}

...

@keyframes NavDisplay {
    0% {
        transform: scaleY(0);
        opacity: 1;
    }

    25% {
        transform: scaleY(0.25);
        opacity: 1;
    }

    50% {
        transform: scaleY(0.5);
        opacity: 1;
    }

    75% {
        transform: scaleY(0.75);
        opacity: 1;
    }

    100% {
        transform: scaleY(1);
        opacity: 1;
    }
}

```


# Deployment

The application has been deployed using GitHub Pages on the following url:

- https://marcogarciakoch.github.io/first-responsive-web/

# Local setup

Although it is deployed in GitHub Pages, it can be configured to run in a local environment.

To do so, the following steps must be performed:

1. Clone the monorepo
    > git clone https://github.com/MarcoGarciaKoch/first-responsive-web.git

2. Now you can test the app running the option `Open with Live Server` over the `index.html` file.