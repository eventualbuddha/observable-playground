<!--
name:		
title:		filter
pageTitle:	RxJS filter operator example + marble diagram
desc:		
docsUrl:	https://rxjs.dev/api/operators/filter
-->

```js
const { rxObserver } = require('api/v0.3');
const { timer } = require('rxjs');
const { filter, take } = require('rxjs/operators');


const source$ = timer(0, 5).pipe(
    take(4)
  );

const result$ = source$.pipe(
    filter(x => x % 2)
  );

source$.subscribe(rxObserver());
result$.subscribe(rxObserver());

```
