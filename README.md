# vGen
We want to develop a language for VideoGen, a system that will generate, from textual specifications, a video generator on the Web.
## Classes

<dl>
<dt><a href="#page.js">page.js</a></dt>
<dd></dd>
</dl>

## Functions

<dl>
<dt><a href="#createElementFromSelectorOrID">createElementFromSelectorOrID(module)</a> ⇒ <code>Element</code></dt>
<dd><p>An element is either identified
by its id or selector</p>
</dd>
<dt><a href="#resolveScriptsLocation">resolveScriptsLocation(url, module)</a> ⇒ <code>String</code></dt>
<dd></dd>
<dt><a href="#appendErrorElement">appendErrorElement(error, errorType)</a></dt>
<dd><p>Construct error element and passes error information to the custom element</p>
</dd>
</dl>

## External

<dl>
<dt><a href="#external_views/index">views/index</a> ⇐ <code><a href="#external_views/layout">views/layout</a></code></dt>
<dd><p>The homepage view. Uses the <a href="#external_views/news">views/news</a> widget to render each news article.</p>
</dd>
<dt><a href="#external_views/news">views/news</a></dt>
<dd><p>The news widget.</p>
</dd>
<dt><a href="#external_views/layout">views/layout</a></dt>
<dd><p>The base layout from which all other views inherit from.</p>
</dd>
</dl>

<a name="page.js"></a>

## page.js
**Kind**: global class  
**See**: <a href="https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_custom_elements">HTMLElement</a>  
<a name="new_page.js_new"></a>

### new page.js()
NovationPage an HTMLElement which is respensible for loading component from <b>modules</b> to the container.

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
<a name="external_views/index"></a>

## views/index ⇐ [<code>views/layout</code>](#external_views/layout)
The homepage view. Uses the [views/news](#external_views/news) widget to render each news article.

**Kind**: global external  
**Extends**: [<code>views/layout</code>](#external_views/layout)  
<a name="external_views/news"></a>

## views/news
The news widget.

**Kind**: global external  
<a name="external_views/layout"></a>

## views/layout
The base layout from which all other views inherit from.

**Kind**: global external  
  
  
  
  
  
 


 

 

