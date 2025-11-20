---


---

<h1 id="whatsapp-forms-node-whatsappforms">WhatsApp Forms Node (<code>whatsappForms</code>)</h1>
<p>This node is used to trigger a <strong>WhatsApp Flow / Form</strong> from a message step.</p>
<p>It includes:</p>
<ul>
<li>Header, body, footer text</li>
<li>Flow metadata (ID, token, status, action)</li>
<li>Button label</li>
<li>Optional attribute mapping + validation error message</li>
<li>Delay (in seconds) and timeout (in minutes)</li>
</ul>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763571975275",

  // Node type - still a masterComponent
  "type": "masterComponent",

  // Node configuration and content
  "data": {
    // Whether this node is draggable in the editor
    "isDrag": true,

    // Logical ID for the component (usually same as node id)
    "id": "1763571975275",

    // Content blocks inside this node
    "content": [
      {
        // Unique ID for this specific WhatsApp Forms block
        "id": "1763571975275-whatsappForms",

        // Content type for WhatsApp Flows / Forms
        "type": "whatsappForms",

        "data": {
          // Header text shown above the body (optional by channel)
          "header": "header",

          // Main body text of the form message
          "body": "body",

          // Footer text shown below the body (optional)
          "footer": "footer",

          // Identifier of the WhatsApp Flow in Meta / WABA
          "flowId": "&lt;Flow Id&gt;",

          // Screen name to be opened or used inside the flow
          "screenName": "Screen name",

          // Optional attribute name where the flow result / data is stored
          // e.g., "lead_form_response", can be blank if not mapped
          "attributeName": "",

          // Status of the flow definition
          // Allowed values: "Draft" | "Published"
          "flowStatus": "Draft",

          // Action type that this flow performs
          // Allowed values:
          // - "data_exchange": flow exchanges data with your system
          // - "navigate": flow is used for navigation / UI only
          "flowAction": "data_exchange",

          // Label shown on the button that launches the flow
          "buttonTitle": "sdfas",

          // Token associated with this flow for authentication/authorization
          "flowToken": "&lt;Flow Token&gt;",

          // When true, use `time` to auto-continue after a timeout
          "timeoutToggle": true,

          // Error message to show when attribute format validation fails
          "attributeFormatValidationErrorMessage": "validation error message",

          // Delay before sending/showing this WhatsApp Forms message
          // UNIT: SECONDS
          "delay": "100",

          // Timeout duration when timeoutToggle is true
          // UNIT: MINUTES
          "time": "200"
        }
      }
    ]
  },

  // Canvas position of this node
  "position": {
    "x": -874.3611353145966,
    "y": -437.1157457509522
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763571975275"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763571975275"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763571975275-whatsappForms"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"whatsappForms"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"header"</span><span class="token punctuation">:</span> <span class="token string">"header"</span><span class="token punctuation">,</span>
          <span class="token string">"body"</span><span class="token punctuation">:</span> <span class="token string">"body"</span><span class="token punctuation">,</span>
          <span class="token string">"footer"</span><span class="token punctuation">:</span> <span class="token string">"footer"</span><span class="token punctuation">,</span>
          <span class="token string">"flowId"</span><span class="token punctuation">:</span> <span class="token string">"&lt;Flow Id&gt;"</span><span class="token punctuation">,</span>
          <span class="token string">"screenName"</span><span class="token punctuation">:</span> <span class="token string">"Screen name"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeName"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"flowStatus"</span><span class="token punctuation">:</span> <span class="token string">"Draft"</span><span class="token punctuation">,</span>
          <span class="token string">"flowAction"</span><span class="token punctuation">:</span> <span class="token string">"data_exchange"</span><span class="token punctuation">,</span>
          <span class="token string">"buttonTitle"</span><span class="token punctuation">:</span> <span class="token string">"sdfas"</span><span class="token punctuation">,</span>
          <span class="token string">"flowToken"</span><span class="token punctuation">:</span> <span class="token string">"&lt;Flow Token&gt;"</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValidationErrorMessage"</span><span class="token punctuation">:</span> <span class="token string">"validation error message"</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"100"</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"200"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">874.3611353145966</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">437.1157457509522</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>

</code></pre>

