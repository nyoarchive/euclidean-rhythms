#euclidean-rhythms

A micro-library in javascript that calculates the rhythmical patterns of equally distributed pulses in available steps.
It implements the bjorklund's algorithm that is described by Godfried Toussaint in [The Euclidean algorithm generates traditional musical rhythms](http://cgm.cs.mcgill.ca/~godfried/publications/banff.pdf)

## Purpose

I wrote this library since I couldn't find out there an implementation that yields to the expected results as described on the paper above and also being well tested with unit tests and code coverage.

The current solution is a javascript interpretation of the python code that is retrieved from [atonalmicroshores.com](http://www.atonalmicroshores.com/2014/03/bjorklund-py/)

## Usage

### Node.js 
Run `npm install euclidean-rhythms`

Then in your javascript code:

`const er = require('euclidean-rhythms');`

`let cumbia = er.getPattern(3, 4)`
cumbia should be [ 1, 0, 1, 1 ]

`let cinquillo = er.getPattern(5, 8)`
cinquillo should be [ 1, 0, 1, 1, 0, 1, 1, 0 ]

and so on ...

### Browser
Use one of the prepared browser bundles from [unpkg.com](https://unpkg.com)
[https://unpkg.com/euclidean-rhythms/dist/bundle.umd.js](https://unpkg.com/euclidean-rhythms/dist/bundle.umd.js)
[https://unpkg.com/euclidean-rhythms/dist/bundle.umd.min.js](https://unpkg.com/euclidean-rhythms/dist/bundle.umd.min.js)

Then in your javascript code:

`var pattern = euclideanRhythms.getPattern(5, 13);`
 
 pattern should be : [ 1, 0, 0, 1, 0, 1, 0, 0, 1, 0, 1, 0, 0 ]

## Develop

Clone the git repository and cd into it. 
Run `npm run test` for executing the unit tests and `npm run build` to build a browser umd bundle with webpack.
