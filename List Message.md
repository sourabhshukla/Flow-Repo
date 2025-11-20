---


---

<h1 id="list-message-node-listmessage">List Message Node (<code>listMessage</code>)</h1>
<p>This node represents a <strong>WhatsApp-style list message</strong> with:</p>
<ul>
<li>Header, body, footer</li>
<li>One button to open the list</li>
<li>Multiple sections</li>
<li>Multiple items inside each section</li>
</ul>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763570491212",

  // Node type - still a masterComponent
  "type": "masterComponent",

  // Node configuration and content
  "data": {
    // Whether this node is draggable in the editor
    "isDrag": true,

    // Logical ID for the component (usually same as node id)
    "id": "1763570491212",

    // Content blocks inside this node
    "content": [
      {
        // Unique ID for this specific list message block
        "id": "1763570491212-listMessage",

        // Content type for list messages
        "type": "listMessage",

        "data": {
          // Header text shown on top of the list message (optional by channel)
          "header": "Header",

          // Main body text of the list message
          "body": "Body",

          // Footer text shown at the bottom (optional)
          "footer": "Footer",

          // Total number of items across all sections
          // Should equal sum(sections[*].items.length)
          "itemsCount": 3,

          // Total number of sections
          // Should equal sections.length
          "sectionsCount": 2,

          // Array of sections in the list
          "sections": [
            {
              // Section title shown in the UI
              "title": "section 1",

              // Items belonging to this section
              "items": [
                {
                  // Item title shown to the user
                  "title": "item title 1",

                  // Optional item description
                  "description": "desc 1",

                  // Unique identifier for this item
                  // Used to map user selection back to a specific item
                  // FORMAT: list_message-right-&lt;node-id&gt;-&lt;section index&gt;-&lt;item id&gt;-|&lt;Flow Id&gt;
                  "id": "list_message-right-1763570491212-0-1763570628085-|68fbd6e8421ba34a53f2d712"
                },
                {
                  "title": "item title 2",
                  "description": "desc 2",
                   // FORMAT: list_message-right-&lt;node-id&gt;-&lt;section index&gt;-&lt;item id&gt;-|&lt;Flow Id&gt;
                  "id": "list_message-right-1763570491212-0-1763570686479-|68fbd6e8421ba34a53f2d712"
                }
              ],

              // Unique ID for this section
              "id": "list_message-right-1763570491212-0"
            },
            {
              "title": "section 2",
              "items": [
                {
                  "title": "item title 3",
                  "description": "item desc 3",
                   // FORMAT: list_message-right-&lt;node-id&gt;-&lt;section index&gt;-&lt;item id&gt;-|&lt;Flow Id&gt;
                  "id": "list_message-right-1763570491212-1-1763570704595-|68fbd6e8421ba34a53f2d712"
                }
              ],
              "id": "list_message-right-1763570491212-1"
            }
          ],

          // Label of the main button that opens the list
          "buttonTitle": "List button lable",

          // Delay before sending/showing this list message
          // UNIT: SECONDS
          "delay": "12",

          // When true, use `time` to auto-continue after a timeout
          "timeoutToggle": true,

          // Timeout duration
          // UNIT: MINUTES
          "time": "33"
        }
      }
    ]
  },

  // Canvas position of this node
  "position": {
    "x": -1210.975723058688,
    "y": -705.7794098763814
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763570491212"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763570491212"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763570491212-listMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"listMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"header"</span><span class="token punctuation">:</span> <span class="token string">"Header"</span><span class="token punctuation">,</span>
          <span class="token string">"body"</span><span class="token punctuation">:</span> <span class="token string">"Body"</span><span class="token punctuation">,</span>
          <span class="token string">"footer"</span><span class="token punctuation">:</span> <span class="token string">"Footer"</span><span class="token punctuation">,</span>
          <span class="token string">"itemsCount"</span><span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span>
          <span class="token string">"sectionsCount"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
          <span class="token string">"sections"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"section 1"</span><span class="token punctuation">,</span>
              <span class="token string">"items"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token punctuation">{</span>
                  <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"item title 1"</span><span class="token punctuation">,</span>
                  <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"desc 1"</span><span class="token punctuation">,</span>
                  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"list_message-right-1763570491212-0-1763570628085-|68fbd6e8421ba34a53f2d712"</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token punctuation">{</span>
                  <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"item title 2"</span><span class="token punctuation">,</span>
                  <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"desc 2"</span><span class="token punctuation">,</span>
                  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"list_message-right-1763570491212-0-1763570686479-|68fbd6e8421ba34a53f2d712"</span>
                <span class="token punctuation">}</span>
              <span class="token punctuation">]</span><span class="token punctuation">,</span>
              <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"list_message-right-1763570491212-0"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>
              <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"section 2"</span><span class="token punctuation">,</span>
              <span class="token string">"items"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token punctuation">{</span>
                  <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"item title 3"</span><span class="token punctuation">,</span>
                  <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"item desc 3"</span><span class="token punctuation">,</span>
                  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"list_message-right-1763570491212-1-1763570704595-|68fbd6e8421ba34a53f2d712"</span>
                <span class="token punctuation">}</span>
              <span class="token punctuation">]</span><span class="token punctuation">,</span>
              <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"list_message-right-1763570491212-1"</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"buttonTitle"</span><span class="token punctuation">:</span> <span class="token string">"List button lable"</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"12"</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"33"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1210.975723058688</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">705.7794098763814</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

