# create react app typescript with all necessary installation

## create react app

`$ create-react-app --scripts-version=react-scripts-ts`

## -------------------first commit git init

## lint and prettier

 are already installed with cra

 in vscode set:

      "tslint.autoFixOnSave": true,

## add no unused parameters in tsconfig.json

      "compilerOptions": {
            "noUnusedParameters": true,
      }

## install enzyme

`$ npm i -D enzyme enzyme-adapter-react-16 @types/enzyme @types/enzyme-adapter-react-16`

* The adapter will also need to be configured in your global setup file (src/setupTests.ts)

      import { configure } from 'enzyme';
      import * as Adapter from 'enzyme-adapter-react-16';

      configure({ adapter: new Adapter() });

* rewrite App.test.tsx:

      import * as React from 'react';
      import { shallow } from 'enzyme';
      import App from './App';

      it('renders without crashing', () => {
            shallow(<App />);
      });

* verify it works:

  `$ npm test`

* add bootstrap theme to src/index.tsx:

      import "../node_modules/bootstrap/dist/css/bootstrap.min";

## install storybook

      follow the official [guide](https://storybook.js.org/basics/guide-react/)