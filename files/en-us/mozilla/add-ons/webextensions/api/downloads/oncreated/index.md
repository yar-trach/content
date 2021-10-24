---
title: downloads.onCreated
slug: Mozilla/Add-ons/WebExtensions/API/downloads/onCreated
tags:
  - API
  - Add-ons
  - Event
  - Extensions
  - Non-standard
  - Reference
  - WebExtensions
  - downloads
  - onCreated
browser-compat: webextensions.api.downloads.onCreated
---
<div>{{AddonSidebar()}}</div>

<p>The <code><strong>onCreated</strong></code><strong><code>()</code></strong> event of the {{WebExtAPIRef("downloads")}} API fires when a download begins, i.e. when {{WebExtAPIRef("downloads.download()")}} is successfully invoked.</p>

<p>The listener is passed the {{WebExtAPIRef('downloads.DownloadItem')}} object in question as a parameter.</p>

<h2 id="Syntax">Syntax</h2>

<pre class="brush:js">browser.downloads.onCreated.addListener(listener)
browser.downloads.onCreated.removeListener(listener)
browser.downloads.onCreated.hasListener(listener)
</pre>

<p>Events have three functions:</p>

<dl>
 <dt><code>addListener(callback)</code></dt>
 <dd>Adds a listener to this event.</dd>
 <dt><code>removeListener(listener)</code></dt>
 <dd>Stop listening to this event. The <code>listener</code> argument is the listener to remove.</dd>
 <dt><code>hasListener(listener)</code></dt>
 <dd>Check whether a given <code>listener</code> is registered for this event. Returns <code>true</code> if it is listening, <code>false</code> otherwise.</dd>
</dl>

<h2 id="addListener_syntax">addListener syntax</h2>

<h3 id="Parameters">Parameters</h3>

<dl>
 <dt><code>function</code></dt>
 <dd>
 <p>A callback function that will be called when this event occurs. This function will be passed the following arguments:</p>

 <dl>
  <dt><code>downloadItem</code></dt>
  <dd>The {{WebExtAPIRef('downloads.DownloadItem')}} object in question.</dd>
 </dl>
 </dd>
</dl>

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>

<h2 id="Examples">Examples</h2>

<p>Log the URL of items as they are downloaded:</p>

<pre class="brush: js">function handleCreated(item) {
  console.log(item.url);
}

browser.downloads.onCreated.addListener(handleCreated);</pre>

<p>{{WebExtExamples}}</p>


<div class="note"><p><strong>Note:</strong> This API is based on Chromium's <a href="https://developer.chrome.com/extensions/downloads#event-onCreated"><code>chrome.downloads</code></a> API.</p>

<p>Microsoft Edge compatibility data is supplied by Microsoft Corporation and is included here under the Creative Commons Attribution 3.0 United States License.</p>
</div>

<div class="hidden">
<pre>// Copyright 2015 The Chromium Authors. All rights reserved.
//
// Redistribution and use in source and binary forms, with or without
// modification, are permitted provided that the following conditions are
// met:
//
//    * Redistributions of source code must retain the above copyright
// notice, this list of conditions and the following disclaimer.
//    * Redistributions in binary form must reproduce the above
// copyright notice, this list of conditions and the following disclaimer
// in the documentation and/or other materials provided with the
// distribution.
//    * Neither the name of Google Inc. nor the names of its
// contributors may be used to endorse or promote products derived from
// this software without specific prior written permission.
//
// THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
// "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
// LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
// A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
// OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
// SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
// LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
// DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
// THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
// (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
// OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
</pre>
</div>