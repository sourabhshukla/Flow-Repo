---


---

<h1 id="api-request-node-setupwebhook">API Request Node (<code>setupWebhook</code>)</h1>
<p>This node is used to <strong>call an external HTTP API</strong> during the flow and <strong>capture values from the response into attributes</strong>.</p>
<blockquote>
<p><strong>Limit:</strong> A flow can contain <strong>maximum 5 API Request nodes</strong>.</p>
</blockquote>
<hr>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763579559028",

  // Wrapper node type
  "type": "masterComponent",

  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Logical ID of the component (usually same as node id)
    "id": "1763579559028",

    // Content blocks inside this master component
    "content": [
      {
        // Unique ID for this API request block
        "id": "1763579559028-setupWebhook",

        // Node type for API/Webhook calls
        "type": "setupWebhook",

        "data": {
          // Full HTTP request configuration
          "requestObject": {
            // Target URL for the API
            "url": "https://jsonplaceholder.typicode.com/todos/1",

            // HTTP method: "GET", "POST", "PUT", "DELETE", etc.
            "method": "GET",

            // Query parameters (key/value pairs)
            // Example: [ { "key": "page", "value": "1" } ]
            "params": [],

            // HTTP headers (key/value pairs)
            // Example: [ { "key": "Authorization", "value": "Bearer &lt;token&gt;" } ]
            "headers": [],

            // Request body (for POST/PUT/PATCH, etc.)
            // Can include variable placeholders like "$firstname"
            "data": {
              "name": "$firstname"
            },

            // Whether the "Test API" action passed in the UI
            "isTestPass": true,

            // Whether the test request is currently in progress (UI loading state)
            "isLoading": false
          },

          // (Optional) Single attribute mapping from a top-level API response key
          // Not used in this example (empty string)
          "attribute": "",

          // (Optional) Single response key path corresponding to `attribute`
          // Not used in this example (empty string)
          "responseKey": "",

          // List of HTTP status codes that are considered "valid"
          // Empty array means default handling
          "statusCodes": [
          {
              // Status Code
              "code": "200",
              // Unique handle id
              "handleId": "setup-webhoook-right-1763579559028-1763932678233"
            }
          ],

          // Multiple attribute mappings from the API response
          // Each entry maps a response data path -&gt; attribute name
          "capturingAttributes": [
            {
              // Attribute to store the full `data` object (stringified or as object)
              "attribute": "Name",
              "responseKey": "data"
            },
            {
              // Attribute for nested value data.userId
              "attribute": "FirstName",
              "responseKey": "data.userId"
            },
            {
              // Attribute for nested value data.title
              "attribute": "LastName",
              "responseKey": "data.title"
            }
          ]
        }
      }
    ]
  },

  // Position of this node on the canvas
  "position": {
    "x": -952.6054824670724,
    "y": -61.40899016172774
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579559028"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579559028"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579559028-setupWebhook"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"setupWebhook"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"requestObject"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
            <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"https://jsonplaceholder.typicode.com/todos/1"</span><span class="token punctuation">,</span>
            <span class="token string">"method"</span><span class="token punctuation">:</span> <span class="token string">"GET"</span><span class="token punctuation">,</span>
            <span class="token string">"params"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
            <span class="token string">"headers"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
            <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
              <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"$firstname"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token string">"isTestPass"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
            <span class="token string">"isLoading"</span><span class="token punctuation">:</span> <span class="token boolean">false</span>
          <span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"responseKey"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"statusCodes"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"code"</span><span class="token punctuation">:</span> <span class="token string">"200"</span><span class="token punctuation">,</span>
              <span class="token string">"handleId"</span><span class="token punctuation">:</span> <span class="token string">"setup-webhoook-right-1763579559028-1763932678233"</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"capturingAttributes"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"Name"</span><span class="token punctuation">,</span>
              <span class="token string">"responseKey"</span><span class="token punctuation">:</span> <span class="token string">"data"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>
              <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"FirstName"</span><span class="token punctuation">,</span>
              <span class="token string">"responseKey"</span><span class="token punctuation">:</span> <span class="token string">"data.id"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>
              <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"LastName"</span><span class="token punctuation">,</span>
              <span class="token string">"responseKey"</span><span class="token punctuation">:</span> <span class="token string">"data.title"</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">952.6054824670724</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">61.40899016172774</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

