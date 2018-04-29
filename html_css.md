# HTML & CSS

`section`:	Sections grouped around a specific theme.

`article`:	Complete or self-contained compositions such as a blog post or a widget. As a rule of thumb, only use if the content makes sense on it’s own (RSS feed, tweet post, facebook post, etc).

`nav`:	Navigation blocks.

`aside`:	Complementary content such as sidebars.

`header`:	Indicates the header inside a section.

`footer`:	Indicates the footer inside a section.
 
Semantic HTML is HTML with a meaning. The tag itself doesn’t matter to your end user. They don’t care if something is a div or p tag.

On the other hand, semantics do **give your page meaning**. Consider a well structured blog post.

In addition, semantic HTML is vital to a website’s SEO (Search Engine Optimization). When an SEO crawler such as Google’s looks at your website, it sees something like this. It doesn’t infer meaning based off of what it sees, it infers meaning based off of tags and attributes.

## Block Elements

<img src="https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_665e61b46e5146c07a02cde10029d919.png">

A block-level element begins a new line on the webpage and, if no width is set, extends the full width of the available horizontal space of its parent element.

Block-level elements create large blocks of content like paragraphs or page divisions. They can contain inline elements, as well as other block-level elements.

The `div` tag is an element that represents a box. It is commonly used to separate sections in the web page or wrap content for styling. The `div` has no semantic value (meaning), as we will discuss in the next section.

**By default, the `div` content will occupy the full width of its container (body by default).**

**If `div` has no content inside, the height will be zero by default.**

## Inline Elements

<img src="https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_204ec773d202cb71b80805ea60a3269f.png">

Inline elements flow like text. They don’t start a new line and they are shown right next to the previous element.

Unlike a block element, an inline element will occupy only the size of its content.

A `<span>` tag is an inline, generic wrapper for text. These are useful for applying styles to specific bits of text, as you will see in future CSS sections.

The span has no semantic meaning other than “Hey, this text is special and I’m going to change it somehow”.

### Semantic Inline Elements 

`a`:	A link used to navigate to different pages, or a different place in the same page.

`br`:	Denotes a line break that is part of the content. For example, in a poem where one line must always be broken after another. This is not meant for moving text from one line to another for stylistic purposes.

`em`:	Italic text that is meant to emphasize contained text.

`small`:	Used for side comments, or small print text.

`i`:	Italic text that is meant to be said in a different tone, or contains a defintion of some sort.

b`:	Bold text. Is not meant to put semantic meaning on text, it’s simply stylistic. A common example is a product name on an ecommerce site.

`strong`:	Indicates the content contained within is very important.

## CSS Selectors

In the CSS, a class selector is a name preceded by a full stop (“.”) and an ID selector is a name preceded by a hash character (“#”). The difference between an ID and a class is that an ID can be used to identify one element, whereas a class can be used to identify more than one.