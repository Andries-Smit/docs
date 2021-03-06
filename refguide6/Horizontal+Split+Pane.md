---
title: "Horizontal Split Pane"
space: "Reference Guide 6"
parent: "Container+Widgets"
---


The horizontal split pane is deprecated since version 5.18.0 in favor of the more powerful [Scroll Container](Scroll+Container).

A horizontal split pane creates a region that is split in two by a horizontal divider. In the client the divider can be dragged up and down by the end user.

<div class="alert alert-info">{% markdown %}

![](attachments/819203/918038.png)
An empty horizontal split pane.

{% endmarkdown %}</div>

## Common Properties

{% snippet Name+Property.md %}

{% snippet Class+Property.md %}

{% snippet Style+Property.md %}

## General Properties

### Splitter position

This property determines the initial position of the dividing line in percentages. The default value of 50 will place the line exactly halfway the split pane.

_Default value:_ 50

### Animated resize

This property indicates whether re-sizing, by dragging the divider, is visualized in real time.

_Default value:_ False

### Height

The height property determines the height of the split pane. A height of 0 will set the pane's height to the default defined in the theme.

_Default value:_ 0
