---
title: "Angular calling fromEvent for a component containing ngIf"
date: "2020-07-24"
draft: false
tags:
- angular
---

In Angular, for a component conditionally render with an `ngIf` directive, to use `fromEvent` to obtain an observable from an event of it, one cannot simply declare `ElementRef` property annotated with `@ViewChild` and invoke `fromEvent` within `ngAfterViewInit` since the `ElementRef` is undefined when the `ngIf` is evaluated false. To solve this problem, we can use a setter for the `ElementRef` property. The following is a simple example.

Excerpt from template .html file:

```html
<button *ngIf="showButton" #bigButton>Click</button>
```

Excerpt from source code .ts file:

```javascript
@ViewChild('bigButton', { read: ElementRef }) set bigButton(content: ElementRef | null) {
  if (content) {
    fromEvent(content.nativeElement, 'click')
      .subscribe({ next: () => console.log('Clicked!') });
  }
}
```