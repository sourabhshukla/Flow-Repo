---


---

<h1 id="multi-product-message-node-multiproductmessage">Multi Product Message Node (<code>multiProductMessage</code>)</h1>
<p>This node is used to send a <strong>multi-product message from a Meta (WhatsApp) catalog</strong>, where products are grouped into one or more <strong>sections</strong>.</p>
<p>It includes:</p>
<ul>
<li>A shared <strong>catalogueId</strong></li>
<li>Overall <strong>header</strong>, <strong>body</strong>, <strong>footer</strong></li>
<li>One or more <strong>sections</strong>, each with a title and product list</li>
<li>A <strong>buttonTitle</strong> shown as the main CTA (e.g. “View Items”)</li>
</ul>
<hr>
<h2 id="json-structure">JSON Structure</h2>
<pre class=" language-jsonc"><code class="prism  language-jsonc">{
  // Unique identifier for this node on the canvas
  "id": "1763580244198",

  // Wrapper node type
  "type": "masterComponent",

  "data": {
    // Whether this node is draggable in the editor UI
    "isDrag": true,

    // Logical ID of this component
    "id": "1763580244198",

    "content": [
      {
        // Unique ID for this multi-product block
        "id": "1763580244198-multiProductMessage",

        // Node type for multi-product catalog messages
        "type": "multiProductMessage",

        "data": {
          // Top header text for the multi-product message
          "header": "Header",

          // Main body/description text
          "body": "Body",

          // Footer text shown below the list
          "footer": "Footer",

          // Meta Catalogue ID from which all products are fetched
          "catalogueId": "4017973368513731",

          // Total number of products across all sections
          "productsCount": 3,

          // Number of sections in this message
          "sectionsCount": 2,

          // Sections that group products logically
          "sections": [
            {
              // Section title shown to the user
              "title": "Section 1",

              // Products inside this section
              "products": [
                {
                  "title": "product 6",
                  "price": "₹220.00",
                  "thumbnail": "https://scontent-bom5-1.xx.fbcdn.net/v/t45.5328-4/534414025_787317317101084_3145013199575488083_n.jpg?_nc_cat=111&amp;ccb=1-7&amp;_nc_sid=c7e7b7&amp;_nc_ohc=e4o5xzu29rwQ7kNvwHH0u1g&amp;_nc_oc=Adm090CiXfqOzKJAWSZOUXo3jvJiMakK7sixbLChTW7WDfDIkky8Ewh2i4d1JjiReMA&amp;_nc_zt=23&amp;_nc_ht=scontent-bom5-1.xx&amp;edm=ANyJclEEAAAA&amp;_nc_gid=JvGnfFtAuYQT1tmeTq0gxg&amp;_nc_tpa=Q5bMBQEkXJfc9Q7jvjq_fLJzwMAWdUZENu_mnlQTfQXmoPi2def7GunNGRueUUi5Jh2vM3GKXf7aVb8s&amp;oh=00_AfiUJ_sK66HxkYQLgwa40WQpb2axIbDGwA31Ml4X4U1_HA&amp;oe=69238FA0",

                  // Product ID as defined by the retailer in Meta catalog
                  "retailerId": "k64k21xnye",

                  // Catalogue ID this product belongs to
                  "catalogueId": "4017973368513731"
                },
                {
                  "title": "product 5",
                  "price": "₹180.00",
                  "thumbnail": "https://scontent-bom5-1.xx.fbcdn.net/v/t45.5328-4/534414025_787317317101084_3145013199575488083_n.jpg?_nc_cat=111&amp;ccb=1-7&amp;_nc_sid=c7e7b7&amp;_nc_ohc=e4o5xzu29rwQ7kNvwHH0u1g&amp;_nc_oc=Adm090CiXfqOzKJAWSZOUXo3jvJiMakK7sixbLChTW7WDfDIkky8Ewh2i4d1JjiReMA&amp;_nc_zt=23&amp;_nc_ht=scontent-bom5-1.xx&amp;edm=ANyJclEEAAAA&amp;_nc_gid=JvGnfFtAuYQT1tmeTq0gxg&amp;_nc_tpa=Q5bMBQFVbBOnAGq79Ib37pN3vsdsZtmc9WYQzrwQYVsPftKj_mjbqmX4SIsd9TWJ4inF7u_93JnLf7sw&amp;oh=00_AfjLWTqt1R6jFrc8nVWdbDxWkrfywxu29hYSV4htvd2xJw&amp;oe=69238FA0",
                  "retailerId": "is67cqf3zf",
                  "catalogueId": "4017973368513731"
                }
              ]
            },
            {
              "title": "Section 2",
              "products": [
                {
                  "title": "product 6",
                  "price": "₹220.00",
                  "thumbnail": "https://scontent-bom5-1.xx.fbcdn.net/v/t45.5328-4/534414025_787317317101084_3145013199575488083_n.jpg?_nc_cat=111&amp;ccb=1-7&amp;_nc_sid=c7e7b7&amp;_nc_ohc=e4o5xzu29rwQ7kNvwHH0u1g&amp;_nc_oc=Adm090CiXfqOzKJAWSZOUXo3jvJiMakK7sixbLChTW7WDfDIkky8Ewh2i4d1JjiReMA&amp;_nc_zt=23&amp;_nc_ht=scontent-bom5-1.xx&amp;edm=ANyJclEEAAAA&amp;_nc_gid=JvGnfFtAuYQT1tmeTq0gxg&amp;_nc_tpa=Q5bMBQEkXJfc9Q7jvjq_fLJzwMAWdUZENu_mnlQTfQXmoPi2def7GunNGRueUUi5Jh2vM3GKXf7aVb8s&amp;oh=00_AfiUJ_sK66HxkYQLgwa40WQpb2axIbDGwA31Ml4X4U1_HA&amp;oe=69238FA0",
                  "retailerId": "k64k21xnye",
                  "catalogueId": "4017973368513731"
                }
              ]
            }
          ],

          // Button label shown in the WhatsApp UI for the multi-product list
          "buttonTitle": "View Items"
        }
      }
    ]
  },

  // Position of this node on the canvas
  "position": {
    "x": -56.5,
    "y": 303.5
  }
}
</code></pre>
<hr>
<h2 id="clean-json">Clean JSON</h2>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
  <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763580244198"</span><span class="token punctuation">,</span>
  <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"masterComponent"</span><span class="token punctuation">,</span>
  <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"isDrag"</span><span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763580244198"</span><span class="token punctuation">,</span>
    <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token string">"1763580244198-multiProductMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token string">"multiProductMessage"</span><span class="token punctuation">,</span>
        <span class="token string">"data"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
          <span class="token string">"header"</span><span class="token punctuation">:</span> <span class="token string">"Header"</span><span class="token punctuation">,</span>
          <span class="token string">"body"</span><span class="token punctuation">:</span> <span class="token string">"Body"</span><span class="token punctuation">,</span>
          <span class="token string">"footer"</span><span class="token punctuation">:</span> <span class="token string">"Footer"</span><span class="token punctuation">,</span>
          <span class="token string">"catalogueId"</span><span class="token punctuation">:</span> <span class="token string">"4017973368513731"</span><span class="token punctuation">,</span>
          <span class="token string">"productsCount"</span><span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span>
          <span class="token string">"sectionsCount"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
          <span class="token string">"sections"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
            <span class="token punctuation">{</span>
              <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"Section 1"</span><span class="token punctuation">,</span>
              <span class="token string">"products"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token punctuation">{</span>
                  <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"product 6"</span><span class="token punctuation">,</span>
                  <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token string">"₹220.00"</span><span class="token punctuation">,</span>
                  <span class="token string">"thumbnail"</span><span class="token punctuation">:</span> <span class="token string">"https://scontent-bom5-1.xx.fbcdn.net/v/t45.5328-4/534414025_787317317101084_3145013199575488083_n.jpg?_nc_cat=111&amp;ccb=1-7&amp;_nc_sid=c7e7b7&amp;_nc_ohc=e4o5xzu29rwQ7kNvwHH0u1g&amp;_nc_oc=Adm090CiXfqOzKJAWSZOUXo3jvJiMakK7sixbLChTW7WDfDIkky8Ewh2i4d1JjiReMA&amp;_nc_zt=23&amp;_nc_ht=scontent-bom5-1.xx&amp;edm=ANyJclEEAAAA&amp;_nc_gid=JvGnfFtAuYQT1tmeTq0gxg&amp;_nc_tpa=Q5bMBQEkXJfc9Q7jvjq_fLJzwMAWdUZENu_mnlQTfQXmoPi2def7GunNGRueUUi5Jh2vM3GKXf7aVb8s&amp;oh=00_AfiUJ_sK66HxkYQLgwa40WQpb2axIbDGwA31Ml4X4U1_HA&amp;oe=69238FA0"</span><span class="token punctuation">,</span>
                  <span class="token string">"retailerId"</span><span class="token punctuation">:</span> <span class="token string">"k64k21xnye"</span><span class="token punctuation">,</span>
                  <span class="token string">"catalogueId"</span><span class="token punctuation">:</span> <span class="token string">"4017973368513731"</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token punctuation">{</span>
                  <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"product 5"</span><span class="token punctuation">,</span>
                  <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token string">"₹180.00"</span><span class="token punctuation">,</span>
                  <span class="token string">"thumbnail"</span><span class="token punctuation">:</span> <span class="token string">"https://scontent-bom5-1.xx.fbcdn.net/v/t45.5328-4/534414025_787317317101084_3145013199575488083_n.jpg?_nc_cat=111&amp;ccb=1-7&amp;_nc_sid=c7e7b7&amp;_nc_ohc=e4o5xzu29rwQ7kNvwHH0u1g&amp;_nc_oc=Adm090CiXfqOzKJAWSZOUXo3jvJiMakK7sixbLChTW7WDfDIkky8Ewh2i4d1JjiReMA&amp;_nc_zt=23&amp;_nc_ht=scontent-bom5-1.xx&amp;edm=ANyJclEEAAAA&amp;_nc_gid=JvGnfFtAuYQT1tmeTq0gxg&amp;_nc_tpa=Q5bMBQFVbBOnAGq79Ib37pN3vsdsZtmc9WYQzrwQYVsPftKj_mjbqmX4SIsd9TWJ4inF7u_93JnLf7sw&amp;oh=00_AfjLWTqt1R6jFrc8nVWdbDxWkrfywxu29hYSV4htvd2xJw&amp;oe=69238FA0"</span><span class="token punctuation">,</span>
                  <span class="token string">"retailerId"</span><span class="token punctuation">:</span> <span class="token string">"is67cqf3zf"</span><span class="token punctuation">,</span>
                  <span class="token string">"catalogueId"</span><span class="token punctuation">:</span> <span class="token string">"4017973368513731"</span>
                <span class="token punctuation">}</span>
              <span class="token punctuation">]</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>
              <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"Section 2"</span><span class="token punctuation">,</span>
              <span class="token string">"products"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token punctuation">{</span>
                  <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"product 6"</span><span class="token punctuation">,</span>
                  <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token string">"₹220.00"</span><span class="token punctuation">,</span>
                  <span class="token string">"thumbnail"</span><span class="token punctuation">:</span> <span class="token string">"https://scontent-bom5-1.xx.fbcdn.net/v/t45.5328-4/534414025_787317317101084_3145013199575488083_n.jpg?_nc_cat=111&amp;ccb=1-7&amp;_nc_sid=c7e7b7&amp;_nc_ohc=e4o5xzu29rwQ7kNvwHH0u1g&amp;_nc_oc=Adm090CiXfqOzKJAWSZOUXo3jvJiMakK7sixbLChTW7WDfDIkky8Ewh2i4d1JjiReMA&amp;_nc_zt=23&amp;_nc_ht=scontent-bom5-1.xx&amp;edm=ANyJclEEAAAA&amp;_nc_gid=JvGnfFtAuYQT1tmeTq0gxg&amp;_nc_tpa=Q5bMBQEkXJfc9Q7jvjq_fLJzwMAWdUZENu_mnlQTfQXmoPi2def7GunNGRueUUi5Jh2vM3GKXf7aVb8s&amp;oh=00_AfiUJ_sK66HxkYQLgwa40WQpb2axIbDGwA31Ml4X4U1_HA&amp;oe=69238FA0"</span><span class="token punctuation">,</span>
                  <span class="token string">"retailerId"</span><span class="token punctuation">:</span> <span class="token string">"k64k21xnye"</span><span class="token punctuation">,</span>
                  <span class="token string">"catalogueId"</span><span class="token punctuation">:</span> <span class="token string">"4017973368513731"</span>
                <span class="token punctuation">}</span>
              <span class="token punctuation">]</span>
            <span class="token punctuation">}</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token string">"buttonTitle"</span><span class="token punctuation">:</span> <span class="token string">"View Items"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token string">"position"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
    <span class="token string">"x"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">56.5</span><span class="token punctuation">,</span>
    <span class="token string">"y"</span><span class="token punctuation">:</span> <span class="token number">303.5</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>

