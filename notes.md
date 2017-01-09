# Intro to Bones

## `package.json`
* make sure to *add your own name on line 2* and *update Node version to 6.7.0 or greater*
* all the scripts:
	* `test` and `test-watch`
	* `build` and `build-watch`
	* `start`
	* `seed`

## Bin: the symlink!
* created in `bin/mkapplink` and `bin/setup`
* we can require things differently
* symlink is checked/created in all package scripts

## DB
* look at `db/index`
	* [debug](https://www.npmjs.com/package/debug)
	* `require('APP')` possible because of symlink
* `db/seed`
* `db/models`
	* user model
	* Oauth model (auth will be covered in its own lecture)
	* no associations right now; you'd want to make those in `db/models/index`

## Server
* `server/start`
* `server/api` - add your additional routes here!
* `server/users` - please note the additional authorization middleware

## App
* React/Redux, React Router
* `.jsx` instead of `.js` files (less common in React world, but has benefits for text-highlighting, server-side rendering)

## Tests
	* writing front-end tests will be covered in its own lecture
	* tests are located in the same directory as the code that they're testing

## Possibly show...
* adding a "Tea" model
* seeding some Teas to the DB
* writing routes for Tea
* hooking that up to an "Teas" component

## Example:
* [link to diff showing adding a model, adding to seed file, adding BE routes, and adding component, reducer, and FE route](https://github.com/intersim/tea-bones/compare/82e7d373ace72eb0b4f3b23ea4e20dd0f0600440...2a5dd01f428c44b0cea208afcd841c6a437b490b)

## References:
	* `index.js`:
		* [`get` in `module.exports`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/get)
	* `db/index`:
		* [debug](https://www.npmjs.com/package/debug)