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
              "_id": "635ce7278c62b361bf05f179",

              // Messages that can act as first-message triggers (currently empty)
              "firstMessages": [],

              // Tag name used in UI and logic
              "tagName": "zoom_booked",

              // Display colors for UI (main + light variant)
              "displayColor": {
                "main": "#0b908b",
                "light": "#bceceb"
              },

              // Category/group this tag belongs to
              "category": "zoom",

              // Whether this tag is treated as a “first message” event
              "isFirstMessage": false,

              // Whether this tag is a journey event (used in analytics/timelines)
              "isJourneyEvent": true,

              // Assistant / bot this tag belongs to
              "assistantId": "633829cd86fc494a463d86e8",

              // Client / account this tag belongs to
              "clientId": "63029c7285871851a4932f58",

              // Audit fields
              "createdAt": "2022-10-29T08:41:11.891Z",
              "updatedAt": "2022-10-29T08:41:11.891Z",
              "__v": 0
            },
            {
              "_id": "6363bf2c7f43ed2765910ba6",
              "firstMessages": [],
              "tagName": "request callback demo",
              "displayColor": {
                "main": "#0e9e06",
                "light": "#cdeccb"
              },
              "category": "callback demo link",
              "isFirstMessage": false,
              "isJourneyEvent": true,
              "assistantId": "633829cd86fc494a463d86e8",
              "clientId": "63029c7285871851a4932f58",
              "createdAt": "2022-11-03T13:16:28.079Z",
              "updatedAt": "2022-11-03T13:16:28.079Z",
              "__v": 0
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
              <span class="token string">"_id"</span><span class="token punctuation">:</span> <span class="token string">"635ce7278c62b361bf05f179"</span><span class="token punctuation">,</span>
              <span class="token string">"firstMessages"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
              <span class="token string">"tagName"</span><span class="token punctuation">:</span> <span class="token string">"zoom_booked"</span><span class="token punctuation">,</span>
              <span class="token string">"displayColor"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                <span class="token string">"main"</span><span class="token punctuation">:</span> <span class="token string">"#0b908b"</span><span class="token punctuation">,</span>
                <span class="token string">"light"</span><span class="token punctuation">:</span> <span class="token string">"#bceceb"</span>
              <span class="token punctuation">}</span><span class="token punctuation">,</span>
              <span class="token string">"category"</span><span class="token punctuation">:</span> <span class="token string">"zoom"</span><span class="token punctuation">,</span>
              <span class="token string">"isFirstMessage"</span><span class="token punctuation">:</span> <span class="token boolean">false</span><span class="token punctuation">,</span>
              <span class="token string">"isJourneyEvent"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
              <span class="token string">"assistantId"</span><span class="token punctuation">:</span> <span class="token string">"633829cd86fc494a463d86e8"</span><span class="token punctuation">,</span>
              <span class="token string">"clientId"</span><span class="token punctuation">:</span> <span class="token string">"63029c7285871851a4932f58"</span><span class="token punctuation">,</span>
              <span class="token string">"createdAt"</span><span class="token punctuation">:</span> <span class="token string">"2022-10-29T08:41:11.891Z"</span><span class="token punctuation">,</span>
              <span class="token string">"updatedAt"</span><span class="token punctuation">:</span> <span class="token string">"2022-10-29T08:41:11.891Z"</span><span class="token punctuation">,</span>
              <span class="token string">"__v"</span><span class="token punctuation">:</span> <span class="token number">0</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>
              <span class="token string">"_id"</span><span class="token punctuation">:</span> <span class="token string">"6363bf2c7f43ed2765910ba6"</span><span class="token punctuation">,</span>
              <span class="token string">"firstMessages"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
              <span class="token string">"tagName"</span><span class="token punctuation">:</span> <span class="token string">"request callback demo"</span><span class="token punctuation">,</span>
              <span class="token string">"displayColor"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                <span class="token string">"main"</span><span class="token punctuation">:</span> <span class="token string">"#0e9e06"</span><span class="token punctuation">,</span>
                <span class="token string">"light"</span><span class="token punctuation">:</span> <span class="token string">"#cdeccb"</span>
              <span class="token punctuation">}</span><span class="token punctuation">,</span>
              <span class="token string">"category"</span><span class="token punctuation">:</span> <span class="token string">"callback demo link"</span><span class="token punctuation">,</span>
              <span class="token string">"isFirstMessage"</span><span class="token punctuation">:</span> <span class="token boolean">false</span><span class="token punctuation">,</span>
              <span class="token string">"isJourneyEvent"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
              <span class="token string">"assistantId"</span><span class="token punctuation">:</span> <span class="token string">"633829cd86fc494a463d86e8"</span><span class="token punctuation">,</span>
              <span class="token string">"clientId"</span><span class="token punctuation">:</span> <span class="token string">"63029c7285871851a4932f58"</span><span class="token punctuation">,</span>
              <span class="token string">"createdAt"</span><span class="token punctuation">:</span> <span class="token string">"2022-11-03T13:16:28.079Z"</span><span class="token punctuation">,</span>
              <span class="token string">"updatedAt"</span><span class="token punctuation">:</span> <span class="token string">"2022-11-03T13:16:28.079Z"</span><span class="token punctuation">,</span>
              <span class="token string">"__v"</span><span class="token punctuation">:</span> <span class="token number">0</span>
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

