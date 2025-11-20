---


---

<h1 id="single-product-message-node-singleproductmessage">Single Product Message Node (<code>singleProductMessage</code>)</h1>
<p>This node is used to send a <strong>single product message from a Meta (Facebook/WhatsApp) catalog</strong>.</p>
<p>It contains:</p>
<ul>
<li>A <strong>product object</strong> (coming from the Meta catalog)</li>
<li>Optional <strong>body</strong> and <strong>footer</strong> text shown in the message</li>
</ul>
<hr>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763580061113",

  // Wrapper node type
  "type": "masterComponent",

  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Logical ID of the component (usually same as node id)
    "id": "1763580061113",

    // Content blocks inside this masterComponent
    "content": [
      {
        // Unique ID for this single product block
        "id": "1763580061113-singleProductMessage",

        // Node type for single product messages
        "type": "singleProductMessage",

        "data": {
          // Product information coming from the Meta catalog
          "product": {
            // Product title as shown to the user
            "title": "product 6",

            // Display price (formatted as shown in catalog)
            "price": "₹220.00",

            // Thumbnail URL of the product image (from Meta)
            "thumbnail": "https://scontent-bom5-1.xx.fbcdn.net/v/t45.5328-4/534414025_787317317101084_3145013199575488083_n.jpg?_nc_cat=111&amp;ccb=1-7&amp;_nc_sid=c7e7b7&amp;_nc_ohc=e4o5xzu29rwQ7kNvwHH0u1g&amp;_nc_oc=Adm090CiXfqOzKJAWSZOUXo3jvJiMakK7sixbLChTW7WDfDIkky8Ewh2i4d1JjiReMA&amp;_nc_zt=23&amp;_nc_ht=scontent-bom5-1.xx&amp;edm=ANyJclEEAAAA&amp;_nc_gid=JvGnfFtAuYQT1tmeTq0gxg&amp;_nc_tpa=Q5bMBQEkXJfc9Q7jvjq_fLJzwMAWdUZENu_mnlQTfQXmoPi2def7GunNGRueUUi5Jh2vM3GKXf7aVb8s&amp;oh=00_AfiUJ_sK66HxkYQLgwa40WQpb2axIbDGwA31Ml4X4U1_HA&amp;oe=69238FA0",

            // Retailer-specific product ID (as configured in the catalog)
            "retailerId": "k64k21xnye",

            // Meta catalogue ID this product belongs to
            "catalogueId": "4017973368513731"
          },

          // Optional body text shown with the product message
          "body": "body",

          // Optional footer text shown below the product message
          "footer": "footer"
        }
      }
    ]
  },

  // Position of this node on the flow canvas
  "position": {
    "x": -182.5,
    "y": 114.5
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763580061113"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763580061113"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763580061113-singleProductMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"singleProductMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"product"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
            <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"product 6"</span><span class="token punctuation">,</span>
            <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token string">"₹220.00"</span><span class="token punctuation">,</span>
            <span class="token string">"thumbnail"</span><span class="token punctuation">:</span> <span class="token string">"https://scontent-bom5-1.xx.fbcdn.net/v/t45.5328-4/534414025_787317317101084_3145013199575488083_n.jpg?_nc_cat=111&amp;ccb=1-7&amp;_nc_sid=c7e7b7&amp;_nc_ohc=e4o5xzu29rwQ7kNvwHH0u1g&amp;_nc_oc=Adm090CiXfqOzKJAWSZOUXo3jvJiMakK7sixbLChTW7WDfDIkky8Ewh2i4d1JjiReMA&amp;_nc_zt=23&amp;_nc_ht=scontent-bom5-1.xx&amp;edm=ANyJclEEAAAA&amp;_nc_gid=JvGnfFtAuYQT1tmeTq0gxg&amp;_nc_tpa=Q5bMBQEkXJfc9Q7jvjq_fLJzwMAWdUZENu_mnlQTfQXmoPi2def7GunNGRueUUi5Jh2vM3GKXf7aVb8s&amp;oh=00_AfiUJ_sK66HxkYQLgwa40WQpb2axIbDGwA31Ml4X4U1_HA&amp;oe=69238FA0"</span><span class="token punctuation">,</span>
            <span class="token string">"retailerId"</span><span class="token punctuation">:</span> <span class="token string">"k64k21xnye"</span><span class="token punctuation">,</span>
            <span class="token string">"catalogueId"</span><span class="token punctuation">:</span> <span class="token string">"4017973368513731"</span>
          <span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token string">"body"</span><span class="token punctuation">:</span> <span class="token string">"body"</span><span class="token punctuation">,</span>
          <span class="token string">"footer"</span><span class="token punctuation">:</span> <span class="token string">"footer"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">182.5</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token number">114.5</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

