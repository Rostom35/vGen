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
</ul>
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

**Kind**: global external  
**Example**  
```js
{.."routes": [
      {"path": "/tot/",
      "exact": false},
      {"path": "/toto/"...}
   ]}
Here we are not going to be able to route at "/toto/" because "/toto/" start with "/tot/" which is defined before "/toto/"
- "public" (by default its value is false) means that the route is accessible by all
```
<a name="external_views/layout"></a>

## views/layout
The base layout from which all other views inherit from.

**Kind**: global external  
