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
        "status": "APPROVED",
        "processed": "2023-12-30T15:08:41.854Z",
        "callToAction": [],
        "quickReplies": [
          "Continue Chat"
        ],
        "templateParams": [],
        "_id": "65903279d094513802a87230",
        "label": "welcome_new",
        "category": "UTILITY",
        "type": "TEXT",
        "name": "welcome_new",

        // Full template format string (with inline buttons specified)
        "format": "Hi there, 👋\n\nWelcome to AiSensy.\n\nClick the button below to continue the Chat 👇 | [Continue Chat]",

        // Example message preview without the button metadata
        "sampleMessage": "Hi there, 👋\n\nWelcome to AiSensy.\n\nClick the button below to continue the Chat 👇",

        // How user interacts with this template ("QuickReplies", "CallToAction", etc.)
        "actionType": "QuickReplies",

        "sampleMediaUrl": "",
        "sampleCTAUrl": "",
        "isClickTrackingEnabled": false,

        // Optional header text for the template
        "headerText": "AiSensy",

        "buttons": [],
        "parameters": 0,
        "namespace": "34a3dddc_9ebd_4556_80a8_418ed6be917c",
        "templateId": "1046615053216990",
        "templateLanguage": "English",
        "assistantId": "633829cd86fc494a463d86e8",
        "clientId": "63029c7285871851a4932f58",
        "assistantName": "customer_support",
        "partnerId": null,
        "carouselCards": [],
        "createdAt": "2023-12-30T15:08:41.860Z",
        "updatedAt": "2025-10-30T12:59:43.938Z",
        "__v": 0,
        "quality": "UNKNOWN",
        "rejectedReason": "NONE"
      },
      {
        "status": "APPROVED",
        "processed": "2023-05-31T08:25:32.292Z",
        "callToAction": [],
        "quickReplies": [
          "Thank You",
          "Have a nice day"
        ],
        "templateParams": [],
        "_id": "6477047c8aac7f7df929e73e",
        "label": "test_hs_5",
        "category": "MARKETING",
        "type": "VIDEO",
        "name": "test_hs_5",
        "format": "*Get Exclusive Access to Exciting Offers*\n\nWith Flipkart Axis Bank Credit Card\n\n*Get 5% Unlimited Cashbacks* on\n\n--Latest Mobile phones\n--Trending Styles\n--BRAND New Home &amp; kitchen Appliances\n\nClick here to apply : https://www.flipkart.com/\n\nClick here to start Shopping: https://www.flipkart.com/ | [Thank You] | [Have a nice day]",
        "sampleMessage": "*Get Exclusive Access to Exciting Offers*\n\nWith Flipkart Axis Bank Credit Card\n\n*Get 5% Unlimited Cashbacks* on\n\n--Latest Mobile phones\n--Trending Styles\n--BRAND New Home &amp; kitchen Appliances\n\nClick here to apply : https://www.flipkart.com/\n\nClick here to start Shopping: https://www.flipkart.com/",
        "actionType": "QuickReplies",
        "sampleMediaUrl": "4::dmlkZW8vbXA0:ARbt6U... (truncated)",
        "sampleCTAUrl": "",
        "isClickTrackingEnabled": false,
        "footerText": "Reply *STOP* to Unsubscribe",
        "parameters": 0,
        "namespace": "34a3dddc_9ebd_4556_80a8_418ed6be917c",
        "templateId": "790325912453662",
        "templateLanguage": "English (UK)",
        "assistantId": "633829cd86fc494a463d86e8",
        "clientId": "63029c7285871851a4932f58",
        "assistantName": "customer_support",
        "partnerId": null,
        "createdAt": "2023-05-31T08:25:32.300Z",
        "updatedAt": "2025-10-30T12:59:43.938Z",
        "__v": 0,
        "rejectedReason": "NONE",
        "quality": "UNKNOWN",
        "buttons": [],
        "carouselCards": []
      }
    ],

    // QR-based campaigns that can map to this flow entry point
    "qrCampaigns": [],

    // Linked ad configuration (if this keyword node is bound to an ad entry)
    "ad": null,

    // When true, regex matching is case-sensitive
    "regexCaseSensitive": true,

    // Whether this node represents a newly created flow entry in the editor
    "isNewFlow": true,

    // Optional regex pattern for matching messages
    // If provided, engine can use this along with or instead of simple keywords.
    "regex": "*a"
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
    <span class="token string">"qrCampaigns"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token string">"ad"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
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

