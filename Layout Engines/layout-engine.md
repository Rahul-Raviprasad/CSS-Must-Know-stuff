# Layout Engines

Wiki defines Layout Engines as
"A layout engine is a software component that combines content and formatting information for electronic or printed display."

List of Layout Engines https://en.wikipedia.org/wiki/List_of_layout_engines

## Web Browser Engines

The first web browsers were monolithic. They used various techniques inherited from text processing, such as regular expressions[citation needed], to parse HTML into a visual representation. Later they adopted a more modular approach and were split into a host application and an engine.

#### The engine
  does most of the work. It essentially takes a URL and a set of window (content area) rectangle coordinates as arguments. It then retrieves the document corresponding to the URL and paints a graphical representation of it in the given rectangle. It also handles links, forms, cookies, client-side scripting, plug-in loading, and other matters.
#### The host application
  provides the menu bar, address bar, status bar, bookmark manager, history and preferences functionality (among other things). It embeds the engine and serves as an interface between the user, the engine, and the underlying operating system. Since it provides the graphical elements surrounding the area in which the engine paints documents, programmers sometimes use the term chrome to refer to its user interface (like the chrome surrounding a car).

This modular approach has the advantage that it then becomes easy to embed web-browser engines in a variety of applications. For example, the same engine used by a web browser can be used by an email client to display HTML email. On-line help systems integrated in applications have largely moved from using custom formats to using standard HTML displayed with a web-browser engine. The EPUB 3 e-book standard uses a layout engine to render XHTML and CSS.

Taken from https://en.wikipedia.org/wiki/Web_browser_engine

Link to comparison of Layout engine https://en.wikipedia.org/wiki/Comparison_of_layout_engines_(Cascading_Style_Sheets)

#### Explore later
Creating you own layout engine https://limpet.net/mbrubeck/2014/08/08/toy-layout-engine-1.html
