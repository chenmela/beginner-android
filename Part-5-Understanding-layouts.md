# Understanding layouts

Part 5 will be a bit longer than each of the preceding parts, so it is broken up into subsections, including Basics of layouts, Editing Layouts, and ConstraintLayout, each of which has its own Objectives heading.

## Editing layouts

### Objectives
In this subsection, you will learn:
- Two different ways to edit layouts
- How to view attributes for each element

### Design vs. Text view
There are two basic methods for manipulating layouts in Android Studio. One is modifying XML code directly and the other is using drag-and-drop functionality in the Layout Editor. Proficient Android developers are familiar with how to use both, often relying on the Layout Editor for a visual confirmation of the changes they make in XML code. To alternate between these two views, open the activity\_main.xml file and check out the Design and Text tabs at the bottom of the window.

The Text tab is pretty straightforward and displays the code just like any other file in your project. The Design tab shows you both a realistic and blueprint (schematic) view of your app. On the left, the palette shows you elements you can use in your project and the ComponentTree displays the Layout heirarchy comprised of Views and View Groups that we will discuss in a later subsection. 

### Viewing attributes
Select the `TextView` component and view the Attributes panel on the right-hand side. This will show you Common Attributes (attributes often used to describe a TextView) as well as All Attributes available for use with a TextView.

Find the `text` attribute in the Common Attributes panel and change the text to something new. Watch that it changes the text on the preview in the Design tab, as well as the `text` attribute in the Text tab.

## Basics of layouts

### Objectives
In this subsection, you will learn:
- What Views and ViewGroups are
- What LayoutParams are
- Common Android attributes modified in layouts
- The different types of layouts and when to use them

### Views and ViewGroups
As described before, a layout (like activity\_main.xml) describes the visual interface a user will see. Take a look at Figure 1 drawn in the [official Google documentation](https://developer.android.com/guide/topics/ui/declaring-layout) and read the section up to, but not including "Write the XML." As the documentation states, the entire tree, or hierarchy, represents the layout and is comprised of Views and ViewGroups. Type `<` in Android Studio in activity\_main.xml and see the suggestions that pop up. The documentation also explains two different ways to declare a layout - in XML (static), or in an Activity (dynamic).

There are many types of Android layouts, including LinearLayout, FrameLayout, and RelativeLayout, among others. All Android layouts share one particular characteristic, though - they are subclasses of ViewGroup, which itself is a subclass of View. Every ViewGroup can add Views as its children (which could be other layouts or more simple Views), making layout possibilities almost endless. In activity\_main.xml, the `TextView` is a View and a child of the `ConstraintLayout` ViewGroup.

### LayoutParams
You may notice the `ConstraintLayout` and `TextView` elements both contain `android:layout_width` and `android:layout_height` attributes. These are attributes that each View (remember the `ConstraintLayout`, although a ViewGroup, is also a View by virtue of subclassing) sets to indicate to their respective parents how they wish to be laid out. The parents, both ViewGroups (by virtue of having children), store this data in a `\<ViewGroup\_Name>.LayoutParams` class. For example, the `ConstraintLayout.LayoutParams` class contains the layout width and height parameters, which are then set by the child `TextView`. The top-level `ConstraintLayout`, or root View, does in fact have a parent which is not visible in this XML file but is part of the Android system and can be obtained in code.

### Common Android attributes
There are many, many attributes available for each Android XML element, but these are the most important:
- `android:layout\_width` and `android:layout\_height` These are used in a child View to specify the child's width and height, respectively, in relation to its parent. These attributes can be assigned the value `match_parent`, `wrap_content`, or a specific number of pixels (often density-independent). `match_parent` will expand the child View until the particular dimension matches that of the parent and `wrap_content` will expand the child View just enough to contain its inner contents.
- `android:id` This is used to specify a unique identifier for the element. This ID can then be referenced in code in order to assign behavior to the element or modify its appearance. It is good coding practice to make IDs unique across the entire component tree.

In order to explore the different width and height settings, change the background color of the `TextView` element. You can do so by adding the attribute `android:background` to the TextView and assigning the value `@color/colorAccent`. Check that the color is now pink, the default accent color for this app.

Now, set the `android:layout_width` attribute to `match_parent` and notice that the TextView has expanded to the width of the entire screen, or more specifically the bounds of its parent ConstraintLayout. You will also notice the text is no longer centered in the TextView. To change this, modify the `android:gravity` attribute to be `center` either in the Design or Text tab. This is an important reason to know what different attributes do - although it may have seemed that the text was centered in the TextView, it was simply the consequence of a different attribute.

Now, add an appropriate ID to the TextView, calling it `mainTextView` or something else informative. You will notice the suggestions to choose either the `@+id/` or `@android:` prefix. Choose the first, so that your code reads `android:id="@+id/mainTextView"`. The `@` indicates the ID is a project resource. You will notice this in `@color/colorAccent`, too, because a color is also a resource. The `+` indicates the ID is being created for the first time and should be added to the project resources.

### Types of layouts
Some, but not all, Android layouts are listed below with their common uses.
- `LinearLayout` Used to align children in either a vertical or horizontal direction.
- `RelativeLayout` Used to arrange children with respect to one another.
- `FrameLayout` Used to stack children on top of each other (think of  a stack of books growing from your phone screen up to the sky).
- `TableLayout` Used to arrange elements into rows and/or columns.
- `ConstraintLayout` A more flexible version of various layouts intended to reduce nested hierarchy patterns that reduce performance.

### Ideas
- sp/dp 
- changing font size to demonstrate wrap\_content
- Breaking up this section into 3 separate ones
- Adding more activities
- Specifying an Activity section with a particular heading



