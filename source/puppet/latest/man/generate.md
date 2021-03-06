---
layout: default
built_from_commit: d84d913905eea6e8180e6aef203edf1d8bf16dfd
title: 'Man Page: puppet generate'
canonical: "/puppet/latest/man/generate.html"
---

<div class='mp'>
<h2 id="NAME">NAME</h2>
<p class="man-name">
  <code>puppet-generate</code> - <span class="man-whatis">Generates Puppet code from Ruby definitions.</span>
</p>

<h2 id="SYNOPSIS">SYNOPSIS</h2>

<p>puppet generate <var>action</var></p>

<h2 id="OPTIONS">OPTIONS</h2>

<p>Note that any setting that's valid in the configuration
file is also a valid long argument, although it may or may not be
relevant to the present action. For example, <code>server</code> and <code>run_mode</code> are valid
settings, so you can specify <code>--server &lt;servername></code>, or
<code>--run_mode &lt;runmode></code> as an argument.</p>

<p>See the configuration file documentation at
<a href="https://puppet.com/docs/puppet/latest/configuration.html" data-bare-link="true">https://puppet.com/docs/puppet/latest/configuration.html</a> for the
full list of acceptable parameters. A commented list of all
configuration options can also be generated by running puppet with
<code>--genconfig</code>.</p>

<dl>
<dt>--render-as FORMAT</dt><dd>The format in which to render output. The most common formats are <code>json</code>,
<code>s</code> (string), <code>yaml</code>, and <code>console</code>, but other options such as <code>dot</code> are
sometimes available.</dd>
<dt>--verbose</dt><dd>Whether to log verbosely.</dd>
<dt class="flush">--debug</dt><dd>Whether to log debug information.</dd>
</dl>


<h2 id="ACTIONS">ACTIONS</h2>

<dl>
<dt><code>types</code> - Generates Puppet code for custom types</dt><dd><p><code>SYNOPSIS</code></p>

<p>puppet generate types [--format <var>format</var>] [--force]</p>

<p><code>DESCRIPTION</code></p>

<p>Generates definitions for custom resource types using Puppet code.</p>

<p>Types defined in Puppet code can be used to isolate custom type definitions
between different environments.</p>

<p><code>OPTIONS</code>
<var>--force</var> -
Forces the generation of output files (skips up-to-date checks).</p>

<p><var>--format &lt;format</var>> -
The generation output format to use. Supported formats: pcore.</p></dd>
</dl>


<h2 id="EXAMPLES">EXAMPLES</h2>

<p><code>types</code></p>

<p>Generate Puppet type definitions for all custom resource types in the current environment:</p>

<pre><code>$ puppet generate types
</code></pre>

<p>Generate Puppet type definitions for all custom resource types in the specified environment:</p>

<pre><code>$ puppet generate types --environment development
</code></pre>

<h2 id="COPYRIGHT-AND-LICENSE">COPYRIGHT AND LICENSE</h2>

<p>Copyright 2016 by Puppet Inc.
Apache 2 license; see COPYING</p>

</div>
