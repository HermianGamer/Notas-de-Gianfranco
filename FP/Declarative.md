[[Functional Programming]] aims to be _declarative_. We prefer to declare _what_ we want the computer to do, rather than muck around with the details of _how_ to do it.

Let's take an extreme example and pretend we wanted to style a webpage with [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)(Obviously a hypothetical because, well, why would anyone want to work on the frontend???)


The following CSS changes all [buttons](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button) elements to have red text:

```css
button {
  color: red;
}
```

It does _not_ execute line-by-line like an imperative language. Instead, it simply declares the desired style, and it's up to a web browser to figure out how to apply and display it.