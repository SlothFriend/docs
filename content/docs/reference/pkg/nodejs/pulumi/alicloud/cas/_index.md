---
title: "Module cas"
title_tag: "Module cas | Package @pulumi/alicloud | Node.js SDK"
linktitle: "cas"
meta_desc: "Explore members of the cas module in the @pulumi/alicloud package."
git_sha: "ba11fd33d15635f294823990be8ffe1564fe697d"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "alicloud" >}}




<h3>Resources</h3>
<ul class="api">
    <li><a href="#Certificate"><span class="symbol resource"></span>Certificate</a></li>
</ul>

<h3>Functions</h3>
<ul class="api">
    <li><a href="#getCertificates"><span class="symbol function"></span>getCertificates</a></li>
</ul>

<h3>Others</h3>
<ul class="api">
    <li><a href="#CertificateArgs"><span class="symbol api"></span>CertificateArgs</a></li>
    <li><a href="#CertificateState"><span class="symbol api"></span>CertificateState</a></li>
    <li><a href="#GetCertificatesArgs"><span class="symbol api"></span>GetCertificatesArgs</a></li>
    <li><a href="#GetCertificatesResult"><span class="symbol api"></span>GetCertificatesResult</a></li>
</ul>


<h2 id="resources">Resources</h2>
<h3 class="pdoc-module-header" id="Certificate" data-link-title="Certificate">
    <a href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L30">
        Resource <strong>Certificate</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>Certificate</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

Provides a CAS Certificate resource.

> **NOTE:** The Certificate name which you want to add must be already registered and had not added by another account. Every Certificate name can only exist in a unique group.

> **NOTE:** The Cas Certificate region only support cn-hangzhou, ap-south-1, me-east-1, eu-central-1, ap-northeast-1, ap-southeast-2.

> **NOTE:** Available in 1.35.0+ .

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";
import * from "fs";

// Add a new Certificate.
const cert = new alicloud.cas.Certificate("cert", {
    cert: fs.readFileSync(`${path.module}/test.crt`),
    key: fs.readFileSync(`${path.module}/test.key`),
});
```

<h4 class="pdoc-member-header" id="Certificate-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L69"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> Certificate(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#CertificateArgs'>CertificateArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a Certificate resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="Certificate-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L40">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#CertificateState'>CertificateState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Certificate'>Certificate</a></code></pre>


Get an existing Certificate resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="Certificate-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L30">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="Certificate-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L51">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is Certificate</code></pre>


Returns true if the given object is an instance of Certificate.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="Certificate-cert">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L61">property <b>cert</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>cert: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Cert of the Certificate in which the Certificate will add.

<h4 class="pdoc-member-header" id="Certificate-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L30">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="Certificate-key">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L65">property <b>key</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>key: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Key of the Certificate in which the Certificate will add.

<h4 class="pdoc-member-header" id="Certificate-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L69">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the Certificate. This name without suffix can have a string of 1 to 63 characters, must contain only alphanumeric characters or "-", and must not begin or end with "-", and "-" must not in the 3th and 4th character positions at the same time. Suffix `.sh` and `.tel` are not supported.

<h4 class="pdoc-member-header" id="Certificate-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L30">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.


<h2 id="functions">Functions</h2>
<h3 class="pdoc-module-header" id="getCertificates" data-link-title="getCertificates">
    <a href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L25">
        Function <strong>getCertificates</strong>
    </a>
</h3>


<pre class="highlight"><code><span class='kd'></span>getCertificates(args?: <a href='#GetCertificatesArgs'>GetCertificatesArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions'>pulumi.InvokeOptions</a>): <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise'>Promise</a>&lt;<a href='#GetCertificatesResult'>GetCertificatesResult</a>&gt;</code></pre>


This data source provides a list of CAS Certificates in an Alibaba Cloud account according to the specified filters.

#### Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const certs = pulumi.output(alicloud.cas.getCertificates({
    nameRegex: "^cas",
    outputFile: `./cas_certificates.json`,
}, { async: true }));

export const cert = certs.certificates[0].id;
```


