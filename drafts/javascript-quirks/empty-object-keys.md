# Java Script Quirks - Empty and null object keys

Java Script is known to have a lot of quirks. I can't cover them all in one post. But I'll try to cover one of them. OK, so surprisingly it is possible to create object case that are an empty strings. To make sure it's possible, I've tried it in Node. JavaScript doesn't complain even when you try to provide null as the valley for the key.

```
> const foo = {};
undefined
> foo[''] = 123;
123
> foo['']
123
> foo[null] = 456;
456
> foo[null]
456
>
```
