---


---

<h1 id="question-node-questionmessage">Question Node (<code>questionMessage</code>)</h1>
<p>This node is used to <strong>ask a question</strong>, validate the user’s answer, and store it in an attribute.</p>
<p>Supported <code>attributeFormat</code> values:</p>
<ul>
<li><code>Any</code></li>
<li><code>Text</code></li>
<li><code>Number</code></li>
<li><code>Date</code></li>
<li><code>True/False</code></li>
<li><code>Email</code></li>
<li><code>Regex</code></li>
</ul>
<hr>
<h2 id="field-overview">Field Overview</h2>
<h3 id="core-fields">Core fields</h3>
<ul>
<li><code>text</code>: Question text shown to the user.</li>
<li><code>attribute</code>: Attribute name where the final (valid) answer will be stored.</li>
<li><code>attributeNumberOfAttempt</code>: Maximum number of validation attempts (stringified integer).</li>
<li><code>attributeFormat</code>: Validation type (<code>Any</code>, <code>Text</code>, <code>Number</code>, <code>Date</code>, <code>True/False</code>, <code>Email</code>, <code>Regex</code>).</li>
<li><code>attributeFormatValue</code>: Object with extra validation options:
<ul>
<li><code>min</code>: Used mainly for <code>Number</code> (min value), or reserved for other future uses.</li>
<li><code>max</code>: Used mainly for <code>Number</code> (max value), or reserved for other future uses.</li>
<li><code>regex</code>: Used for <code>Regex</code> format (custom regex).</li>
</ul>
</li>
<li><code>attributeFormatValidationErrorMessage</code>: Error text shown when validation fails.</li>
<li><code>mediaType</code>: Reserved for attaching/expecting media answers (currently empty in samples).</li>
<li><code>timeoutToggle</code>: Enables/disables timeout behavior.</li>
<li><code>delay</code>: <strong>Seconds</strong> before sending the question.</li>
<li><code>time</code>: <strong>Minutes</strong> before timeout when <code>timeoutToggle</code> is <code>true</code>.</li>
</ul>
<hr>
<h2 id="format-specific-behavior-conceptual">Format-specific behavior (conceptual)</h2>

<table>
<thead>
<tr>
<th><code>attributeFormat</code></th>
<th>Meaning / validation</th>
<th>Uses <code>min/max</code>?</th>
<th>Uses <code>regex</code>?</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Any</code></td>
<td>Accept any input (no extra validation)</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<td><code>Text</code></td>
<td>Accept any text, can be combined with custom rules later</td>
<td>Typically no</td>
<td>No</td>
</tr>
<tr>
<td><code>Number</code></td>
<td>Only numeric; <code>min</code>/<code>max</code> define allowed numeric range</td>
<td><strong>Yes (numeric range)</strong></td>
<td>No</td>
</tr>
<tr>
<td><code>Date</code></td>
<td>Date value; <code>min</code>/<code>max</code> can be used as date range (optional)</td>
<td>Possibly (date range)</td>
<td>No</td>
</tr>
<tr>
<td><code>True/False</code></td>
<td>Boolean-like values (yes/no, true/false, etc.)</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<td><code>Email</code></td>
<td>Should be a valid email address</td>
<td>No</td>
<td>No (internal regex)</td>
</tr>
<tr>
<td><code>Regex</code></td>
<td>Answer must match custom regex in <code>attributeFormatValue.regex</code></td>
<td>No</td>
<td><strong>Yes</strong></td>
</tr>
</tbody>
</table><hr>
<h2 id="generic-question-node">Generic Question Node</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763576969102",

  // Node type - masterComponent wrapper
  "type": "masterComponent",

  "data": {
    // Node is draggable in the editor
    "isDrag": true,

    // Logical ID of the component (usually same as node id)
    "id": "1763576969102",

    "content": [
      {
        // Unique ID for this question block
        "id": "1763576969102-questionMessage",

        // Question node type
        "type": "questionMessage",

        "data": {
          // Question text shown to the user
          "text": "What country are you from ?",

          // Attribute key where the validated response will be stored
          "attribute": "Country",

          // Maximum number of validation attempts (stringified integer)
          // e.g. "1", "3"
          "attributeNumberOfAttempt": "1",

          // Extra validation config (depends on attributeFormat)
          "attributeFormatValue": {
            // For Number: minimum allowed value (string)
            // For Date: can be used as min date (if implemented)
            "min": "",

            // For Number: maximum allowed value (string)
            // For Date: can be used as max date (if implemented)
            "max": "",

            // For Regex: the regex pattern that must be matched
            "regex": ""
          },

          // Error message shown when validation fails.
          // Empty string means no custom message.
          "attributeFormatValidationErrorMessage": "",

          // Validation type:
          // "Any" | "Text" | "Number" | "Date" | "True/False" | "Email" | "Regex"
          "attributeFormat": "Any",

          // Reserved for cases where the answer involves media.
          // Empty in current examples.
          "mediaType": "",

          // When true, timeout behavior is enabled using `time`
          "timeoutToggle": true,

          // Delay before sending this question
          // UNIT: SECONDS
          "delay": "10",

          // Timeout duration (after message is sent)
          // UNIT: MINUTES
          "time": "2"
        }
      }
    ]
  },

  // Position of this node on the canvas
  "position": {
    "x": -920.9101980181649,
    "y": -314.97126575298853
  }
}
</code></pre>
<hr>
<h2 id="json-examples-per-attributeformat">JSON Examples (per <code>attributeFormat</code>)</h2>
<h3 id="any">1. <code>Any</code></h3>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576969102"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576969102"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763576969102-questionMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"questionMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"What country are you from ?"</span><span class="token punctuation">,</span>
          <span class="token string">"attribute"</span><span class="token punctuation">:</span> <span class="token string">"Country"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeNumberOfAttempt"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValue"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
            <span class="token string">"min"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"max"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"regex"</span><span class="token punctuation">:</span> <span class="token string">""</span>
          <span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormatValidationErrorMessage"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"attributeFormat"</span><span class="token punctuation">:</span> <span class="token string">"Any"</span><span class="token punctuation">,</span>
          <span class="token string">"mediaType"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
          <span class="token string">"timeoutToggle"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token string">"delay"</span><span class="token punctuation">:</span> <span class="token string">"10"</span><span class="token punctuation">,</span>
          <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"2"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">920.9101980181649</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">314.97126575298853</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

