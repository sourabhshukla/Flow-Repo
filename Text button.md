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
<pre><code>{
  "id": "1763564100751",
  "type": "masterComponent",
  "data": {
    "isDrag": true,
    "id": "1763564100751",
    "content": [
      {
        "id": "1763564100751-message",
        "type": "message",
        "data": {
          "text": "this is demo message",
          "buttons": [
            {
              "text": "button text",
              "id": 1763564160176
            }
          ],
          "delay": "12",
          "timeoutToggle": true,
          "time": "12"
        }
      }
    ]
  },
  "position": {
    "x": -334.3917236328125,
    "y": -86.28158569335938
  }
}
</code></pre>

