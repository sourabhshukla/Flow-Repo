---


---

<h1 id="template-node-templatemessage-–-runtime-payload">Template Node (<code>templateMessage</code>) – Runtime Payload</h1>
<p>This node is used to <strong>send a WhatsApp template message (HSM)</strong>.</p>
<p>Inside <code>content[0].data</code> (the inner <code>data</code> object), you only need to pass:</p>
<ul>
<li><code>id</code> → internal DB id of the template (<code>_id</code> from your template collection)</li>
<li><code>templateParams</code> → array of parameter values in order of <code>{{1}}</code>, <code>{{2}}</code>, …</li>
<li><code>formattedButtons</code> → runtime button configuration (e.g. for dynamic URLs / parameters)</li>
</ul>
<hr>
<h2 id="full-sample">1. Full Sample</h2>
<p>For reference, here is the full object you gave initially:</p>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Node id on the canvas
  "id": "1763634895184",

  // Wrapper type for all flow nodes
  "type": "masterComponent",

  "data": {
    // Draggable flag in the editor
    "isDrag": true,

    // Same as node id, used internally
    "id": "1763634895184",

    "content": [
      {
        // Unique id for this template block
        "id": "1763634895184-templateMessage",

        // Node type
        "type": "templateMessage",
        
        "data": {
          // Template id
          "id": "6904779fdfeeb70d508d1fe7",

          // Ordered list of parameter values for {{1}}, {{2}}, ...
          "templateParams": [
            "1234"
          ],

          // Button runtime config (dynamic values, URLs, etc.)
          "formattedButtons": [
            {
               "type": "BUTTON",
               "sub_type": "URL",
               "index": 0,
               "parameters": [
                // Parameter in URL
                {
                  "type": "text",
                  "text": "12345"
                }
              ]
            }
          ]
        }
      }
    ]
  },

  // Canvas position
  "position": {
    "x": -170,
    "y": 11
  }
}
</code></pre>
<pre><code>{
  "id": "1763634895184",
  "type": "masterComponent",
  "data": {
    "isDrag": true,
    "id": "1763634895184",
    "content": [
      {
        "id": "1763634895184-templateMessage",
        "type": "templateMessage",
        "data": {
          "id": "6904779fdfeeb70d508d1fe7",
          "templateParams": [
            "1234"
          ],
          "formattedButtons": [
            {
              "type": "BUTTON",
              "sub_type": "URL",
              "index": 0,
              "parameters": [
                {
                  "type": "text",
                  "text": "12345"
                }
              ]
            }
          ]
        }
      }
    ]
  },
  "position": {
    "x": -170,
    "y": 11
  }
}
</code></pre>
<h3 id="text-template">1. Text Template</h3>
<p>Here the template has 2 body parameters and one button of type url and the button also has one parameter. In case there is no parameter in the button we don’t need to add the button in <code>formattedButtons</code> here.</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763634895184"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763634895184"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763634895184-templateMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"templateMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"6904779fdfeeb70d508d1fe7"</span><span class="token punctuation">,</span>
          <span class="token string">"templateParams"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token string">"param1"</span><span class="token punctuation">,</span><span class="token string">"param2"</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"formattedButtons"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"BUTTON"</span><span class="token punctuation">,</span>
              <span class="token string">"sub_type"</span><span class="token punctuation">:</span> <span class="token string">"URL"</span><span class="token punctuation">,</span>
              <span class="token string">"index"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
              <span class="token string">"parameters"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token punctuation">{</span>
                  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"text"</span><span class="token punctuation">,</span>
                  <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"xyz"</span>
                <span class="token punctuation">}</span>
              <span class="token punctuation">]</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">170</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token number">11</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="imagevideodocument-template">2. Image/Video/Document Template</h3>
<p>In case of these templates one more attribute <code>url</code> will be added.</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763634895184"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763634895184"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763634895184-templateMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"templateMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"6904779fdfeeb70d508d1fe7"</span><span class="token punctuation">,</span>
          <span class="token string">"templateParams"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token string">"param1"</span><span class="token punctuation">,</span><span class="token string">"param2"</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"url"</span><span class="token punctuation">:</span><span class="token string">"https://d3jt6ku4g6z5l8.cloudfront.net/VIDEO/633829cd86fc494a463d86e8/7175738_WhatsApp%20Video%2020240111%20at%2018.31.21%201%201.mp4"</span><span class="token punctuation">,</span>
          <span class="token string">"formattedButtons"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"BUTTON"</span><span class="token punctuation">,</span>
              <span class="token string">"sub_type"</span><span class="token punctuation">:</span> <span class="token string">"URL"</span><span class="token punctuation">,</span>
              <span class="token string">"index"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
              <span class="token string">"parameters"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token punctuation">{</span>
                  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"text"</span><span class="token punctuation">,</span>
                  <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"xyz"</span>
                <span class="token punctuation">}</span>
              <span class="token punctuation">]</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">170</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token number">11</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="in-case-of-copy-code-button">3. In case of COPY CODE Button</h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763634895184"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763634895184"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763634895184-templateMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"templateMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"6904779fdfeeb70d508d1fe7"</span><span class="token punctuation">,</span>
          <span class="token string">"templateParams"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token string">"param1"</span><span class="token punctuation">,</span>
            <span class="token string">"param2"</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"https://d3jt6ku4g6z5l8.cloudfront.net/VIDEO/633829cd86fc494a463d86e8/7175738_WhatsApp%20Video%2020240111%20at%2018.31.21%201%201.mp4"</span><span class="token punctuation">,</span>
          <span class="token string">"formattedButtons"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"BUTTON"</span><span class="token punctuation">,</span>
              <span class="token string">"sub_type"</span><span class="token punctuation">:</span> <span class="token string">"URL"</span><span class="token punctuation">,</span>
              <span class="token string">"index"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
              <span class="token string">"parameters"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token punctuation">{</span>
                  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"text"</span><span class="token punctuation">,</span>
                  <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"xyz"</span>
                <span class="token punctuation">}</span>
              <span class="token punctuation">]</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>
              <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"BUTTON"</span><span class="token punctuation">,</span>
              <span class="token string">"sub_type"</span><span class="token punctuation">:</span> <span class="token string">"COPY_CODE"</span><span class="token punctuation">,</span>
              <span class="token string">"index"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
              <span class="token string">"parameters"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token punctuation">{</span>
                  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"coupon_code"</span><span class="token punctuation">,</span>
                  <span class="token string">"coupon_code"</span><span class="token punctuation">:</span> <span class="token string">"sdf"</span>
                <span class="token punctuation">}</span>
              <span class="token punctuation">]</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">170</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token number">11</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

