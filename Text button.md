---


---

<h1 id="text-button-node">Text Button Node</h1>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token comment">// Unique identifier (timestamp) for the node on the canvas</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763564100751"</span><span class="token punctuation">,</span>

  <span class="token comment">// Node type - "masterComponent" nodes represent reusable message blocks</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>

  <span class="token comment">// All configuration &amp; content for this node</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token comment">// Whether this node is draggable in the editor UI</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>

    <span class="token comment">// Same as node id above</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763564100751"</span><span class="token punctuation">,</span>

    <span class="token comment">// Array of content blocks inside this master component</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token comment">// Unique ID for this specific content block</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763564100751-message"</span><span class="token punctuation">,</span>

        <span class="token comment">// Content type. For now we support "message"</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"message"</span><span class="token punctuation">,</span>

        <span class="token comment">// Payload for the message shown to the end user</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token comment">// Text that will be sent/rendered as the message bubble</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"This is demo message"</span><span class="token punctuation">,</span>

          <span class="token comment">// Optional array of buttons rendered below the message</span>
          <span class="token comment">// - 0 buttons allowed (no array or empty array)</span>
          <span class="token comment">// - Max 3 buttons allowed</span>
          <span class="token string">"buttons"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token comment">// Label shown on the button</span>
              <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"button text"</span><span class="token punctuation">,</span>

              <span class="token comment">// Unique identifier for this button (for click handling/analytics)</span>
              <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1763564160176</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>

          <span class="token comment">// Optional delay before this message is sent/shown (in seconds)</span>
          <span class="token comment">// "" =&gt; use default behavior / no explicit delay</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"12"</span><span class="token punctuation">,</span>

          <span class="token comment">// When true, a timeout will be applied using the "time" field</span>
          <span class="token comment">// When false, message waits for user action or next explicit trigger</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>

          <span class="token comment">// Duration used when timeoutToggle is true (in minutes)</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"12"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  <span class="token comment">// Position of this node on the editor canvas (in pixels)</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token comment">// Horizontal coordinate</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">334.3917236328125</span><span class="token punctuation">,</span>

    <span class="token comment">// Vertical coordinate</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">86.28158569335938</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>

</code></pre>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763564100751"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763564100751"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763564100751-message"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"message"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"this is demo message"</span><span class="token punctuation">,</span>
          <span class="token string">"buttons"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"button text"</span><span class="token punctuation">,</span>
              <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1763564160176</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"12"</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"12"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">334.3917236328125</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">86.28158569335938</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

