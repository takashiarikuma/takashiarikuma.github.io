---
layout: post
title: "New DataFlex Web Grid Layou"
date: 2023-10-31
last_modified_at: false
tags: DataFlex
image:
  path: /assets/images/dataflex_studio_faded.jpg.1356x526.2.jpg
---

![DataFlex](/assets/images/DataFlex.png){: .left}

DataFlex 23.0 introduces for Web Applications a new layout called Grid Layout. Typical Web pages are single axis oriented design based on Flexible Box Layout. The new Grid Layout is optimized for 2 a dimensional layout. In simple words, the Grid Layout allows to control the vertical position of a control in the page.
To use this new layout type, simple change the peLayoutType web property to ltGrid on web container objects:

{% highlight DataFlex %}

    Object oWebMainPanel is a cWebPanel
        Set piColumnCount to 16
        Set peLayoutType to ltGrid
        Set psRowHeights to "0/175 1/240 2/75 3/75"

{% endhighlight %}

On the previous code the columns are set to 16. This is not changed from previous versions. The new property peLayoutType is set to ltGrid which allows to set the layout to grid and psRowHeights contains the detail of each row height (px). Row 0 is 175px, row 1 is 240px, row 2 is 75px, row 3 is 75px.

When pgLayoutType is set to ltInherit the container will take the parent layout type.
