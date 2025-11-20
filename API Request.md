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
            <span class="token string">"testResponse"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
              <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                <span class="token string">"config"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                  <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"https://jsonplaceholder.typicode.com/todos/1"</span><span class="token punctuation">,</span>
                  <span class="token string">"method"</span><span class="token punctuation">:</span> <span class="token string">"get"</span><span class="token punctuation">,</span>
                  <span class="token string">"headers"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                    <span class="token string">"User-Agent"</span><span class="token punctuation">:</span> <span class="token string">"axios/0.21.4"</span>
                  <span class="token punctuation">}</span><span class="token punctuation">,</span>
                  <span class="token string">"params"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
                  <span class="token string">"transformRequest"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                    <span class="token keyword">null</span>
                  <span class="token punctuation">]</span><span class="token punctuation">,</span>
                  <span class="token string">"transformResponse"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                    <span class="token keyword">null</span>
                  <span class="token punctuation">]</span><span class="token punctuation">,</span>
                  <span class="token string">"timeout"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
                  <span class="token string">"xsrfCookieName"</span><span class="token punctuation">:</span> <span class="token string">"XSRF-TOKEN"</span><span class="token punctuation">,</span>
                  <span class="token string">"xsrfHeaderName"</span><span class="token punctuation">:</span> <span class="token string">"X-XSRF-TOKEN"</span><span class="token punctuation">,</span>
                  <span class="token string">"maxContentLength"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">,</span>
                  <span class="token string">"maxBodyLength"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">,</span>
                  <span class="token string">"transitional"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                    <span class="token string">"silentJSONParsing"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
                    <span class="token string">"forcedJSONParsing"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
                    <span class="token string">"clarifyTimeoutError"</span><span class="token punctuation">:</span> <span class="token boolean">false</span>
                  <span class="token punctuation">}</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                  <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
                  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
                  <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"delectus aut autem"</span><span class="token punctuation">,</span>
                  <span class="token string">"completed"</span><span class="token punctuation">:</span> <span class="token boolean">false</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token string">"headers"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                  <span class="token string">"date"</span><span class="token punctuation">:</span> <span class="token string">"Wed, 19 Nov 2025 19:13:14 GMT"</span><span class="token punctuation">,</span>
                  <span class="token string">"content-type"</span><span class="token punctuation">:</span> <span class="token string">"application/json; charset=utf-8"</span><span class="token punctuation">,</span>
                  <span class="token string">"content-length"</span><span class="token punctuation">:</span> <span class="token string">"83"</span><span class="token punctuation">,</span>
                  <span class="token string">"connection"</span><span class="token punctuation">:</span> <span class="token string">"close"</span><span class="token punctuation">,</span>
                  <span class="token string">"access-control-allow-credentials"</span><span class="token punctuation">:</span> <span class="token string">"true"</span><span class="token punctuation">,</span>
                  <span class="token string">"cache-control"</span><span class="token punctuation">:</span> <span class="token string">"max-age=43200"</span><span class="token punctuation">,</span>
                  <span class="token string">"etag"</span><span class="token punctuation">:</span> <span class="token string">"W/\"53-hfEnumeNh6YirfjyjaujcOPPT+s\""</span><span class="token punctuation">,</span>
                  <span class="token string">"expires"</span><span class="token punctuation">:</span> <span class="token string">"-1"</span><span class="token punctuation">,</span>
                  <span class="token string">"nel"</span><span class="token punctuation">:</span> <span class="token string">"{\"report_to\":\"heroku-nel\",\"response_headers\":[\"Via\"],\"max_age\":3600,\"success_fraction\":0.01,\"failure_fraction\":0.1}"</span><span class="token punctuation">,</span>
                  <span class="token string">"pragma"</span><span class="token punctuation">:</span> <span class="token string">"no-cache"</span><span class="token punctuation">,</span>
                  <span class="token string">"report-to"</span><span class="token punctuation">:</span> <span class="token string">"{\"group\":\"heroku-nel\",\"endpoints\":[{\"url\":\"https://nel.heroku.com/reports?s=BcSAsSlGMsGSceqa%2Be2c4XTFtuApvV%2FHM7emB%2F8fHVU%3D\\u0026sid=e11707d5-02a7-43ef-b45e-2cf4d2036f7d\\u0026ts=1752468645\"}],\"max_age\":3600}"</span><span class="token punctuation">,</span>
                  <span class="token string">"reporting-endpoints"</span><span class="token punctuation">:</span> <span class="token string">"heroku-nel=\"https://nel.heroku.com/reports?s=BcSAsSlGMsGSceqa%2Be2c4XTFtuApvV%2FHM7emB%2F8fHVU%3D&amp;sid=e11707d5-02a7-43ef-b45e-2cf4d2036f7d&amp;ts=1752468645\""</span><span class="token punctuation">,</span>
                  <span class="token string">"server"</span><span class="token punctuation">:</span> <span class="token string">"cloudflare"</span><span class="token punctuation">,</span>
                  <span class="token string">"vary"</span><span class="token punctuation">:</span> <span class="token string">"Origin, Accept-Encoding"</span><span class="token punctuation">,</span>
                  <span class="token string">"via"</span><span class="token punctuation">:</span> <span class="token string">"2.0 heroku-router"</span><span class="token punctuation">,</span>
                  <span class="token string">"x-content-type-options"</span><span class="token punctuation">:</span> <span class="token string">"nosniff"</span><span class="token punctuation">,</span>
                  <span class="token string">"x-powered-by"</span><span class="token punctuation">:</span> <span class="token string">"Express"</span><span class="token punctuation">,</span>
                  <span class="token string">"x-ratelimit-limit"</span><span class="token punctuation">:</span> <span class="token string">"1000"</span><span class="token punctuation">,</span>
                  <span class="token string">"x-ratelimit-remaining"</span><span class="token punctuation">:</span> <span class="token string">"999"</span><span class="token punctuation">,</span>
                  <span class="token string">"x-ratelimit-reset"</span><span class="token punctuation">:</span> <span class="token string">"1752468652"</span><span class="token punctuation">,</span>
                  <span class="token string">"age"</span><span class="token punctuation">:</span> <span class="token string">"21909"</span><span class="token punctuation">,</span>
                  <span class="token string">"accept-ranges"</span><span class="token punctuation">:</span> <span class="token string">"bytes"</span><span class="token punctuation">,</span>
                  <span class="token string">"cf-cache-status"</span><span class="token punctuation">:</span> <span class="token string">"HIT"</span><span class="token punctuation">,</span>
                  <span class="token string">"server-timing"</span><span class="token punctuation">:</span> <span class="token string">"cfCacheStatus;desc=\"HIT\", cfEdge;dur=4,cfOrigin;dur=0"</span><span class="token punctuation">,</span>
                  <span class="token string">"cf-ray"</span><span class="token punctuation">:</span> <span class="token string">"9a1206120e1b55fe-BOM"</span><span class="token punctuation">,</span>
                  <span class="token string">"alt-svc"</span><span class="token punctuation">:</span> <span class="token string">"h3=\":443\"; ma=86400"</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">200</span>
              <span class="token punctuation">}</span><span class="token punctuation">,</span>
              <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">200</span><span class="token punctuation">,</span>
              <span class="token string">"statusText"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
              <span class="token string">"headers"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                <span class="token string">"content-type"</span><span class="token punctuation">:</span> <span class="token string">"application/json; charset=utf-8"</span>
              <span class="token punctuation">}</span><span class="token punctuation">,</span>
              <span class="token string">"config"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"https://backend.aisensy.com/client/t1/testing/webhook-test"</span><span class="token punctuation">,</span>
                <span class="token string">"method"</span><span class="token punctuation">:</span> <span class="token string">"post"</span><span class="token punctuation">,</span>
                <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token string">"{\"url\":\"https://jsonplaceholder.typicode.com/todos/1\",\"method\":\"GET\",\"params\":[],\"headers\":[],\"data\":{\"name\":\"$firstname\"},\"assistantId\":\"633829cd86fc494a463d86e8\"}"</span><span class="token punctuation">,</span>
                <span class="token string">"headers"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                  <span class="token string">"Accept"</span><span class="token punctuation">:</span> <span class="token string">"application/json, text/plain, */*"</span><span class="token punctuation">,</span>
                  <span class="token string">"Content-Type"</span><span class="token punctuation">:</span> <span class="token string">"application/json;charset=utf-8"</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token string">"transformRequest"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                  <span class="token keyword">null</span>
                <span class="token punctuation">]</span><span class="token punctuation">,</span>
                <span class="token string">"transformResponse"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                  <span class="token keyword">null</span>
                <span class="token punctuation">]</span><span class="token punctuation">,</span>
                <span class="token string">"timeout"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
                <span class="token string">"withCredentials"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
                <span class="token string">"xsrfCookieName"</span><span class="token punctuation">:</span> <span class="token string">"XSRF-TOKEN"</span><span class="token punctuation">,</span>
                <span class="token string">"xsrfHeaderName"</span><span class="token punctuation">:</span> <span class="token string">"X-XSRF-TOKEN"</span><span class="token punctuation">,</span>
                <span class="token string">"maxContentLength"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token string">"maxBodyLength"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1</span>
              <span class="token punctuation">}</span><span class="token punctuation">,</span>
              <span class="token string">"request"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span><span class="token punctuation">}</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
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
              <span class="token string">"responseKey"</span><span class="token punctuation">:</span> <span class="token string">"data.userId"</span>
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

