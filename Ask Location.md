---


---

<h1 id="ask-location-node-questionlocationmessage">Ask Location Node (<code>questionLocationMessage</code>)</h1>
<p>This node is used to <strong>ask the user for their location</strong> (typically via WhatsApp’s location picker) and store the coordinates into attributes.</p>
<p>It supports:</p>
<ul>
<li>A question text</li>
<li>Attributes to store latitude and longitude</li>
<li>Timeout behavior in minutes</li>
</ul>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763576723785",

  // Node type - still a masterComponent
  "type": "masterComponent",

  // Node configuration and content
  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Logical ID of the component (usually same as node id)
    "id": "1763576723785",

    // Content blocks inside this node
    "content": [
      {
        // Unique ID for this ask-location block
        "id": "1763576723785-questionLocationMessage",

        // Content type for location question nodes
        "type": "questionLocationMessage",

        "data": {
          // Question text shown to the user
          "text": "Where is you location",

          // NOTE: appears unused / legacy; kept for backward compatibility.
          // Can remain empty string.
          "longituteAttribute": "",

          // Attribute key where LATITUDE will be stored
          // e.g. "UserLatitude"
          "latitudeAttribute": "latitude",

          // Attribute key where LONGITUDE will be stored
          // e.g. "UserLongitude"
          "longitudeAttribute": "longitude",

          // When true, use `time` to apply a timeout
          "timeoutToggle": true,

          // Timeout duration
          // UNIT: MINUTES (same convention as other question nodes)
          "time": "34"
        }
      }
    ]
  },

  // Position of this node on the editor canvas
  "position": {
    "x": -973.0540530792708,
    "y": -399.83283379361217
  }
}
</code></pre>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576723785"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576723785"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576723785-questionLocationMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"questionLocationMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"Where is you location"</span><span class="token punctuation">,</span>
          <span class="token string">"longituteAttribute"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"latitudeAttribute"</span><span class="token punctuation">:</span> <span class="token string">"latitude"</span><span class="token punctuation">,</span>
          <span class="token string">"longitudeAttribute"</span><span class="token punctuation">:</span> <span class="token string">"longitude"</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"34"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">973.0540530792708</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">399.83283379361217</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

