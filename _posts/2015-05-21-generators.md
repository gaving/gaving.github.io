---
layout:     post
title:      ES6 Generators
date:       2015-05-21 21:23:52
---

From [Hanging Up On
Callbacks](https://docs.google.com/presentation/d/1dtQNXP6mN9buEvFSlUqMdBJtmhJTVv59VOqdL3MmcTQ/edit#slide=id.g297a5dd29_052) 
(video [here](https://www.youtube.com/watch?v=s-BwEk-Y4kg)).

What does the following code output?

```javascript
function* powGenerator() {
  var result = Math.pow(yield "a", yield "b");
  return result;
}

var g = powGenerator();
log(g.next().value);
log(g.next(10).value);
log(g.next(2).value);
```

Hover below for the answer!

<div class="hidden">
<pre>
> "a"
> "b"
> 100
</pre>
</div>
