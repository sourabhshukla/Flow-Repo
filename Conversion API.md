---


---

<h1 id="conversion-api-node-conversionapi">Conversion API Node (<code>ConversionApi</code>)</h1>
<p>This node is used to send <strong>conversion events</strong> (e.g. Purchase, Lead) to your backend / Meta Conversion API from within a flow.</p>
<p>It captures:</p>
<ul>
<li>Conversion <strong>value</strong></li>
<li><strong>Conversion type</strong> (Purchase / Lead)</li>
<li><strong>Currency code</strong> (ISO 4217 list)</li>
</ul>
<hr>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763573738905",

  // Node type - still a masterComponent
  "type": "masterComponent",

  // Node configuration and content
  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Logical ID of the component (usually same as node id)
    "id": "1763573738905",

    // Content blocks inside this node
    "content": [
      {
        // Unique ID for this specific Conversion API block
        "id": "1763573738905-ConversionApi",

        // Content type for Conversion API events
        "type": "ConversionApi",

        "data": {
          // Monetary value of the conversion.
          // Typically a stringified number. You can enforce numeric parsing in backend.
          "value": "100",

          // Type of conversion event.
          // Allowed values:
          // - "Purchase"
          // - "Lead"
          "conversionType": "Purchase",

          // ISO 4217 currency code for the conversion value.
          // Allowed values (examples):
          // "INR", "USD", "EUR", "GBP", "AED", ...
          //
          // Full allowed list:
          // [
          //   "AFN","ALL","DZD","AOA","ARS","AMD","AWG","AUD","AZN",
          //   "BSD","BHD","BDT","BBD","BYN","BZD","BMD","BTN","BOB",
          //   "BAM","BWP","BRL","GBP","BND","BGN","MMK","BIF","KHR",
          //   "CAD","CVE","KYD","XAF","XPF","CLP","CLF","CNY","COP",
          //   "KMF","CDF","CRC","HRK","CZK","DKK","DJF","DOP","XCD",
          //   "EGP","ERN","EEK","ETB","EUR","FKP","FJD","GMD","GEL",
          //   "GHS","GIP","GTQ","GNF","GYD","HTG","HNL","HKD","HUF",
          //   "ISK","INR","IDR","IQD","ILS","JMD","JPY","JOD","KZT",
          //   "KES","KRW","KWD","KGS","LAK","LVL","LBP","LSL","LRD",
          //   "LYD","LTL","MOP","MKD","MGA","MWK","MYR","MVR","MRO",
          //   "MUR","MXN","MDL","MNT","MAD","MZN","NAD","NPR","ANG",
          //   "NZD","NIO","NGN","NOK","OMR","PKR","PAB","PGK","PYG",
          //   "PEN","PHP","PLN","QAR","RON","RUB","RWF","SHP","SVC",
          //   "WST","STD","SAR","RSD","SCR","SLE","SLL","SGD","SKK",
          //   "SBD","SOS","ZAR","SSP","LKR","SRD","SZL","SEK","CHF",
          //   "TWD","TJS","TZS","THB","TOP","TTD","TND","TRY","TMT",
          //   "AED","UGX","UAH","USD","UYU","UZS","VUV","VEF","VES",
          //   "VND","XOF","YER","ZMW","ZWL","FBZ"
          // ]
          "currencyCode": "INR"
        }
      }
    ]
  },

  // Position of this node on the editor canvas
  "position": {
    "x": -906.725341796875,
    "y": -307.05743408203125
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763573738905"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763573738905"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763573738905-ConversionApi"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"ConversionApi"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"value"</span><span class="token punctuation">:</span> <span class="token string">"100"</span><span class="token punctuation">,</span>
          <span class="token string">"conversionType"</span><span class="token punctuation">:</span> <span class="token string">"Purchase"</span><span class="token punctuation">,</span>
          <span class="token string">"currencyCode"</span><span class="token punctuation">:</span> <span class="token string">"INR"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">906.725341796875</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">307.05743408203125</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>


</code></pre>

