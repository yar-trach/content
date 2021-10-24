---
title: tabs.goBack()
slug: Mozilla/Add-ons/WebExtensions/API/tabs/goBack
tags:
  - API
  - Add-ons
  - Extensions
  - Method
  - Non-standard
  - Reference
  - WebExtensions
  - goBack
browser-compat: webextensions.api.tabs.goBack
---
<div>{{AddonSidebar()}}</div>

<p>Navigate to the previous page in tab's history, if available.</p>

<p>This is an asynchronous function that returns a <code><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise">Promise</a></code>.</p>

<h2 id="Syntax">Syntax</h2>

<pre class="brush:js">var withGoingBack = browser.tabs.goBack(
  tabId,                  // optional integer
  callback                  // optional function
)
</pre>

<h3 id="Parameters">Parameters</h3>

<dl>
 <dt><code>tabId</code>{{optional_inline}}</dt>
 <dd><code>integer</code>. The ID of the tab to navigate. Defaults to the active tab of the current window.</dd>
 <dt><code>callback</code>{{optional_inline}}</dt>
 <dd><code>function</code>. When the page navigation finishes, this function is called without parameters.</dd>
</dl>

<h3 id="Return_value">Return value</h3>

<p>A <code><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise">Promise</a></code> that is fulfilled when the page navigation finishes.</p>

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>

<h2 id="Examples">Examples</h2>

<p>Go back to the previous page in the current tab:</p>

<pre class="brush: js">function onGoBack() {
  console.log("Gone back");
}

function onError(error) {
  console.log(`Error: ${error}`);
}

var goingBack = browser.tabs.goBack();
goingBack.then(onGoBack, onError);</pre>

<p>{{WebExtExamples}}</p>

<div class="note"><p><strong>Note:</strong> This API is based on Chromium's <a href="https://developer.chrome.com/extensions/tabs#method-getZoomSettings"><code>chrome.tabs</code></a> API. This documentation is derived from <a href="https://chromium.googlesource.com/chromium/src/+/master/chrome/common/extensions/api/tabs.json"><code>tabs.json</code></a> in the Chromium code.</p>

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