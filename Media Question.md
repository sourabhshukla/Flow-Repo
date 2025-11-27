---


---

<h1 id="media-question-node-questionmediamessage">Media Question Node (<code>questionMediaMessage</code>)</h1>
<p>This node is used to <strong>ask the user for a media response</strong> and store the result in an attribute.</p>
<ul>
<li>Validation type is fixed as: <code>attributeFormat: "Media"</code></li>
<li>The expected media type is controlled by <code>mediaType</code>.</li>
</ul>
<p>Supported <code>mediaType</code> values:</p>
<ul>
<li><code>Any</code></li>
<li><code>Image</code></li>
<li><code>Video</code></li>
<li><code>Document</code></li>
<li><code>Audio</code></li>
</ul>
<p>Other behavior (attempts, delay, timeout) works like the normal question node.</p>
<hr>
<h2 id="generic-media-question-node-with-comments">Generic Media Question Node (with comments)</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763577888932",

  // Wrapper node type
  "type": "masterComponent",

  "data": {
    // Node is draggable in editor
    "isDrag": true,

    // Logical component ID
    "id": "1763577888932",

    "content": [
      {
        // Unique ID for this media question block
        "id": "1763577888932-questionMediaMessage",

        // Node type for media questions
        "type": "questionMediaMessage",

        "data": {
          // Question text shown to the user
          "text": "Enter link",

          // Attribute where the media reference (URL/id) will be stored
          "attribute": "VideoLink",

          // Maximum number of validation attempts (stringified integer)
          "attributeNumberOfAttempt": "1",

          // Extra validation config (currently not used for Media, but kept for consistency)
          "attributeFormatValue": {
            "min": "",
            "max": "",
            "regex": ""
          },

          // Error message shown when validation fails
          "attributeFormatValidationErrorMessage": "Error",

          // Validation type for this node is always "Media"
          "attributeFormat": "Media",

          // Expected media type:
          // "Any" | "Image" | "Video" | "Document" | "Audio"
          "mediaType": "Any",

          // Delay before asking this question (UNIT: SECONDS)
          "delay": "10",

          // Enables timeout when true
          "timeoutToggle": true,

          // Timeout duration after sending the message (UNIT: MINUTES)
          "time": "2"
        }
      }
    ]
  },

  // Position of this node on the canvas
  "position": {
    "x": -893.304627691697,
    "y": -291.45540954896035
  }
}
</code></pre>
<hr>
<h2 id="clean-json-examples-no-comments">Clean JSON Examples (no comments)</h2>
<h3 id="mediatype-any">1. <code>mediaType: "Any"</code></h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932-questionMediaMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"questionMediaMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"Enter link"</span><span class="token punctuation">,</span>
          <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"Link"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeNumberOfAttempt"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValue"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
            <span class="token string">"min"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"max"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"regex"</span><span class="token punctuation">:</span> <span class="token string">""</span>
          <span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValidationErrorMessage"</span><span class="token punctuation">:</span> <span class="token string">"Error"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormat"</span><span class="token punctuation">:</span> <span class="token string">"Media"</span><span class="token punctuation">,</span>
          <span class="token string">"mediaType"</span><span class="token punctuation">:</span> <span class="token string">"Any"</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"10"</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"2"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">893.304627691697</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">291.45540954896035</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="mediatype-image">2. <code>mediaType: "Image"</code></h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932-questionMediaMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"questionMediaMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"Enter link"</span><span class="token punctuation">,</span>
          <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"ImageLink"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeNumberOfAttempt"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValue"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
            <span class="token string">"min"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"max"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"regex"</span><span class="token punctuation">:</span> <span class="token string">""</span>
          <span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValidationErrorMessage"</span><span class="token punctuation">:</span> <span class="token string">"Error"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormat"</span><span class="token punctuation">:</span> <span class="token string">"Media"</span><span class="token punctuation">,</span>
          <span class="token string">"mediaType"</span><span class="token punctuation">:</span> <span class="token string">"Image"</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"10"</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"2"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">900.4616274059665</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">367.1151208140946</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="mediatype-video">3. <code>mediaType: "Video"</code></h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932-questionMediaMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"questionMediaMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"Enter link"</span><span class="token punctuation">,</span>
          <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"VideoLink"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeNumberOfAttempt"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValue"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
            <span class="token string">"min"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"max"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"regex"</span><span class="token punctuation">:</span> <span class="token string">""</span>
          <span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValidationErrorMessage"</span><span class="token punctuation">:</span> <span class="token string">"Error"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormat"</span><span class="token punctuation">:</span> <span class="token string">"Media"</span><span class="token punctuation">,</span>
          <span class="token string">"mediaType"</span><span class="token punctuation">:</span> <span class="token string">"Video"</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"10"</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"2"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">900.4616274059665</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">367.1151208140946</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="mediatype-document">4. <code>mediaType: "Document"</code></h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932-questionMediaMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"questionMediaMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"Enter link"</span><span class="token punctuation">,</span>
          <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"DocLink"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeNumberOfAttempt"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValue"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
            <span class="token string">"min"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"max"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"regex"</span><span class="token punctuation">:</span> <span class="token string">""</span>
          <span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValidationErrorMessage"</span><span class="token punctuation">:</span> <span class="token string">"Error"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormat"</span><span class="token punctuation">:</span> <span class="token string">"Media"</span><span class="token punctuation">,</span>
          <span class="token string">"mediaType"</span><span class="token punctuation">:</span> <span class="token string">"Document"</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"10"</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"2"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">900.4616274059665</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">367.1151208140946</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="mediatype-audio">5. <code>mediaType: "Audio"</code></h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763577888932-questionMediaMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"questionMediaMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"Enter link"</span><span class="token punctuation">,</span>
          <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"AudioLink"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeNumberOfAttempt"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValue"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
            <span class="token string">"min"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"max"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"regex"</span><span class="token punctuation">:</span> <span class="token string">""</span>
          <span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValidationErrorMessage"</span><span class="token punctuation">:</span> <span class="token string">"Error"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormat"</span><span class="token punctuation">:</span> <span class="token string">"Media"</span><span class="token punctuation">,</span>
          <span class="token string">"mediaType"</span><span class="token punctuation">:</span> <span class="token string">"Audio"</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"10"</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"2"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">900.4616274059665</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">367.1151208140946</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

