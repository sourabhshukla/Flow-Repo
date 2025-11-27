---


---

<h1 id="text-button-node">Text Button Node</h1>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier (timestamp) for the node on the canvas
  "id": "1763564100751",

  // Node type - "masterComponent" nodes represent reusable message blocks
  "type": "masterComponent",

  // All configuration &amp; content for this node
  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Same as node id above
    "id": "1763564100751",

    // Array of content blocks inside this master component
    "content": [
      {
        // Unique ID for this specific content block
        "id": "1763564100751-message",

        // Content type. For now we support "message"
        "type": "message",

        // Payload for the message shown to the end user
        "data": {
          // Text that will be sent/rendered as the message bubble
          "text": "This is demo message",

          // Optional array of buttons rendered below the message
          // - 0 buttons allowed (no array or empty array)
          // - Max 3 buttons allowed
          "buttons": [
            {
              // Label shown on the button
              "text": "button text",

              // Unique identifier for this button (for click handling/analytics)
              "id": 1763564160176
            }
          ],

          // Optional delay before this message is sent/shown (in seconds)
          // "" =&gt; use default behavior / no explicit delay
          "delay": "12",

          // When true, a timeout will be applied using the "time" field
          // When false, message waits for user action or next explicit trigger
          "timeoutToggle": true,

          // Duration used when timeoutToggle is true (in minutes)
          "time": "12"
        }
      }
    ]
  },

  // Position of this node on the editor canvas (in pixels)
  "position": {
    // Horizontal coordinate
    "x": -334.3917236328125,

    // Vertical coordinate
    "y": -86.28158569335938
  }
}

</code></pre>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763564100751"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763564100751"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763564100751-message"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"message"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"this is demo message"</span><span class="token punctuation">,</span>
          <span class="token string">"buttons"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"button text"</span><span class="token punctuation">,</span>
              <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1763564160176</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"12"</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"12"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">334.3917236328125</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">86.28158569335938</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

