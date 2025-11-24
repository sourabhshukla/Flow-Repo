---


---

<h1 id="keyword-node-keywordbox">Keyword Node (<code>keywordBox</code>)</h1>
<p>This node is used as an <strong>entry point</strong> to start a flow when:</p>
<ul>
<li>A user message matches <strong>any of the configured keywords</strong></li>
<li>A user replies using a <strong>linked template</strong></li>
<li>(Optionally) A user comes from QR campaigns or ads (if configured)</li>
<li>A user message matches a <strong>regex</strong> pattern (if <code>regex</code> is set)</li>
</ul>
<hr>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "keyword",

  // Node type for keyword-based entry
  "type": "keywordBox",

  "data": {
    // Label displayed on the node in the editor
    "label": "Node 1",

    // Helper/description text shown in the editor UI
    "text": "Add keywords to start chat ",

    // List of plain-text keywords that can trigger this flow
    // Matching behavior depends on platform logic (full match / contains).
    "keywords": [
      "hii",
      "hello"
    ],

    // List of WhatsApp templates that can also start this flow.
    // When a user replies to or interacts with these templates,
    // this node can be treated as the starting point.
    "templates": [
      {
        "_id": "65903279d094513802a87230",
      },
      {
         "_id": "6477047c8aac7f7df929e73e",
       }
    ],

    // When true, regex matching is case-sensitive
    "regexCaseSensitive": true,

    // Whether this node represents a newly created flow entry in the editor
    "isNewFlow": true,

    // Optional regex pattern for matching messages
    // If provided, engine can use this along with or instead of simple keywords.
    "regex": "/^\d+$/"
  },

  // Position on the canvas (relative)
  "position": {
    "x": -1262.4900259419146,
    "y": 595.4498502174376
  },

  // Absolute position used by the editor for rendering
  "positionAbsolute": {
    "x": -1214.4358850032481,
    "y": -395.28339594357766
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"keyword"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"keywordBox"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"label"</span><span class="token punctuation">:</span> <span class="token string">"Node 1"</span><span class="token punctuation">,</span>
    <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"Add keywords to start chat "</span><span class="token punctuation">,</span>
    <span class="token string">"keywords"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token string">"hii"</span><span class="token punctuation">,</span>
      <span class="token string">"hello"</span>
    <span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token string">"templates"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span><span class="token string">"&lt;templateMongoId&gt;"</span>
      <span class="token punctuation">}</span><span class="token punctuation">,</span>
      <span class="token punctuation">{</span>
         <span class="token string">"id"</span><span class="token punctuation">:</span><span class="token string">"&lt;templateMongoId&gt;"</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token string">"regexCaseSensitive"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"isNewFlow"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"regex"</span><span class="token punctuation">:</span> <span class="token string">"*a"</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1262.4900259419146</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token number">595.4498502174376</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"positionAbsolute"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1214.4358850032481</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">395.28339594357766</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

