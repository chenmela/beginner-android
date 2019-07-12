# Understanding XML

## Objectives
In Part 4, you will learn:
- What XML is
- How XML is used in Android
- How to read XML
- The definitions of elements, tags, content, and attributes

## XML and Android
XML, which stands for eXtensible Markup Language, is an important component of most Android applications. It is a language for organizing data in a lightweight fashion that is understandable by both human developers and machines. In Android development in particular, XML is used to describe several kinds of data including layouts (defines user interface design), strings, colors, styles, dimensions, drawable objects, and the application components (including activities, services, permissions, and packages). This workshop will cover layouts, strings, and colors in more detail in upcoming sections.

If you feel comfortable reading XML, you may skip this section.

## Reading XML
First, navigate to `activity_main.xml`, located under app > res > layoutwhen viewing the files in the Android Project view. If you need a refresher on navigating the file structure, review the [Google codelab](https://codelabs.developers.google.com/codelabs/build-your-first-android-app/index.html?index=..%2F..index#2) linked earlier.

### Elements, tags, and content
There are two XML elements in this file. The first is the `androidx.constraintlayout.widget.ConstraintLayout` element (or just `ConstraintLayout` for short) and the second is the `TextView` element. Typically, each XML element has a openingtag, such as `<section>` and closing tag, such as `</section>`. You can identify an opening tag because it is enclosed by `<` and `>` and a closing tag because it is enclosed by `</` and `>`. For example, lines 2-7 comprise the `ConstraintLayout` opening tag and line 18 comprises the closing tag.

At first glance, it looks like the `TextView` element doesn't have a closing tag. In fact, it does not have an opening tag either, since it is enclosed by `<` and `/>`, a combination you haven't seen yet. This is the third type of tag, called an empty-element tag, and it is used as shorthand for the combination of both opening and closing tag. So `<hello_tag></hello_tag>` is the same as `<hello_tag/>`. 

Between the opening and closing tags, you also have the option to include content. There is not an example in this file, but you can find one in strings.xml, which is located in the app > res > values folder. On line 2, the `string` element contains the content `NumberGenerator` between its opening and closing tags. You would not use the empty-element tag if you needed to put some content in between the opening and closing tags.

### Attributes
Navigate back to `activity_main.xml` (you will see recent files as tabs on top) and take a look at the `ConstraintLayout` opening tag. Here, there are several attributes, or name-value pairs, that indicate even more data about the `ConstraintLayout` element. Every XML attribute is comprised of a name (like `tools:context`) followed by `=` and the corresponding key in quotations (like `".MainActivity"`). This particular attribute links the main layout (design) with the main activity (functionality). Although all the attribute names in this file contain a colon, this is not always the case. XML attributes can be found in both opening tags and empty-element tags (as you can see with the `TextView` empty-element tag in lines 9-16), but not closing tags. 

