---


---

<h1 id="catalogue-message-node-cataloguemessage">Catalogue Message Node (<code>catalogueMessage</code>)</h1>
<p>This node is used to send a <strong>generic catalogue message</strong> for Meta (WhatsApp) catalogs.</p>
<p>Instead of selecting specific products in the flow, this message typically lets the user <strong>open the linked catalog itself</strong> and browse products there.</p>
<p>It supports:</p>
<ul>
<li><code>body</code>: Main message text</li>
<li><code>footer</code>: Optional footer text</li>
</ul>
<hr>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763580464194",

  // Wrapper node type
  "type": "masterComponent",

  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Logical ID of this component (usually same as node id)
    "id": "1763580464194",

    // Content blocks inside this node
    "content": [
      {
        // Unique ID for this catalogue message block
        "id": "1763580464194-catalogueMessage",

        // Node type for generic catalogue messages
        "type": "catalogueMessage",

        "data": {
          // Main body text shown with the catalogue entry
          "body": "Body",

          // Optional footer text shown below the catalogue message
          "footer": "Footer"
        }
      }
    ]
  },

  // Position of this node on the canvas
  "position": {
    "x": 282.1923974437441,
    "y": 82.85386424741533
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763580464194"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763580464194"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763580464194-catalogueMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"catalogueMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"body"</span><span class="token punctuation">:</span> <span class="token string">"Body"</span><span class="token punctuation">,</span>
          <span class="token string">"footer"</span><span class="token punctuation">:</span> <span class="token string">"Footer"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token number">282.1923974437441</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token number">82.85386424741533</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

