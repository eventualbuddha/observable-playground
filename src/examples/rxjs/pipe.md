<!--
name:		
title:		pipe
pageTitle:	RxJS pipe operator example + marble diagram
desc:		
docsUrl:	https://rxjs.dev/api/index/function/pipe
-->

```js
const { rxObserver } = require('api/v0.3');
const { timer } = require('rxjs');
const { filter,take } = require('rxjs/operators');


timer(0, 10)
  .pipe(
    take(10),
    filter(x => x % 2)
  )
  .subscribe(rxObserver('Odd'));

```
