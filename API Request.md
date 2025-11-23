---


---

<h1 id="api-request-node-setupwebhook">API Request Node (<code>setupWebhook</code>)</h1>
<p>This node is used to <strong>call an external HTTP API</strong> during the flow and <strong>capture values from the response into attributes</strong>.</p>
<blockquote>
<p><strong>Limit:</strong> A flow can contain <strong>maximum 5 API Request nodes</strong>.</p>
</blockquote>
<hr>
<h2 id="json-structure-with-comments">JSON Structure (with comments)</h2>
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

            // Raw test response stored from the last manual test call.
            // This mirrors an Axios-like response object.
            "testResponse": {
              "data": {
                // Original request config used in the test
                "config": {
                  "url": "https://jsonplaceholder.typicode.com/todos/1",
                  "method": "get",
                  "headers": {
                    "User-Agent": "axios/0.21.4"
                  },
                  "params": [],
                  "transformRequest": [null],
                  "transformResponse": [null],
                  "timeout": 0,
                  "xsrfCookieName": "XSRF-TOKEN",
                  "xsrfHeaderName": "X-XSRF-TOKEN",
                  "maxContentLength": -1,
                  "maxBodyLength": -1,
                  "transitional": {
                    "silentJSONParsing": true,
                    "forcedJSONParsing": true,
                    "clarifyTimeoutError": false
                  }
                },

                // Actual response body returned by the API
                "data": {
                  "userId": 1,
                  "id": 1,
                  "title": "delectus aut autem",
                  "completed": false
                },

                // Response headers from the target API
                "headers": {
                  "date": "Wed, 19 Nov 2025 19:13:14 GMT",
                  "content-type": "application/json; charset=utf-8",
                  "content-length": "83",
                  "connection": "close",
                  "access-control-allow-credentials": "true",
                  "cache-control": "max-age=43200",
                  "etag": "W/\"53-hfEnumeNh6YirfjyjaujcOPPT+s\"",
                  "expires": "-1",
                  "nel": "{...}",
                  "pragma": "no-cache",
                  "report-to": "{...}",
                  "reporting-endpoints": "heroku-nel=\"...\"",
                  "server": "cloudflare",
                  "vary": "Origin, Accept-Encoding",
                  "via": "2.0 heroku-router",
                  "x-content-type-options": "nosniff",
                  "x-powered-by": "Express",
                  "x-ratelimit-limit": "1000",
                  "x-ratelimit-remaining": "999",
                  "x-ratelimit-reset": "1752468652",
                  "age": "21909",
                  "accept-ranges": "bytes",
                  "cf-cache-status": "HIT",
                  "server-timing": "cfCacheStatus;desc=\"HIT\", cfEdge;dur=4,cfOrigin;dur=0",
                  "cf-ray": "9a1206120e1b55fe-BOM",
                  "alt-svc": "h3=\":443\"; ma=86400"
                },

                // HTTP status code from the target API
                "status": 200
              },

              // High-level status wrapper
              "status": 200,
              "statusText": "",

              // Top-level headers in the stored test response
              "headers": {
                "content-type": "application/json; charset=utf-8"
              },

              // Axios request config for the internal test endpoint
              "config": {
                "url": "https://backend.aisensy.com/client/t1/testing/webhook-test",
                "method": "post",
                "data": "{\"url\":\"https://jsonplaceholder.typicode.com/todos/1\",\"method\":\"GET\",\"params\":[],\"headers\":[],\"data\":{\"name\":\"$firstname\"},\"assistantId\":\"633829cd86fc494a463d86e8\"}",
                "headers": {
                  "Accept": "application/json, text/plain, */*",
                  "Content-Type": "application/json;charset=utf-8"
                },
                "transformRequest": [null],
                "transformResponse": [null],
                "timeout": 0,
                "withCredentials": true,
                "xsrfCookieName": "XSRF-TOKEN",
                "xsrfHeaderName": "X-XSRF-TOKEN",
                "maxContentLength": -1,
                "maxBodyLength": -1
              },

              // Placeholder for underlying request object
              "request": {}
            },

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
          "statusCodes": [],

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
<h2 id="clean-json-no-comments">Clean JSON (no comments)</h2>
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
          <span class="token string">"statusCodes"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
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

