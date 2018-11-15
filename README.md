# vGen
We want to develop a language for VideoGen, a system that will generate, from textual specifications, a video generator on the Web.
## Classes

<dl>
<dt><a href="#router.js">router.js</a></dt>
<dd></dd>
</dl>

## Functions

<dl>
<dt><a href="#goToRoute">goToRoute(path, force, event)</a></dt>
<dd><p>Perform a routing to the path</p>
</dd>
<dt><a href="#renderRoute">renderRoute(targetRoute)</a></dt>
<dd><p>Display the appropriate component for the target route</p>
</dd>
</dl>

## External

<dl>
<dt><a href="#external_views/index">views/index</a> ⇐ <code><a href="#external_views/layout">views/layout</a></code></dt>
<dd><p>The homepage view. Uses the <a href="#external_config">config</a> widget to render each news article.</p>
</dd>
<dt><a href="#external_config">config</a></dt>
<dd><p>The news widget.</p>
</dd>
<dt><a href="#external_views/layout">views/layout</a></dt>
<dd><p>The base layout from which all other views inherit from.</p>
</dd>
</dl>

<a name="router.js"></a>

## router.js
**Kind**: global class  
<a name="new_router.js_new"></a>

### new router.js()
NovatioRouter is responsible for routing to the appropriate module. Module's routes are described in a json file see [config](#external_config).

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

<a name="external_views/index"></a>

## views/index ⇐ [<code>views/layout</code>](#external_views/layout)
The homepage view. Uses the [config](#external_config) widget to render each news article.

**Kind**: global external  
**Extends**: [<code>views/layout</code>](#external_views/layout)  
<a name="external_config"></a>

## config
The news widget.

**Kind**: global external  
<a name="external_views/layout"></a>

## views/layout
The base layout from which all other views inherit from.

**Kind**: global external  
  
  
  
  
  
  
  
  
  
 


 

 

