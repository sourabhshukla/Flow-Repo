---


---

<h1 id="add-tag-node-addtag">Add Tag Node (<code>addTag</code>)</h1>
<p>This node is used to <strong>attach one or more tags</strong> to the current contact/conversation.</p>
<p>Typical use cases:</p>
<ul>
<li>Marking important events in the journey (e.g. <code>zoom_booked</code>)</li>
<li>Segmenting users (e.g. <code>request callback demo</code>)</li>
<li>Triggering analytics or downstream workflows based on tags.</li>
</ul>
<hr>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token comment">// Unique identifier for this node on the canvas</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579182272"</span><span class="token punctuation">,</span>

  <span class="token comment">// Node type wrapper</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>

  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token comment">// Whether this node is draggable in the editor UI</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>

    <span class="token comment">// Logical ID of the component (usually same as node id)</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579182272"</span><span class="token punctuation">,</span>

    <span class="token comment">// Content blocks inside this node</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token comment">// Unique ID for this add-tag block</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763579182272-addTag"</span><span class="token punctuation">,</span>

        <span class="token comment">// Node type for adding tags</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"addTag"</span><span class="token punctuation">,</span>

        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token comment">// Array of tag objects to be applied.</span>
          <span class="token comment">// Typically these are pre-configured tags from your system.</span>
          <span class="token string">"tags"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token comment">// Name of tag</span>
              <span class="token string">"tagName"</span><span class="token punctuation">:</span> <span class="token string">"My tag 1"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>
              <span class="token string">"tagName"</span><span class="token punctuation">:</span> <span class="token string">"My tag 2"</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  <span class="token comment">// Position of this node on the canvas</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1025.197908140377</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">247.49098273273367</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
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
              <span class="token string">"tagName"</span><span class="token punctuation">:</span> <span class="token string">"My tag 1"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>
              <span class="token string">"tagName"</span><span class="token punctuation">:</span> <span class="token string">"My tag 2"</span>
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

