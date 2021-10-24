---
title: short_name
slug: Mozilla/Add-ons/WebExtensions/manifest.json/short_name
tags:
  - Add-ons
  - Extensions
  - WebExtensions
browser-compat: webextensions.manifest.short_name
---
<div>{{AddonSidebar}}</div>

<table class="fullwidth-table standard-table">
 <tbody>
  <tr>
   <th scope="row">Type</th>
   <td><code>String</code></td>
  </tr>
  <tr>
   <th scope="row">Mandatory</th>
   <td>No</td>
  </tr>
  <tr>
   <th scope="row">Example</th>
   <td>
    <pre class="brush: json">
"short_name": "My Extension"</pre>
   </td>
  </tr>
 </tbody>
</table>

<p>Short name for the extension. If given, this will be used in contexts where the <a href="/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json/name">name</a> field is too long. It's recommended that the short name should not exceed 12 characters. If the short name field is not included in manifest.json, then name will be used instead and may be truncated. </p>

<p>This is a <a href="/en-US/docs/Mozilla/Add-ons/WebExtensions/Internationalization#internationalizing_manifest.json">localizable property</a>.</p>

<h2 id="Example">Example</h2>

<pre class="brush: json">"short_name": "My Extension"</pre>

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>