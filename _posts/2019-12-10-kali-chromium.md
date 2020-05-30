---
layout: post
title:  "Chromium installation in Kali Linux"
author: sal
categories: [ kali ]
image: assets/images/kali-chromium.jpg
beforetoc: "Step by step process to install chromium browser in kali "
toc: true
---

<!-- wp:paragraph -->
<p>Chromium exists within the Kali repositories and can be installed using:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>apt-get install chromium</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>By default chromium won’t launch on Kali Linux, this is due to chromium running as the root user. You can fix this by opening&nbsp;<code>/etc/chromium.d/default-flags</code>&nbsp;in vim and adding the following lines:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code># Run as root Kali
export CHROMIUM_FLAGS="$CHROMIUM_FLAGS --password-store=detect --no-sandbox --user-data-dir"</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>It&nbsp;<code>user-data-dir</code>&nbsp;and&nbsp;<code>sandboxing</code>, disabling sandboxing will have some obvious security issues but this browser is for web application penetration testing only.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>To use chromium for Web Application Penetration Testing you need to disable all the security features, allowing for DOM based XSS testing in chromium.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code># Disable Chromium security features for web app testing
export CHROMIUM_FLAGS="$CHROMIUM_FLAGS --disable-web-security"</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>To summarize the steps used,</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code># A set of command line flags that we want to set by default.

# Do not hide any extensions in the about:extensions dialog
export CHROMIUM_FLAGS="$CHROMIUM_FLAGS --show-component-extension-options"

# Don't use the GPU blacklist (bug #802933)
export CHROMIUM_FLAGS="$CHROMIUM_FLAGS --ignore-gpu-blacklist"

# Run as root Kali
export CHROMIUM_FLAGS="$CHROMIUM_FLAGS --password-store=detect --no-sandbox --user-data-dir"

# Disable Chromium security features for web app testing
export CHROMIUM_FLAGS="$CHROMIUM_FLAGS --disable-web-security"</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Finally Kali will give this error message and you can ignore this,</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>You Are using an Unsupported Command line flag –disable-web-security. Security and Stability will suffer</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p><strong><em>Note</em></strong> : <em><strong>DOM</strong> is document object model and <strong>XSS</strong> is cross site scripting</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>What is Chromium ?? </strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Chromium is an open source web browser run by&nbsp;<a href="https://www.chromium.org/Home">the Chromium Project</a>, first released in 2008. Any developer can modify or update the source code (but only small number of Chromium devs can actually add their very own code).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>How Chrome and Chromium is related ??</strong></p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol><li>Google's Chrome is actually built on top of Chromium's source code they share the same bones, as we've already established. </li><li>Their logos are also quite similar. Chrome's is Google-themed multi-color, and Chromium's is a few shades of blue.</li></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Biggest difference between chromium and chrome !!</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol><li>Chromium updates all the time as the developers would release the new code then an there its done and you have to update chromium manually whereas Google chrome doesn't update nearly as often as Chromium</li><li><strong>Security : </strong>Chrome is easy to use and Google tracks the data. Chromium  doesn't do this.</li><li><strong>Support for Flash Adobe:</strong> As Flash is not a open source, Chromium does not support it whereas Chrome does. </li></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Hope this information is useful !! please do leave your thoughts on chromium and the stuff you know about it in the comment section ....</p>
<!-- /wp:paragraph -->