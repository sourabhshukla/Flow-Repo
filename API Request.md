---


---

<h1 id="api-request-node-setupwebhook">API Request Node (<code>setupWebhook</code>)</h1>
<p>This node is used to <strong>call an external HTTP API</strong> during the flow and <strong>capture values from the response into attributes</strong>.</p>
<blockquote>
<p><strong>Limit:</strong> A flow can contain <strong>maximum 5 API Request nodes</strong>.</p>
</blockquote>
<hr>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token comment">// Unique identifier for this node on the canvas</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579559028"</span><span class="token punctuation">,</span>

  <span class="token comment">// Wrapper node type</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>

  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token comment">// Whether this node is draggable in the editor UI</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>

    <span class="token comment">// Logical ID of the component (usually same as node id)</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579559028"</span><span class="token punctuation">,</span>

    <span class="token comment">// Content blocks inside this master component</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token comment">// Unique ID for this API request block</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579559028-setupWebhook"</span><span class="token punctuation">,</span>

        <span class="token comment">// Node type for API/Webhook calls</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"setupWebhook"</span><span class="token punctuation">,</span>

        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token comment">// Full HTTP request configuration</span>
          <span class="token string">"requestObject"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
            <span class="token comment">// Target URL for the API</span>
            <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"https://jsonplaceholder.typicode.com/todos/1"</span><span class="token punctuation">,</span>

            <span class="token comment">// HTTP method: "GET", "POST", "PUT", "DELETE", etc.</span>
            <span class="token string">"method"</span><span class="token punctuation">:</span> <span class="token string">"GET"</span><span class="token punctuation">,</span>

            <span class="token comment">// Query parameters (key/value pairs)</span>
            <span class="token comment">// Example: [ { "key": "page", "value": "1" } ]</span>
            <span class="token string">"params"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>

            <span class="token comment">// HTTP headers (key/value pairs)</span>
            <span class="token comment">// Example: [ { "key": "Authorization", "value": "Bearer &lt;token&gt;" } ]</span>
            <span class="token string">"headers"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>

            <span class="token comment">// Request body (for POST/PUT/PATCH, etc.)</span>
            <span class="token comment">// Can include variable placeholders like "$firstname"</span>
            <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
              <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"$firstname"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>

            <span class="token comment">// Whether the "Test API" action passed in the UI</span>
            <span class="token string">"isTestPass"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>

            <span class="token comment">// Whether the test request is currently in progress (UI loading state)</span>
            <span class="token string">"isLoading"</span><span class="token punctuation">:</span> <span class="token boolean">false</span>
          <span class="token punctuation">}</span><span class="token punctuation">,</span>

          <span class="token comment">// (Optional) Single attribute mapping from a top-level API response key</span>
          <span class="token comment">// Not used in this example (empty string)</span>
          <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>

          <span class="token comment">// (Optional) Single response key path corresponding to `attribute`</span>
          <span class="token comment">// Not used in this example (empty string)</span>
          <span class="token string">"responseKey"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>

          <span class="token comment">// List of HTTP status codes that are considered "valid"</span>
          <span class="token comment">// Empty array means default handling</span>
          <span class="token string">"statusCodes"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
          <span class="token punctuation">{</span>
              <span class="token comment">// Status Code</span>
              <span class="token string">"code"</span><span class="token punctuation">:</span> <span class="token string">"200"</span><span class="token punctuation">,</span>
              <span class="token comment">// Unique handle id</span>
              <span class="token string">"handleId"</span><span class="token punctuation">:</span> <span class="token string">"setup-webhoook-right-1763579559028-1763932678233"</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>

          <span class="token comment">// Multiple attribute mappings from the API response</span>
          <span class="token comment">// Each entry maps a response data path -&gt; attribute name</span>
          <span class="token string">"capturingAttributes"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token comment">// Attribute to store the full `data` object (stringified or as object)</span>
              <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"Name"</span><span class="token punctuation">,</span>
              <span class="token string">"responseKey"</span><span class="token punctuation">:</span> <span class="token string">"data"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>
              <span class="token comment">// Attribute for nested value data.userId</span>
              <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"FirstName"</span><span class="token punctuation">,</span>
              <span class="token string">"responseKey"</span><span class="token punctuation">:</span> <span class="token string">"data.userId"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>
              <span class="token comment">// Attribute for nested value data.title</span>
              <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"LastName"</span><span class="token punctuation">,</span>
              <span class="token string">"responseKey"</span><span class="token punctuation">:</span> <span class="token string">"data.title"</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  <span class="token comment">// Position of this node on the canvas</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">952.6054824670724</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">61.40899016172774</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
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

