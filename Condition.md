---


---

<h1 id="condition-node-condition">Condition Node (<code>condition</code>)</h1>
<p>The <strong>Condition Node</strong> is used to branch the flow based on attributes, time, or date.</p>
<p>Supported condition types:</p>
<ol>
<li><strong>Equal</strong> → <code>conditionKey: "equal"</code></li>
<li><strong>Exists</strong> → <code>conditionKey: "exists"</code></li>
<li><strong>Time In</strong> → <code>conditionKey: "time_in"</code></li>
<li><strong>Date In</strong> → <code>conditionKey: "date_in"</code></li>
</ol>
<h3 id="field-usage-rules">Field usage rules</h3>

<table>
<thead>
<tr>
<th>Condition Type</th>
<th>attributeOne</th>
<th>attributeTwo</th>
<th>rangeObject</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Equal</strong></td>
<td>Value/attribute to compare</td>
<td>Used (RHS of comparison)</td>
<td>Not used</td>
</tr>
<tr>
<td><strong>Exists</strong></td>
<td>Attribute being checked for presence</td>
<td><strong>Ignored</strong> (<code>""</code>)</td>
<td>Not used</td>
</tr>
<tr>
<td><strong>Time In</strong></td>
<td><strong>Time string in <code>hh:mm</code> UTC format</strong></td>
<td><strong>Ignored</strong></td>
<td>May hold future time-range data</td>
</tr>
<tr>
<td><strong>Date In</strong></td>
<td><strong>Date string in <code>mm-dd-yyyy</code> UTC format</strong></td>
<td><strong>Ignored</strong></td>
<td>May hold future date-range data</td>
</tr>
</tbody>
</table><h3 id="format-requirements">Format Requirements</h3>
<h4 id="time-in">Time In</h4>
<p><code>attributeOne</code> <strong>must be in:</strong></p>
<p>Examples:<br>
<code>"09:30"</code>, <code>"18:05"</code></p>
<h4 id="date-in">Date In</h4>
<p><code>attributeOne</code> <strong>must be in:</strong></p>
<p>Examples:<br>
<code>"01-15-2025"</code>, <code>"12-31-2025"</code></p>
<hr>
<h2 id="updated-generic-condition-node-with-comments">Updated Generic Condition Node (with comments)</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  "id": "1763574255070",
  "type": "masterComponent",
  "data": {
    "isDrag": true,
    "id": "1763574255070",
    "content": [
      {
        "id": "1763574255070-condition",
        "type": "condition",
        "data": {
          // Type of condition:
          // "Equal" | "Exists" | "Time In" | "Date In"
          "condition": "Time In",

          // attributeOne rules:
          // - For "Equal": value/attribute to compare
          // - For "Exists": attribute to check
          // - For "Time In": MUST be in "hh:mm" format (24-hr, UTC Standard)
          // - For "Date In": MUST be in "mm-dd-yyyy" format (UTC Standard)
          "attributeOne": "09:30",

          // attributeTwo usage:
          // - Used ONLY for "Equal"
          // - For all other conditions: MUST be empty ""
          "attributeTwo": "",

          // Reserved for future time/date range structure
          // Currently not used
          "rangeObject": "",

          // Internal machine key for the condition
          // "equal" | "exists" | "time_in" | "date_in"
          "conditionKey": "time_in"
        }
      }
    ]
  },

  "position": {
    "x": -939.725341796875,
    "y": -417.05743408203125
  }
}
</code></pre>
<hr>
<h2 id="json-samples">JSON samples</h2>
<h3 id="equal">Equal</h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070-condition"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"condition"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"condition"</span><span class="token punctuation">:</span> <span class="token string">"Equal"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeOne"</span><span class="token punctuation">:</span> <span class="token string">"EmbededURL"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeTwo"</span><span class="token punctuation">:</span> <span class="token string">"$IndustryKind"</span><span class="token punctuation">,</span>
          <span class="token string">"rangeObject"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"conditionKey"</span><span class="token punctuation">:</span> <span class="token string">"equal"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">939.725341796875</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">417.05743408203125</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="equal-1">Equal</h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070-condition"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"condition"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"condition"</span><span class="token punctuation">:</span> <span class="token string">"Exists"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeOne"</span><span class="token punctuation">:</span> <span class="token string">"EmbededURL"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeTwo"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"rangeObject"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"conditionKey"</span><span class="token punctuation">:</span> <span class="token string">"exists"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">939.725341796875</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">417.05743408203125</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="time-in-with-correct-format">Time In (with correct format)</h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070-condition"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"condition"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"condition"</span><span class="token punctuation">:</span> <span class="token string">"Time In"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeOne"</span><span class="token punctuation">:</span> <span class="token string">"09:30"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeTwo"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"rangeObject"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"conditionKey"</span><span class="token punctuation">:</span> <span class="token string">"time_in"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">939.725341796875</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">417.05743408203125</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="date-in-with-correct-format">Date In (with correct format)</h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763574255070-condition"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"condition"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"condition"</span><span class="token punctuation">:</span> <span class="token string">"Date In"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeOne"</span><span class="token punctuation">:</span> <span class="token string">"12-31-2025"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeTwo"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"rangeObject"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"conditionKey"</span><span class="token punctuation">:</span> <span class="token string">"date_in"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">939.725341796875</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">417.05743408203125</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>

</code></pre>

