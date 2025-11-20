---


---

<h1 id="set-attribute-node-setavariable">Set Attribute Node (<code>setAVariable</code>)</h1>
<p>This node is used to <strong>set/update an attribute value</strong> without asking the user a question.</p>
<p>Common use cases:</p>
<ul>
<li>Storing static values (e.g., default URLs, flags).</li>
<li>Overwriting attributes based on flow logic.</li>
<li>Pre-populating data for later conditions or API calls.</li>
</ul>
<hr>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763579079482",

  // Node type wrapper
  "type": "masterComponent",

  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Logical ID of the component (usually same as node id)
    "id": "1763579079482",

    // Content blocks inside this node
    "content": [
      {
        // Unique ID for this set-attribute block
        "id": "1763579079482-setAVariable",

        // Node type for setting an attribute
        "type": "setAVariable",

        "data": {
          // The value that will be assigned to the attribute.
          // Can be a static string or, depending on engine support,
          // a dynamic expression / variable reference.
          "value": "https://google.com",

          // The attribute key that will be set/updated.
          // Example: "EmbededURL", "Country", "LeadStatus"
          "attribute": "EmbededURL"
        }
      }
    ]
  },

  // Canvas position of this node
  "position": {
    "x": -906.596198589626,
    "y": -317.0161228142084
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579079482"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579079482"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579079482-setAVariable"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"setAVariable"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"value"</span><span class="token punctuation">:</span> <span class="token string">"https://google.com"</span><span class="token punctuation">,</span>
          <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"EmbededURL"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">906.596198589626</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">317.0161228142084</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

