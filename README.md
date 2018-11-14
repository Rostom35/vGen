# vGen
We want to develop a language for VideoGen, a system that will generate, from textual specifications, a video generator on the Web.
## Classes

<dl>
<dt><a href="#page.js">page.js</a></dt>
<dd></dd>
</dl>

## Functions

<dl>
<dt><a href="#createElementFromSelectorOrID">createElementFromSelectorOrID(module)</a></dt>
<dd><p>An element is either identified
by its id or selector</p>
</dd>
<dt><a href="#resolveScriptsLocation">resolveScriptsLocation(url, module)</a></dt>
<dd></dd>
<dt><a href="#appendErrorElement">appendErrorElement(error, errorType)</a></dt>
<dd><p>Construct error element and passes error information to the custom element</p>
</dd>
<dt><a href="#goToRoute">goToRoute(path, force, event)</a></dt>
<dd><p>Perform a routing to a path</p>
</dd>
<dt><a href="#renderRoute">renderRoute(targetRoute)</a></dt>
<dd><p>Display the appropriate component for the target route</p>
</dd>
</dl>

<a name="page.js"></a>

## page.js
**Kind**: global class  
<a name="new_page.js_new"></a>

### new page.js()
NovationPage is respensible for loading component from module to the container

<a name="createElementFromSelectorOrID"></a>

## createElementFromSelectorOrID(module)
An element is either identified
by its id or selector

**Kind**: global function  
**Throws**:

- <code>Error</code> an exception could be thrown during execution if a module definition don't have tag or id key


| Param | Type | Description |
| --- | --- | --- |
| module | <code>Route</code> | {@see config.json[routes]} |

<a name="resolveScriptsLocation"></a>

## resolveScriptsLocation(url, module)
**Kind**: global function  

| Param |
| --- |
| url | 
| module | 

<a name="appendErrorElement"></a>

## appendErrorElement(error, errorType)
Construct error element and passes error information to the custom element

**Kind**: global function  

| Param | Type |
| --- | --- |
| error | <code>Error</code> | 
| errorType | <code>String</code> | 

<a name="goToRoute"></a>

## goToRoute(path, force, event)
Perform a routing to a path

**Kind**: global function  

| Param | Type | Default |
| --- | --- | --- |
| path | <code>String</code> |  | 
| force | <code>Boolean</code> | <code>false</code> | 
| event | <code>Event</code> |  | 

<a name="renderRoute"></a>

## renderRoute(targetRoute)
Display the appropriate component for the target route

**Kind**: global function  

| Param |
| --- |
| targetRoute | 

 

