Foreword
========
As start point I got working app by link: http://www.sanskrit-lexicon.uni-koeln.de/scans/MWScan/2014/web/webtc2/

Motivation
==========
1. Update UI. There is some issues for improvement UI, but for me it will be easy to fix it on new modern platform.
2. Mobile version
3. Functional Feature improvements - add smart search for instance...
4. Component model - it will allow to work on the UI to several developers in parallel at once

DESIGN
======
1 I want to bring to your attention on two products:
https://app.zeplin.io/projects.html - this is mostly for presentation layer
https://www.axure.com/ - more complicated tool.
I will create design forms/screens, and you will suggest or make a changes yourself. (Screens I may send directly by email for details as example)

ARCHITECTURE
============
All code divided to parts:
- backend
- web frontend
- mobile frontend

Backend will be REST-full Web Services which are respond json's format responses. Today backend return simple html. I apologise that it will not be hard to extend it for json responds on existing source code without huge refactoring.
Frontend will be based on React.JS and Redux
Mobile version will be based on React Native library.

Links:
React: https://facebook.github.io/react/
React Native: https://facebook.github.io/react-native/
Redux: http://redux.js.org/

PROTOTYPE
=========
The basic aim of this stage is validate some solutions, behaviors...
Some easy prototype may be create in simple html file and directly open it in browser without place in webserver.
Some complex prototype may be done in axure.

Following I show my action log when another one has been done.

DEVELOPMENT
===========
Create demo, in console:

1. Download and install Node.JS https://nodejs.org/en/
Node.JS isn't necessary for production, it's only for development case

2. In console type:
npm install -g create-react-app

This is a Facebook tool

create-react-app sanskrit-lexicon

Result: success creation project and suggestions:
cd sanskrit-lexicon
npm start

or other commands:
npm start
npm run build
npm test
npm run eject

Here is development environment setup.

MY PROTOTYPE LOG
================
AIM: create search component. In this issue context - represent how to easy to solve problems which was not trivial years ago.
1. I wrote index.html and open in browser. First component "HelloWorld" has been shown on the page.
2. Duplicate index.html as index-2.html and add list of words. Stub data incoming from server WORDS json array (made search by "om" screenshot: get_stub_data.png).
Create 3 components:
App - top level component agregator
Word - item in list
WordsList - list of stubbed words.
Fetching data from server instead of stubbing will be shown later.
3. Duplicate index-2.html as index-3.html and add css for pretty look.
4. Duplicate index-3.html as index-4.html and add search component.

ISSUES
======
1. Working with cookies - fix by using https://github.com/thereactivestack/react-cookie
I think it will be useful to store user tag's in cookies, for instance: last viewed words, tags by book, vocabulary, last corrections, and so on...
2. Corrections - fix by store data for corrections to data model, stored in state and use in react component Correction.
3. It needs actualize existing issues and make review

PROBLEMS
========
1. React Native still have 0.x version, that's why there is risk of global changes and absence back reward.
2. Mobile version for iOS and Android can't have one react native code, there is not full cross platform support.
3. Create new component take a time, that is why before writing it will be better detail prototype component and test for usability.
4. Redux - data model and it's evolution is unclear for me. For models with a large number of the relational fields in tables the operations with Redux is difficult. Therefore, whenever possible, it is necessary to research the existing data model and refactor it in advance before development of components.
If the datamodel will be more complex it will be useful investigate redux-orm  https://github.com/tommikaikkonen/redux-orm
5. Fonts... It's unclear for me is the true type exists on mobile both iOS and Android devices.
6. I haven't designer skills. I try to ask the brother to develop styles for the application - he is an artist, the designer. Maybe he will develop in PhotoShop and screen forms that they then could be exported to Zeplin.

RESUME
======
Thank you that have found time and have read up to the end. I have tried to describe a full cycle of development on the React and to show that improvement UI by transition to these technology not such a complex challenge as could seem on at first.
