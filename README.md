# carousel-with-tabs

Demonstration showing a basic-carousel (a JavaScript-based component in the
[Basic Web Components](https://github.com/basic-web-components/basic-web-components)
project) being used with paper-tabs (a Polymer-based component).

[Live demo](http://basicwebcomponents.org/carousel-with-tabs/)

This demonstration is meant to confirm that the standard nature of web
components permits interoperability, not to say that this particular combination
of user interface elements is necessarily beautiful or useful.

One interoperability feature explored here is using Polymer's data binding
against an attribute defined by a non-Polymer element. In this case, the
`selected` attribute of the paper-tabs component is bound successfully to the
`selected-index` attribute of the basic-carousel component. This works because
both components support the same convention: when a property backing an
attribute changes, the component raises an event. The event's name is the
attribute's name, plus `-changed`, e.g., `selected-index-changed`.

Note that this binding works in both directions: clicking on a tab changes
the image shown and, in the other direction, using touch/keyboard/trackpad to
change the image shown updates the selected tab.
