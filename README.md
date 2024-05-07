[![@taktikorg/soluta-voluptates-omnis](https://cloud.githubusercontent.com/assets/399776/13906899/1de62f0c-ee9f-11e5-95c0-c515fee8e918.png)](https://@taktikorg/soluta-voluptates-omnis.github.io)

[![NPM Version](https://img.shields.io/npm/v/@taktikorg/soluta-voluptates-omnis.svg?branch=master)](https://www.npmjs.com/package/@taktikorg/soluta-voluptates-omnis) [![Build Status](https://github.com/taktikorg/soluta-voluptates-omnis/actions/workflows/test.yml/badge.svg?branch=master)](https://github.com/taktikorg/soluta-voluptates-omnis) [![Coverage Status](https://coveralls.io/repos/github/@taktikorg/soluta-voluptates-omnis/@taktikorg/soluta-voluptates-omnis/badge.svg?branch=master)](https://coveralls.io/github/@taktikorg/soluta-voluptates-omnis/@taktikorg/soluta-voluptates-omnis?branch=master) [![License](https://img.shields.io/npm/l/@taktikorg/soluta-voluptates-omnis.svg)](https://github.com/taktikorg/soluta-voluptates-omnis/blob/master/LICENSE)

# @taktikorg/soluta-voluptates-omnis

Stateless React Components for Bootstrap 5.

If you're using Bootstrap 4, you'll need to use [Reactstrap v8](https://deploy-preview-2356--@taktikorg/soluta-voluptates-omnis.netlify.app/)

## Getting Started

Follow the [create-react-app instructions](https://create-react-app.dev/docs/getting-started) to get started and then follow the @taktikorg/soluta-voluptates-omnis version of [adding bootstrap](#adding-bootstrap).

### tl;dr

 ```
npx create-react-app my-app
cd my-app/
npm start
```
or,  if npx (Node >= 6 and npm >= 5.2 ) not available 

```
npm install -g create-react-app

create-react-app my-app
cd my-app/
npm start
``` 

Then open [http://localhost:3000/](http://localhost:3000/) to see your app. The initial structure of your app is setup. Next, let's [add @taktikorg/soluta-voluptates-omnis and bootstrap](#adding-bootstrap).

### Adding Bootstrap

Install @taktikorg/soluta-voluptates-omnis and Bootstrap from NPM. Reactstrap does not include Bootstrap CSS so this needs to be installed as well:

```
npm i bootstrap
npm i @taktikorg/soluta-voluptates-omnis react react-dom
```

Import Bootstrap CSS in the ```src/index.js``` file:

```js
import 'bootstrap/dist/css/bootstrap.css';
```

Import required @taktikorg/soluta-voluptates-omnis components within ```src/App.js``` file or your custom component files:

```js
import { Button } from '@taktikorg/soluta-voluptates-omnis';
```

Now you are ready to use the imported @taktikorg/soluta-voluptates-omnis components within your component hierarchy defined in the render
method. Here is an example [`App.js`](https://gist.github.com/Thomas-Smyth/006fd507a7295f17a8473451938f9935) redone
using @taktikorg/soluta-voluptates-omnis.

### Dependencies

##### Required Peer Dependencies

These libraries are not bundled with Reactstrap and required at runtime:

  * [**react**](https://www.npmjs.com/package/react)
  * [**react-dom**](https://www.npmjs.com/package/react-dom)

## About the Project

This library contains React Bootstrap components that favor composition and control. The library does not depend on jQuery or Bootstrap javascript. However, [Poppers.js](https://popper.js.org/) via [react-popper](https://github.com/popperjs/react-popper) is relied upon for advanced positioning of content like Tooltips, Popovers, and auto-flipping Dropdowns.

There are a few core concepts to understand in order to make the most out of this library.

1. Your content is expected to be composed via props.children rather than using named props to pass in Components.

    ```js
    // Content passed in via props
    const Example = (props) => {
      return (
        <p>This is a tooltip <TooltipTrigger tooltip={TooltipContent}>example</TooltipTrigger>!</p>
      );
    }

    // Content passed in as children (Preferred)
    const PreferredExample = (props) => {
      return (
        <p>
          This is a <a href="#" id="TooltipExample">tooltip</a> example.
          <Tooltip target="TooltipExample">
            <TooltipContent/>
          </Tooltip>
        </p>
      );
    }
    ```

2. Attributes in this library are used to pass in state, conveniently apply modifier classes, enable advanced functionality (like tether), or automatically include non-content based elements.

    Examples:

    - `isOpen` - current state for items like dropdown, popover, tooltip
    - `toggle` - callback for toggling `isOpen` in the controlling component
    - `color` - applies color classes, ex: `<Button color="danger"/>`
    - `size` - for controlling size classes. ex: `<Button size="sm"/>`
    - `tag` - customize component output by passing in an element name or Component
    - boolean based props (attributes) when possible for alternative style classes or `visually-hidden` content


## [Documentation](https://@taktikorg/soluta-voluptates-omnis.github.io)

https://@taktikorg/soluta-voluptates-omnis.github.io

Documentation search is powered by [Algolia's DocSearch](https://community.algolia.com/docsearch/).

## [CodeSandbox Examples](https://github.com/@taktikorg/soluta-voluptates-omnis/code-sandbox-examples)

Here are some ready-to-go examples for [CodeSandbox](https://codesandbox.io/) that you can experiment with.

https://github.com/@taktikorg/soluta-voluptates-omnis/code-sandbox-examples

## [Contributing](CONTRIBUTING.md)

## Development

Install dependencies:

```sh
yarn install
```

Run examples at [http://localhost:8080/](http://localhost:8080/) with webpack dev server:

```sh
yarn start
```

Run tests & coverage report:

```sh
yarn cover
```

Watch tests:

```sh
yarn test
```

## Releasing

Release branches/versioning/notes will be automatically created and maintained by the [release-please](https://github.com/googleapis/release-please) github action. When you're ready to publish the release, just merge the release branch. The release will be created, the new package will be published, and the updated docs will be deployed to https://@taktikorg/soluta-voluptates-omnis.github.io/.

## In the wild

Organizations and projects using `@taktikorg/soluta-voluptates-omnis`

- [airframe-react](https://github.com/0wczar/airframe-react) - [demo](http://dashboards.webkom.co/react/airframe/) - Airframe provides all the components a developer needs to build data-intensive web apps using React.
- [component-template](https://@taktikorg/soluta-voluptates-omnis.github.io/component-template/)
- [video-react](https://video-react.github.io/)
- [CoreUI-Free-Bootstrap-Admin-Template](https://github.com/mrholek/CoreUI-Free-Bootstrap-Admin-Template) - [demo](http://coreui.io/demo/React_Demo/#/)
- [Admin dashboard example app built with @taktikorg/soluta-voluptates-omnis](https://github.com/reduction-admin/react-reduction) - [demo](https://reduction-admin.firebaseapp.com/)
- [DevExtreme React Grid](https://devexpress.github.io/devextreme-reactive/react/grid/) - It's a stateless data grid built on top of `@taktikorg/soluta-voluptates-omnis` with paging, sorting, filtering, grouping, selection, editing and virtual scrolling features.
- [DevExtreme React Chart](https://devexpress.github.io/devextreme-reactive/react/chart/) - A chart built on top of `@taktikorg/soluta-voluptates-omnis` that visualizes data using a variety of series types, including bar, line, area, scatter, pie, and more.
- [@taktikorg/soluta-voluptates-omnis-scrollspy](https://github.com/keidrun/@taktikorg/soluta-voluptates-omnis-scrollspy/) - [demo](https://keidrun.github.io/@taktikorg/soluta-voluptates-omnis-scrollspy/)
- [formstrap](https://github.com/pedox/formstrap/) - [demo](https://pedox.github.io/formstrap/) - Let your `@taktikorg/soluta-voluptates-omnis` input component integrate seamlessly using `Formik` 
- [Jimu UI](https://developers.arcgis.com/experience-builder/api-reference/jimu-ui/) - [demo](https://developers.arcgis.com/experience-builder/storybook/?path=/story/welcome--page) - The UI library for [ArcGIS Experience Builder](https://developers.arcgis.com/experience-builder/)  mapping platform.

Submit a PR to add to this list!

Looking to build, document and publish reusable components built on top of `@taktikorg/soluta-voluptates-omnis`? Consider forking https://github.com/@taktikorg/soluta-voluptates-omnis/component-template to kickstart your project!
