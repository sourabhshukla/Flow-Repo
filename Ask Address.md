---


---

<h1 id="ask-address-node-questionaddressmessage">Ask Address Node (<code>questionAddressMessage</code>)</h1>
<p>This node is used to <strong>ask the user for an address</strong> (e.g., country, city, full address) and store the response into attributes.</p>
<p>It supports:</p>
<ul>
<li>A question text</li>
<li>A raw attribute to store the user’s answer</li>
<li>A formatted/processed attribute</li>
<li>Timeout behavior in minutes</li>
</ul>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763576431960",

  // Node type - still a masterComponent
  "type": "masterComponent",

  // Node configuration and content
  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Logical ID of the component (usually same as node id)
    "id": "1763576431960",

    // Content blocks inside this node
    "content": [
      {
        // Unique ID for this ask-address block
        "id": "1763576431960-questionAddressMessage",

        // Content type for address question nodes
        "type": "questionAddressMessage",

        "data": {
          // Question text shown to the user
          "text": "Where is your address",

          // Attribute key where the raw user response will be stored
          // e.g. "Country", "FullAddress"
          "attribute": "Country",

          // Attribute key where a formatted / normalized version
          // of the address can be stored (e.g., standardized country code)
          "formattedAttribute": "IndustryType",

          // When true, use `time` to apply a timeout
          "timeoutToggle": true,

          // Timeout duration
          // UNIT: MINUTES (consistent with other nodes)
          "time": "100"
        }
      }
    ]
  },

  // Position of this node on the editor canvas
  "position": {
    "x": -951.5830539364624,
    "y": -320.0834084060382
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576431960"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576431960"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576431960-questionAddressMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"questionAddressMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"Where is your address"</span><span class="token punctuation">,</span>
          <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"Country"</span><span class="token punctuation">,</span>
          <span class="token string">"formattedAttribute"</span><span class="token punctuation">:</span> <span class="token string">"IndustryType"</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"100"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">951.5830539364624</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">320.0834084060382</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

