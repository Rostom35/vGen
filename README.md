## Classes

<dl>
<dt><a href="#components/app.js">components/app.js</a></dt>
<dd></dd>
<dt><a href="#components/error.js">components/error.js</a></dt>
<dd></dd>
<dt><a href="#components/header.js">components/header.js</a></dt>
<dd></dd>
<dt><a href="#components/home.js">components/home.js</a></dt>
<dd></dd>
<dt><a href="#components/loader.js">components/loader.js</a></dt>
<dd></dd>
<dt><a href="#components/navbar.js">components/navbar.js</a></dt>
<dd></dd>
<dt><a href="#components/page.js">components/page.js</a></dt>
<dd></dd>
<dt><a href="#components/router.js">components/router.js</a></dt>
<dd></dd>
</dl>

## Functions

<dl>
<dt><a href="#customMessage">customMessage(info)</a> ⇒ <code>String</code></dt>
<dd><p>This method constructs a message that will be used to notify the user</p>
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

## External

<dl>
<dt><a href="#external_config">config</a></dt>
<dd><p>The config must respect the following JSON Schema :<br/>&quot;!&quot; means that the key is required while &quot;?&quot; means that it&#39;s optional</p>
<pre><code class="language-javascripton">   {
      &quot;assets&quot;: {
          &quot;url!&quot;: &quot;string&quot;,
          &quot;icons!&quot;: &quot;string&quot;,
          &quot;logo!&quot;: &quot;string&quot;,
          &quot;webcomponents!&quot;: &quot;string&quot;,
          &quot;style!&quot;: &quot;string&quot;
      },
      &quot;routes&quot;: [{
          &quot;path!&quot;: &quot;string&quot;,
          &quot;exact?&quot;: boolean,
          &quot;public?&quot;: boolean,
          &quot;component?&quot;: &quot;string&quot;,
          &quot;icon?&quot;: &quot;string&quot;,
          &quot;action?&quot;: &quot;string&quot;,
          &quot;title?&quot;: &quot;string&quot;,
          &quot;module?&quot;: {
              &quot;id!&quot;: &quot;string&quot;,
              &quot;url!&quot;: &quot;string&quot;,
              &quot;scripts!&quot;: [&quot;string&quot;]
          },
          &quot;links?&quot;: [{ &quot;path&quot;: &quot;string&quot;, &quot;title&quot;: &quot;string&quot; }]
      }]
   }
</code></pre>
<ul>
<li>Use &quot;exact&quot; (by default its value is false) to perform a routing to the exact url not on an url which start whith &quot;url&quot;. It also means that you have to respect a * potential order.</li>
<li>&quot;public&quot; (by default its value is false) means that the route is accessible by all</li>
<li>&quot;component&quot; is used to specify which container&#39;s component to load</li>
<li>&quot;action&quot; we execute an action when we are redirect to a specific route</li>
</ul>
</dd>
</dl>

<a name="components/app.js"></a>

## components/app.js
**Kind**: global class  
<a name="new_components/app.js_new"></a>

### new components/app.js()
NovatioApp the app(root) element

<a name="components/error.js"></a>

## components/error.js
**Kind**: global class  
<a name="new_components/error.js_new"></a>

### new components/error.js()
NovatioError the error element which is used to render a message to the user

<a name="components/header.js"></a>

## components/header.js
**Kind**: global class  
<a name="new_components/header.js_new"></a>

### new components/header.js()
NovatioHeader the header element

<a name="components/home.js"></a>

## components/home.js
**Kind**: global class  
<a name="new_components/home.js_new"></a>

### new components/home.js()
NovatioHome the home element

<a name="components/loader.js"></a>

## components/loader.js
**Kind**: global class  
<a name="new_components/loader.js_new"></a>

### new components/loader.js()
NovatioLoader the spinner element

<a name="components/navbar.js"></a>

## components/navbar.js
**Kind**: global class  
<a name="new_components/navbar.js_new"></a>

### new components/navbar.js()
NovatioNavbar the navbar element

<a name="components/page.js"></a>

## components/page.js
**Kind**: global class  
**See**: <a href="https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_custom_elements">HTMLElement</a>  
<a name="new_components/page.js_new"></a>

### new components/page.js()
NovationPage an HTMLElement which is respensible for loading component from <b>modules</b> to the container.<br/>
             Modules are described in a json file see [config](#external_config) to get more informations on the config file.

<a name="components/router.js"></a>

## components/router.js
**Kind**: global class  
<a name="new_components/router.js_new"></a>

### new components/router.js()
NovatioRouter is responsible for routing to the appropriate module. Module's routes are described in a json file see [config](#external_config).

<a name="customMessage"></a>

## customMessage(info) ⇒ <code>String</code>
This method constructs a message that will be used to notify the user

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

<a name="external_config"></a>

## config
The config must respect the following JSON Schema :<br/>"!" means that the key is required while "?" means that it's optional
```json
   {
      "assets": {
          "url!": "string",
          "icons!": "string",
          "logo!": "string",
          "webcomponents!": "string",
          "style!": "string"
      },
      "routes": [{
          "path!": "string",
          "exact?": boolean,
          "public?": boolean,
          "component?": "string",
          "icon?": "string",
          "action?": "string",
          "title?": "string",
          "module?": {
              "id!": "string",
              "url!": "string",
              "scripts!": ["string"]
          },
          "links?": [{ "path": "string", "title": "string" }]
      }]
   }
```
- Use "exact" (by default its value is false) to perform a routing to the exact url not on an url which start whith "url". It also means that you have to respect a * potential order.
- "public" (by default its value is false) means that the route is accessible by all
- "component" is used to specify which container's component to load
- "action" we execute an action when we are redirect to a specific route

**Kind**: global external  
**Example**  
```js
{.."routes": [
      {"path": "/tot/",
      "exact": false},
      {"path": "/toto/"...}
   ]}
Here we are not going to be able to route at "/toto/" because "/toto/" start with "/tot/" which is defined before "/toto/"
```