<h2 id="apis">Others</h2>
<h3 class="pdoc-module-header" id="CertificateArgs" data-link-title="CertificateArgs">
    <a href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L130">
        interface <strong>CertificateArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>CertificateArgs</span></code></pre>

The set of arguments for constructing a Certificate resource.

<h4 class="pdoc-member-header" id="CertificateArgs-cert">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L134">property <b>cert</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>cert: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Cert of the Certificate in which the Certificate will add.

<h4 class="pdoc-member-header" id="CertificateArgs-key">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L138">property <b>key</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>key: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Key of the Certificate in which the Certificate will add.

<h4 class="pdoc-member-header" id="CertificateArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L142">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the Certificate. This name without suffix can have a string of 1 to 63 characters, must contain only alphanumeric characters or "-", and must not begin or end with "-", and "-" must not in the 3th and 4th character positions at the same time. Suffix `.sh` and `.tel` are not supported.

<h3 class="pdoc-module-header" id="CertificateState" data-link-title="CertificateState">
    <a href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L112">
        interface <strong>CertificateState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>CertificateState</span></code></pre>

Input properties used for looking up and filtering Certificate resources.

<h4 class="pdoc-member-header" id="CertificateState-cert">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L116">property <b>cert</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>cert?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Cert of the Certificate in which the Certificate will add.

<h4 class="pdoc-member-header" id="CertificateState-key">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L120">property <b>key</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>key?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Key of the Certificate in which the Certificate will add.

<h4 class="pdoc-member-header" id="CertificateState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/certificate.ts#L124">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Name of the Certificate. This name without suffix can have a string of 1 to 63 characters, must contain only alphanumeric characters or "-", and must not begin or end with "-", and "-" must not in the 3th and 4th character positions at the same time. Suffix `.sh` and `.tel` are not supported.

<h3 class="pdoc-module-header" id="GetCertificatesArgs" data-link-title="GetCertificatesArgs">
    <a href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L44">
        interface <strong>GetCertificatesArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetCertificatesArgs</span></code></pre>

A collection of arguments for invoking getCertificates.

<h4 class="pdoc-member-header" id="GetCertificatesArgs-ids">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L48">property <b>ids</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>ids?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</code></pre>

A list of cert IDs.

<h4 class="pdoc-member-header" id="GetCertificatesArgs-nameRegex">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L52">property <b>nameRegex</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>nameRegex?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

A regex string to filter results by the certificate name.

<h4 class="pdoc-member-header" id="GetCertificatesArgs-outputFile">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L53">property <b>outputFile</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>outputFile?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h3 class="pdoc-module-header" id="GetCertificatesResult" data-link-title="GetCertificatesResult">
    <a href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L59">
        interface <strong>GetCertificatesResult</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>GetCertificatesResult</span></code></pre>

A collection of values returned by getCertificates.

<h4 class="pdoc-member-header" id="GetCertificatesResult-certificates">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L63">property <b>certificates</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>certificates: <a href='/docs/reference/pkg/nodejs/pulumi/alicloud/types/output/#GetCertificatesCertificate'>GetCertificatesCertificate</a>[];</code></pre>

A list of apis. Each element contains the following attributes:

<h4 class="pdoc-member-header" id="GetCertificatesResult-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L67">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>

The provider-assigned unique ID for this managed resource.

<h4 class="pdoc-member-header" id="GetCertificatesResult-ids">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L71">property <b>ids</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>ids: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</code></pre>

A list of cert IDs.

<h4 class="pdoc-member-header" id="GetCertificatesResult-nameRegex">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L72">property <b>nameRegex</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>nameRegex?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
<h4 class="pdoc-member-header" id="GetCertificatesResult-names">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L76">property <b>names</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>names: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</code></pre>

A list of cert names.

<h4 class="pdoc-member-header" id="GetCertificatesResult-outputFile">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-alicloud/blob/ba11fd33d15635f294823990be8ffe1564fe697d/sdk/nodejs/cas/getCertificates.ts#L77">property <b>outputFile</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>outputFile?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</code></pre>
