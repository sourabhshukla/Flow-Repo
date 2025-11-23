---


---

<h1 id="media-component-node-imagewithcaption">Media Component Node (<code>imageWithCaption</code>)</h1>
<p>This node is used to send <strong>media + caption + buttons</strong>.<br>
The same structure is used for:</p>
<ul>
<li><code>fileType: "IMAGE"</code></li>
<li><code>fileType: "AUDIO"</code></li>
<li><code>fileType: "VIDEO"</code></li>
<li><code>fileType: "FILE"</code></li>
</ul>
<h2 id="json-structure-with-comments">JSON Structure (with comments)</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763566563619",

  // Node type - still a masterComponent
  "type": "masterComponent",

  // Node configuration and content
  "data": {
    // Whether this node is draggable in the editor
    "isDrag": true,

    // Logical ID for the component (usually same as node id)
    "id": "1763566563619",

    // List of content blocks. Here we have one media block.
    "content": [
      {
        // Unique ID for this specific media block
        "id": "1763566563619-imageWithCaption",

        // Content type for media + caption
        // Used for IMAGE, AUDIO, VIDEO, FILE
        "type": "imageWithCaption",

        "data": {
          // Public URL of the media file
          // Prefix path usually encodes the media type: IMAGE / AUDIO / VIDEO / FILE
          "url": "https://d3jt6ku4g6z5l8.cloudfront.net/IMAGE/633829cd86fc494a463d86e8/4762179_Rectangle 40737.jpg",

          // Caption or text shown with the media
          "text": "caption",

          // Type of file being sent.
          // Allowed values: "IMAGE" | "AUDIO" | "VIDEO" | "FILE"
          "fileType": "IMAGE",

          // Optional buttons rendered below the media + caption
          // Button rules:
          // - 0 buttons allowed
          // - Maximum 3 buttons allowed
          "buttons": [
            {
              // Button label
              "text": "button 1",

              // Unique button identifier (for click handling / analytics)
              "id": 1763566654196
            }
          ],

          // When true, use `time` to auto-continue after a timeout
          "timeoutToggle": true,

          // Optional delay before sending/showing this media message (in seconds)
          "delay": "12",

          // Timeout duration when timeoutToggle is true (in minutes)
          "time": "23"
        }
      }
    ]
  },

  // Canvas position of this node
  "position": {
    "x": -765.7998046875,
    "y": -527.9233245849609
  }
}
</code></pre>
<hr>
<h2 id="clean-json-examples">Clean JSON Examples</h2>
<h3 id="audio">AUDIO</h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619-imageWithCaption"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"imageWithCaption"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"https://d3jt6ku4g6z5l8.cloudfront.net/AUDIO/633829cd86fc494a463d86e8/7752888_poonawala.mp3"</span><span class="token punctuation">,</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"caption"</span><span class="token punctuation">,</span>
          <span class="token string">"fileType"</span><span class="token punctuation">:</span> <span class="token string">"AUDIO"</span><span class="token punctuation">,</span>
          <span class="token string">"buttons"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"button 1"</span><span class="token punctuation">,</span>
              <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1763566654196</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"12"</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"23"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">765.7998046875</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">527.9233245849609</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="image">IMAGE</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619-imageWithCaption"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"imageWithCaption"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"https://d3jt6ku4g6z5l8.cloudfront.net/IMAGE/633829cd86fc494a463d86e8/4762179_Rectangle 40737.jpg"</span><span class="token punctuation">,</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"caption"</span><span class="token punctuation">,</span>
          <span class="token string">"fileType"</span><span class="token punctuation">:</span> <span class="token string">"IMAGE"</span><span class="token punctuation">,</span>
          <span class="token string">"buttons"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"button 1"</span><span class="token punctuation">,</span>
              <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1763566654196</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"12"</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"23"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">765.7998046875</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">527.9233245849609</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="video">VIDEO</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619-imageWithCaption"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"imageWithCaption"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"https://d3jt6ku4g6z5l8.cloudfront.net/VIDEO/633829cd86fc494a463d86e8/1733790_WhatsApp%20Video%2020230530%20at%201.07.12%20PM.mp4"</span><span class="token punctuation">,</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"caption"</span><span class="token punctuation">,</span>
          <span class="token string">"fileType"</span><span class="token punctuation">:</span> <span class="token string">"VIDEO"</span><span class="token punctuation">,</span>
          <span class="token string">"buttons"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"button 1"</span><span class="token punctuation">,</span>
              <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1763566654196</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"12"</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"23"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">765.7998046875</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">527.9233245849609</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="file">FILE</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763566563619-imageWithCaption"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"imageWithCaption"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"https://d3jt6ku4g6z5l8.cloudfront.net/FILE/633829cd86fc494a463d86e8/2273386_WhatsApp%20New%20ConversationalBased%20Pricing.pdf"</span><span class="token punctuation">,</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"caption"</span><span class="token punctuation">,</span>
          <span class="token string">"fileType"</span><span class="token punctuation">:</span> <span class="token string">"FILE"</span><span class="token punctuation">,</span>
          <span class="token string">"buttons"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"button 1"</span><span class="token punctuation">,</span>
              <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1763566654196</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"12"</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"23"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">765.7998046875</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">527.9233245849609</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

