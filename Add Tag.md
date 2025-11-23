---


---

<h1 id="add-tag-node-addtag">Add Tag Node (<code>addTag</code>)</h1>
<p>This node is used to <strong>attach one or more tags</strong> to the current contact/conversation.</p>
<p>Typical use cases:</p>
<ul>
<li>Marking important events in the journey (e.g. <code>zoom_booked</code>)</li>
<li>Segmenting users (e.g. <code>request callback demo</code>)</li>
<li>Triggering analytics or downstream workflows based on tags</li>
</ul>
<hr>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763579182272",

  // Node type wrapper
  "type": "masterComponent",

  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Logical ID of the component (usually same as node id)
    "id": "1763579182272",

    // Content blocks inside this node
    "content": [
      {
        // Unique ID for this add-tag block
        "id": "1763579182272-addTag",

        // Node type for adding tags
        "type": "addTag",

        "data": {
          // Array of tag objects to be applied.
          // Typically these are pre-configured tags from your system.
          "tags": [
            {
              // Internal DB ID of the tag
              "_id": "635ce7278c62b361bf05f179"
            },
            {
              "_id": "6363bf2c7f43ed2765910ba6"
            }
          ]
        }
      }
    ]
  },

  // Position of this node on the canvas
  "position": {
    "x": -1025.197908140377,
    "y": -247.49098273273367
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579182272"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579182272"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579182272-addTag"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"addTag"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"tags"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"_id"</span><span class="token punctuation">:</span> <span class="token string">"635ce7278c62b361bf05f179"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>
              <span class="token string">"_id"</span><span class="token punctuation">:</span> <span class="token string">"6363bf2c7f43ed2765910ba6"</span><span class="token punctuation">,</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1025.197908140377</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">247.49098273273367</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

