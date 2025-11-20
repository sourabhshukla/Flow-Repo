---


---

<h1 id="edge-structure">Edge Structure</h1>
<p>An edge connects an <strong>output handle</strong> of a source node to the <strong>input handle</strong> of a target node.</p>
<p>Most properties of an edge are <strong>constant</strong>. Only these change:</p>
<ul>
<li><code>source</code></li>
<li><code>sourceHandle</code></li>
<li><code>target</code></li>
</ul>
<hr>
<h2 id="generic-edge">1. Generic Edge</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // ID of the source node (or special keyword "keyword")
  "source": "keyword",

  // ID of the specific handle on the source node
  // (varies by node/component type, see patterns below)
  "sourceHandle": "keyword-right-keyword",

  // ID of the target node (always the node's id)
  "target": "1763581453582",

  // Edge type – fixed for all edges in this flow builder
  "type": "buttonedge",

  // Arrow marker at the end of the edge – fixed style
  "markerEnd": {
    "type": "arrowclosed",
    "width": 20,
    "height": 20,
    "color": "#008069"
  },

  // Whether the edge is animated – fixed
  "animated": true,

  // Stroke styling for the edge – fixed
  "style": {
    "strokeWidth": 1,
    "stroke": "#008069"
  }
}
</code></pre>
<h2 id="clean-json-example">2. Clean JSON Example</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"source"</span><span class="token punctuation">:</span> <span class="token string">"keyword"</span><span class="token punctuation">,</span>
  <span class="token string">"sourceHandle"</span><span class="token punctuation">:</span> <span class="token string">"keyword-right-keyword"</span><span class="token punctuation">,</span>
  <span class="token string">"target"</span><span class="token punctuation">:</span> <span class="token string">"1763581453582"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"buttonedge"</span><span class="token punctuation">,</span>
  <span class="token string">"markerEnd"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"arrowclosed"</span><span class="token punctuation">,</span>
    <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">20</span><span class="token punctuation">,</span>
    <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">20</span><span class="token punctuation">,</span>
    <span class="token string">"color"</span><span class="token punctuation">:</span> <span class="token string">"#008069"</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"animated"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
  <span class="token string">"style"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"strokeWidth"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
    <span class="token string">"stroke"</span><span class="token punctuation">:</span> <span class="token string">"#008069"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="source--sourcehandle-patterns">3. <code>source</code> / <code>sourceHandle</code> Patterns</h2>
