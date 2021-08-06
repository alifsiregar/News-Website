# News Website

_Good news for good people!_

"News Website" is a news website focusing on the business, healthcare, and sports category. This website is made in order to complete one of the recruitment stage of YesDok Indonesia.

## Tech Stack

* Nuxt.JS
* Javascript
* VueX
* TailwindCSS

## Structure

There are 7 __folders__ in this project:

1. `assets`
2. `components`
3. `layouts`
4. `pages`
5. `services`
6. `static`
7. `store`

`assets` is where the images and data are located. `components` contains components that are used in the `pages` folder, which has the pages inside. In order to add more pages and routes, add new files in the `pages` folder and it will be created automatically. `layouts` contains the default layout and the error layout in case there is an error. `services` is where the URLs for HTTP requests are stored. `static` contains the favicon logo, in order to change the favicon just change the logo and it will be good to go. `store` has the VueX store inside, with the getters and mutations as well.


## Documentation

In order to start the app in development mode,  you can run this syntax in the project directory:

### `npm run dev`

By default, the app will open in [http://localhost:3000](http://localhost:3000). The page also has hot reload, which means that it will refresh if you make any edits.

If you want to build the app for production, you can run this syntax in the project directory:

### `npm run build`

This will bundle the project and optimizes the build with webpack for production mode.

Last, if you want to start the app server, run this syntax in the project directory:

### `npm run start`

This will start the production server and can then be deployed in any deployment sites.

