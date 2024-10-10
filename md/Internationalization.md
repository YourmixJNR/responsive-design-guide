# Internationalization

The goal of responsive design is to make your content available to everyone. Applying that same philosophy to human languages is the driving force behind internationalization—preparing your content and designs for an international audience.

### [Logical properties](https://web.dev/learn/design/internationalization#logical_properties)

English is written from left to right and top to bottom, but not all languages are written this way. Some languages like Arabic and Hebrew read from right to left, and some Japanese typefaces read vertically instead of horizontally. To accommodate these writing modes, logical properties were introduced in CSS.

If you write CSS, you may have used directional keywords like "left", "right", "top", and "bottom." Those keywords refer to the physical layout of the user's device.

[Logical properties](https://web.dev/learn/css/logical-properties), on the other hand, refer to the edges of a box as they relate to the flow of content. If the writing mode changes, CSS written with logical properties will update accordingly. That's not the case with directional properties.

Whereas the directional property `margin-left` always refers to the margin on the left side of a content box, the logical property margin-inline-start refers to the margin on the left side of a content box in a left-to-right language, and the margin on the right side of a content box in a right-to-left language.

Use logical properties instead.Whereas the directional property margin-left always refers to the margin on the left side of a content box, the logical property `margin-inline-start` refers to the margin on the left side of a content box in a left-to-right language, and the margin on the right side of a content box in a right-to-left language.

In order for your designs to adapt to different writing modes, avoid directional properties. Use logical properties instead.

**Don't**

```css
.byline {
  text-align: right;
}
```

**Do**

```css
.byline {
  text-align: end;
}
```

In a language like English where text flows from left to right, `inline-start` corresponds to "left" and `inline-end` corresponds to "right".

Likewise, in a language like English where the text is written from top to bottom, `block-start` corresponds to "top" and `block-end` corresponds to "bottom."

Take a common pattern like an icon next to some text or a label next to a form field. Instead of thinking "the label should have a margin on the right," think "the label should have a margin on the end of its inline axis."

**Don't**

```css
label {
  margin-right: 0.5em;
}
```

**Do**

```css
label {
  margin-inline-end: 0.5em;
}
```

### [Identify page language](https://web.dev/learn/design/internationalization#identify_page_language)

It's a good idea to identify the language of your page by using the `lang` attribute on the `html` element.

Declaring the language of your document is useful for search engines. It's also useful for assistive technologies like screen readers and voice assistants. By providing language metadata you're helping these kinds of speech synthesizers pronounce your content correctly.

The `lang` attribute can go on any HTML element, not just `html`. If you switch languages in your web page, indicate that change. In this case, one word is in German:

```html
<p>I felt some <span lang="de">schadenfreude</span>.</p>
```

### [Identify a linked document's language](https://web.dev/learn/design/internationalization#identify_a_linked_documents_language)

There's another attribute called hreflang which you can use on links. The hreflang takes the same language code notation as the lang attribute and describes the linked document's language. If there's a translation of your entire page available in German, link to it like this:

```html
<a href="/path/to/german/version" hreflang="de">German version</a>
```

You can also use the hreflang attribute on the link element. This goes in the head of your document:

```html
<link href="/path/to/german/version" rel="alternate" hreflang="de" />
```

### [Think internationally](https://web.dev/learn/design/internationalization#think_internationally)

Attributes like `lang` and `hreflang` make your HTML more meaningful for internationalization. Likewise, logical properties make your CSS more adaptable.

If you're used to thinking in terms of `top`, `bottom`, `left`, and `right`, it might be hard to start thinking of `block start`, `block end`, `inline start` and `inline end` instead. But it's worth it. Logical properties are key to creating truly responsive layouts.

## [Check your understanding](https://web.dev/learn/design/internationalization#check_your_understanding)

Test your knowledge of internationalization.
