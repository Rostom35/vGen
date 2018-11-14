# vGen
We want to develop a language for VideoGen, a system that will generate, from textual specifications, a video generator on the Web.
## Classes

<dl>
<dt><a href="#app.js">app.js</a></dt>
<dd></dd>
<dt><a href="#error.js">error.js</a></dt>
<dd></dd>
<dt><a href="#header.js">header.js</a></dt>
<dd></dd>
<dt><a href="#home.js">home.js</a></dt>
<dd></dd>
<dt><a href="#loader.js">loader.js</a></dt>
<dd></dd>
<dt><a href="#navbar.js">navbar.js</a></dt>
<dd></dd>
<dt><a href="#page.js">page.js</a></dt>
<dd></dd>
<dt><a href="#router.js">router.js</a></dt>
<dd></dd>
</dl>

## Functions

<dl>
<dt><a href="#customMessage">customMessage(info)</a> ⇒ <code>String</code></dt>
<dd><p>This method constructs a message that will be used to notify a user or a developer</p>
</dd>
<dt><a href="#createElementFromSelectorOrID">createElementFromSelectorOrID(module)</a> ⇒ <code>Element</code></dt>
<dd><p>An element is either identified
by its id or selector</p>
</dd>
<dt><a href="#resolveScriptsLocation">resolveScriptsLocation(url, module)</a> ⇒ <code>String</code></dt>
<dd></dd>
<dt><a href="#appendErrorElement">appendErrorElement(error, errorType)</a></dt>
<dd><p>Construct error element and passes error information to the custom element</p>
</dd>
<dt><a href="#goToRoute">goToRoute(path, force, event)</a></dt>
<dd><p>Perform a routing to the path</p>
</dd>
<dt><a href="#renderRoute">renderRoute(targetRoute)</a></dt>
<dd><p>Display the appropriate component for the target route</p>
</dd>
</dl>

<a name="app.js"></a>

## app.js
**Kind**: global class  
<a name="new_app.js_new"></a>

### new app.js()
NovatioApp the app(root) element

<a name="error.js"></a>

## error.js
**Kind**: global class  
<a name="new_error.js_new"></a>

### new error.js()
NovatioError the error element which is used to render a message to the user

<a name="header.js"></a>

## header.js
**Kind**: global class  
<a name="new_header.js_new"></a>

### new header.js()
NovatioHeader the header element

<a name="home.js"></a>

## home.js
**Kind**: global class  
<a name="new_home.js_new"></a>

### new home.js()
NovatioHome the home element

<a name="loader.js"></a>

## loader.js
**Kind**: global class  
<a name="new_loader.js_new"></a>

### new loader.js()
NovatioLoader the spinner element

<a name="navbar.js"></a>

## navbar.js
**Kind**: global class  
<a name="new_navbar.js_new"></a>

### new navbar.js()
NovatioNavbar

<a name="page.js"></a>

## page.js
**Kind**: global class  
**See**: <a href="https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_custom_elements">HTMLElement</a>  
<a name="new_page.js_new"></a>

### new page.js()
NovationPage an HTMLElement is respensible for loading component from module to the container

<a name="router.js"></a>

## router.js
**Kind**: global class  
<a name="new_router.js_new"></a>

### new router.js()
NovatioRouter is responsible for routing to the appropriate module

<a name="customMessage"></a>

## customMessage(info) ⇒ <code>String</code>
This method constructs a message that will be used to notify a user or a developer

**Kind**: global function  
**Returns**: <code>String</code> - The constructed message  

| Param | Type | Description |
| --- | --- | --- |
| info | <code>String</code> | Information about the error |

<a name="createElementFromSelectorOrID"></a>

## createElementFromSelectorOrID(module) ⇒ <code>Element</code>
An element is either identified
by its id or selector

**Kind**: global function  
**Returns**: <code>Element</code> - a wrapper element where the module should be loaded  
**Throws**:

- <code>Error</code> an exception could be thrown during execution if a module definition don't have tag or id key


| Param | Type | Description |
| --- | --- | --- |
| module | <code>Route</code> | the actual route |

<a name="resolveScriptsLocation"></a>

## resolveScriptsLocation(url, module) ⇒ <code>String</code>
**Kind**: global function  
**Returns**: <code>String</code> - the exact url to where load script  

| Param | Type | Description |
| --- | --- | --- |
| url | <code>String</code> | script url to load |
| module | <code>Route</code> | the actual route |

<a name="appendErrorElement"></a>

## appendErrorElement(error, errorType)
Construct error element and passes error information to the custom element

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| error | <code>Error</code> | Object that describe the error that was occurred |
| errorType | <code>String</code> | Which type of error we are in |

**Example**  
```js
appendErrorElement(theError, '400 Bad Request')
```
<a name="goToRoute"></a>

## goToRoute(path, force, event)
Perform a routing to the path

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| path | <code>String</code> |  | where to perform routing |
| force | <code>Boolean</code> | <code>false</code> |  |
| event | <code>Event</code> |  | object |

<a name="renderRoute"></a>

## renderRoute(targetRoute)
Display the appropriate component for the target route

**Kind**: global function  

| Param | Type |
| --- | --- |
| targetRoute | <code>String</code> | 


 

 

