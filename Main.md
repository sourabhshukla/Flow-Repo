---


---

<h1 id="flow-update-api-–-main-curl">Flow Update API – Main cURL</h1>
<p>This API is used to <strong>create or update a flow</strong> for a given project.</p>
<p>It sends:</p>
<ul>
<li><code>projectId</code> → the project to which the flow belongs</li>
<li><code>flowId</code> → the specific flow being updated</li>
<li><code>flow</code> → full React Flow–style graph (<code>nodes</code> + <code>edges</code>)</li>
<li><code>flowName</code> → human-readable name of the flow</li>
<li><code>status</code> → whether the flow is active/enabled</li>
</ul>
<hr>
<h2 id="curl-request">1. cURL Request</h2>
<pre class=" language-bash"><code class="prism  language-bash">curl --location <span class="token string">'&lt;BASE_URL&gt;/client/t1/project-apis/v2/project/flow/create'</span> \
--header <span class="token string">'Content-Type: application/json'</span> \
--data <span class="token string">'{
  "projectId": "68ac67dc9a630835f9ac7601",
  "flowName": "Dummy Flow"
}'</span>
</code></pre>
<h2 id="curl-request-update">2. cURL Request (update)</h2>
<pre class=" language-bash"><code class="prism  language-bash">curl --location <span class="token string">'&lt;BASE_URL&gt;/client/t1/project-apis/v2/project/68ac67dc9a630835f9ac7601/flow/update'</span> \
--header <span class="token string">'Content-Type: application/json'</span> \
--data <span class="token string">'{
  "projectId": "68ac67dc9a630835f9ac7601",
  "flowId": "68ff9d6da67048001e402b3b",
  "flow": {
    "nodes": [
      {
        "id": "keyword",
        "type": "keywordBox",
        "data": {
          "label": "Node 1",
          "text": "Add keywords to start chat ",
          "keywords": [
            "hii",
            "hello"
          ],
          "templates": [],
          "qrCampaigns": [],
          "ad": null,
          "regexCaseSensitive": true,
          "isNewFlow": true,
          "regex": "*a"
        },
        "position": {
          "x": -1262.4900259419146,
          "y": 595.4498502174376
        },
        "positionAbsolute": {
          "x": -1214.4358850032481,
          "y": -395.28339594357766
        }
      }
    ],
    "edges": []
  },
  "flowName": "Untitled",
  "status": true
}'</span>
</code></pre>