<p>Below are the patterns for <code>source</code> and <code>sourceHandle</code> depending on where the edge originates.</p>
<blockquote>
<p>In all cases:<br>
<code>target = &lt;target node id&gt;</code><br>
<code>type</code>, <code>markerEnd</code>, <code>animated</code>, <code>style</code> remain constant as above.</p>
</blockquote>
<h3 id="keyword-node">3.1 Keyword Node</h3>
<ul>
<li>
<p><strong>Main edge coming out from keyword block</strong>:</p>
<ul>
<li><code>source = "keyword"</code></li>
<li><code>sourceHandle = "keyword-right-keyword"</code></li>
</ul>
</li>
</ul>
<blockquote>
<p>Only for keyword node the <code>source</code> is literally <code>"keyword"</code>.<br>
For all other nodes it is the <strong>node id</strong> (timestamp-like).</p>
</blockquote>
<ul>
<li><strong>edge coming out from quick reply button from template in keyword node</strong>:
<ul>
<li><code>source = "keyword"</code></li>
<li><code>sourceHandle = "Click_here:--:691f1b396cd9150d5bed705f"</code></li>
<li><code>Format for sourceHandle is "&lt;quick_reply_btn_text(with all buttons concatenated using underscore)&gt;:-:&lt;templateMongoId&gt;"</code></li>
<li>For eg: for above example the text of quick reply button was <code>Click here</code>.</li>
</ul>
</li>
</ul>
<h3 id="buttons-inside-message-with-button-node">3.2 Buttons (inside message-with-button node)</h3>
<ul>
<li>
<p>Pattern:<br>
<code>source = &lt;node id&gt; sourceHandle = message_with_button-right-&lt;node id&gt;-&lt;button id&gt;</code></p>
</li>
<li>
<p>Example:<br>
<code>message_with_button-right-1763581453582-1763582120536</code></p>
</li>
</ul>
<h3 id="after-timeout-button">3.3 After Timeout Button</h3>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = component-right-timeout-&lt;node id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>component-right-timeout-1763581453582</code></p>
</li>
</ul>
<h3 id="edge-from-a-list-item-list-message-node">3.4 Edge from a List Item (List Message Node)</h3>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = list_message-right-&lt;node id&gt;-&lt;section idx&gt;-&lt;item id&gt;-|&lt;flow id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>list_message-right-1763582376784-0-1763582383395-|691dad1e1323ae0c615826ee</code></p>
</li>
</ul>
<h3 id="whatsapp-forms">3.5 WhatsApp Forms</h3>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = whatsapp-forms-&lt;node id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>whatsapp-forms-1763582460116</code></p>
</li>
</ul>
<h3 id="conversion-api-node">3.6 Conversion API Node</h3>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = set-conversion-right-&lt;node id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>set-conversion-right-1763582528450</code></p>
</li>
</ul>
<h3 id="condition-node">3.7 Condition Node</h3>
<p>Two possible outgoing edges: <strong>true</strong> and <strong>false</strong> branches.</p>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle (true branch) = condition-right-true-&lt;node id&gt; sourceHandle (false branch) = condition-right-false-&lt;node id&gt;</code></p>
</li>
<li>
<p>Examples:</p>
<p><code>condition-right-true-1763582570764 condition-right-false-1763582570764</code></p>
</li>
</ul>
<h3 id="add-tag--connect-flow">3.8 Add Tag &amp; Connect Flow</h3>
<p>They share the same-style handle:</p>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = add-tag-right-&lt;node id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>add-tag-right-1763582717832</code></p>
</li>
</ul>
<h3 id="ask-address-node">3.9 Ask Address Node</h3>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = question-address-message-right-&lt;node id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>question-address-message-right-1763582818086</code></p>
</li>
</ul>
<h3 id="ask-location-node">3.10 Ask Location Node</h3>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = question-location-message-right-&lt;node id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>question-location-message-right-1763582860953</code></p>
</li>
</ul>
<h3 id="ask-question-node-textnumberdateetc.">3.11 Ask Question Node (Text/Number/Date/etc.)</h3>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = question-right-&lt;node id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>question-right-1763582863552</code></p>
</li>
</ul>
<h3 id="ask-media-question-node">3.12 Ask Media Question Node</h3>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = question-media-right-&lt;node id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>question-media-right-1763582901490</code></p>
</li>
</ul>
<h3 id="set-a-variable-set-attribute-node">3.13 Set a Variable (Set Attribute Node)</h3>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = set-a-varibale-right-&lt;node id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>set-a-varibale-right-1763582985492</code></p>
</li>
</ul>
<blockquote>
<p>Note: spelling is <strong><code>varibale</code></strong> in the handle, matching your current implementation.</p>
</blockquote>
<h3 id="api-request-node-setupwebhook">3.14 API Request Node (<code>setupWebhook</code>)</h3>
<p>Two kinds of edges:</p>
<ol>
<li>
<p><strong>Custom status code branch</strong></p>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = setup-webhoook-right-&lt;node id&gt;-&lt;status code id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>setup-webhoook-right-1763583037952-1763583049579</code></p>
</li>
</ul>
</li>
<li>
<p><strong>Status fallback / default branch</strong></p>
<ul>
<li>
<p>Pattern:</p>
<p><code>source = &lt;node id&gt; sourceHandle = setup-webhoook-right-&lt;node id&gt;</code></p>
</li>
<li>
<p>Example:</p>
<p><code>setup-webhoook-right-1763583037952</code></p>
</li>
</ul>
</li>
</ol>
<blockquote>
<p>Note: handle uses <strong><code>webhoook</code></strong> (3 o’s), matching your current naming.</p>
</blockquote>

