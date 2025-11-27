---


---

<h1 id="connect-flows-node-connectflows">Connect Flows Node (<code>connectFlows</code>)</h1>
<p>This node is used to <strong>redirect the user from the current flow into another flow</strong>.</p>
<p>When executed, the engine should stop the current flow and start the target flow identified by <code>flowId</code>.</p>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763576059055",

  // Node type - still a masterComponent
  "type": "masterComponent",

  // Node configuration and content
  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Logical ID of the component (usually same as node id)
    "id": "1763576059055",

    // Content blocks inside this master component
    "content": [
      {
        // Unique ID for this connectFlows block
        "id": "1763576059055-connectFlows",

        // Content type for flow-connection logic
        "type": "connectFlows",

        "data": {
          // ID of the target flow to connect to
          "flowId": "68fbd6e8421ba34a53f2d712",

          // Human-readable name of the target flow.
          // Used only for UI display, logs, and debugging.
          "flowName": "Untitled"
        }
      }
    ]
  },

  // Position of this node on the editor canvas
  "position": {
    "x": -903.5289129977962,
    "y": -269.98441040615205
  }
}
</code></pre>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576059055"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576059055"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576059055-connectFlows"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"connectFlows"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"flowId"</span><span class="token punctuation">:</span> <span class="token string">"68fbd6e8421ba34a53f2d712"</span><span class="token punctuation">,</span>
          <span class="token string">"flowName"</span><span class="token punctuation">:</span> <span class="token string">"Untitled"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">903.5289129977962</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">269.98441040615205</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

