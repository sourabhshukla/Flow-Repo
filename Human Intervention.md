---


---

<h1 id="human-intervention-node-humanintervention">Human Intervention Node (<code>humanIntervention</code>)</h1>
<p>This node is used to <strong>request human/agent intervention</strong> in the conversation.<br>
When this node is executed, the system can pause bot automation and notify a human agent (depending on your backend logic).</p>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763573321790",

  // Node type - still a masterComponent
  "type": "masterComponent",

  // Node configuration and content
  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Logical ID of the component (usually same as node id)
    "id": "1763573321790",

    // Content blocks inside this node
    "content": [
      {
        // Unique ID for this human intervention block
        "id": "1763573321790-humanIntervention",

        // Content type for requesting human intervention
        "type": "humanIntervention",

        "data": {
         
          "isRequesting": true
        }
      }
    ]
  },

  // Position of this node on the editor canvas
  "position": {
    "x": -925.725341796875,
    "y": -297.05743408203125
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763573321790"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763573321790"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763573321790-humanIntervention"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"humanIntervention"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"isRequesting"</span><span class="token punctuation">:</span> <span class="token boolean">true</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">925.725341796875</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">297.05743408203125</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

