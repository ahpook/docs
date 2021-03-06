
---
title: "GetSecret"
title_tag: "Function GetSecret | Module secretsmanager | Package AWS"
meta_desc: "Explore the GetSecret function of the secretsmanager module, including examples, input properties, output properties, and supporting types. Retrieve metadata information about a Secrets Manager secret. To retrieve a secret value, see the `aws.secretsmanager.SecretVersion`."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Retrieve metadata information about a Secrets Manager secret. To retrieve a secret value, see the `aws.secretsmanager.SecretVersion`.

{{% examples %}}
## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}
### ARN
{{% example csharp %}}
```csharp
using Pulumi;
using Aws = Pulumi.Aws;

class MyStack : Stack
{
    public MyStack()
    {
        var by_arn = Output.Create(Aws.SecretsManager.GetSecret.InvokeAsync(new Aws.SecretsManager.GetSecretArgs
        {
            Arn = "arn:aws:secretsmanager:us-east-1:123456789012:secret:example-123456",
        }));
    }

}
```

{{% /example %}}

{{% example go %}}
```go
package main

import (
	"github.com/pulumi/pulumi-aws/sdk/v3/go/aws/secretsmanager"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "arn:aws:secretsmanager:us-east-1:123456789012:secret:example-123456"
		_, err := secretsmanager.LookupSecret(ctx, &secretsmanager.LookupSecretArgs{
			Arn: &opt0,
		}, nil)
		if err != nil {
			return err
		}
		return nil
	})
}
```

{{% /example %}}

{{% example python %}}
```python
import pulumi
import pulumi_aws as aws

by_arn = aws.secretsmanager.get_secret(arn="arn:aws:secretsmanager:us-east-1:123456789012:secret:example-123456")
```

{{% /example %}}

{{% example typescript %}}

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const by_arn = pulumi.output(aws.secretsmanager.getSecret({
    arn: "arn:aws:secretsmanager:us-east-1:123456789012:secret:example-123456",
}, { async: true }));
```

{{% /example %}}

### Name
{{% example csharp %}}
```csharp
using Pulumi;
using Aws = Pulumi.Aws;

class MyStack : Stack
{
    public MyStack()
    {
        var by_name = Output.Create(Aws.SecretsManager.GetSecret.InvokeAsync(new Aws.SecretsManager.GetSecretArgs
        {
            Name = "example",
        }));
    }

}
```

{{% /example %}}

{{% example go %}}
```go
package main

import (
	"github.com/pulumi/pulumi-aws/sdk/v3/go/aws/secretsmanager"
	"github.com/pulumi/pulumi/sdk/v2/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "example"
		_, err := secretsmanager.LookupSecret(ctx, &secretsmanager.LookupSecretArgs{
			Name: &opt0,
		}, nil)
		if err != nil {
			return err
		}
		return nil
	})
}
```

{{% /example %}}

{{% example python %}}
```python
import pulumi
import pulumi_aws as aws

by_name = aws.secretsmanager.get_secret(name="example")
```

{{% /example %}}

{{% example typescript %}}

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const by_name = pulumi.output(aws.secretsmanager.getSecret({
    name: "example",
}, { async: true }));
```

{{% /example %}}

{{% /examples %}}


## Using GetSecret {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getSecret<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/secretsmanager/#GetSecretArgs">GetSecretArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/secretsmanager/#GetSecretResult">GetSecretResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_secret(</span>arn=None<span class="p">, </span>name=None<span class="p">, </span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupSecret<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/v3/go/aws/secretsmanager?tab=doc#LookupSecretArgs">LookupSecretArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/v3/go/aws/secretsmanager?tab=doc#LookupSecretResult">LookupSecretResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupSecret` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetSecret </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Secretsmanager.GetSecretResult.html">GetSecretResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.SecretsManager.GetSecretArgs.html">GetSecretArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="arn_csharp">
<a href="#arn_csharp" style="color: inherit; text-decoration: inherit;">Arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the secret to retrieve.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the secret to retrieve.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="arn_go">
<a href="#arn_go" style="color: inherit; text-decoration: inherit;">Arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the secret to retrieve.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the secret to retrieve.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="arn_nodejs">
<a href="#arn_nodejs" style="color: inherit; text-decoration: inherit;">arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the secret to retrieve.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the secret to retrieve.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="arn_python">
<a href="#arn_python" style="color: inherit; text-decoration: inherit;">arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the secret to retrieve.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The name of the secret to retrieve.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## GetSecret Result {#result}

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="arn_csharp">
<a href="#arn_csharp" style="color: inherit; text-decoration: inherit;">Arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}A description of the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="kmskeyid_csharp">
<a href="#kmskeyid_csharp" style="color: inherit; text-decoration: inherit;">Kms<wbr>Key<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The Key Management Service (KMS) Customer Master Key (CMK) associated with the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="policy_csharp">
<a href="#policy_csharp" style="color: inherit; text-decoration: inherit;">Policy</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The resource-based policy document that's attached to the secret.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotationenabled_csharp">
<a href="#rotationenabled_csharp" style="color: inherit; text-decoration: inherit;">Rotation<wbr>Enabled</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">bool</a></span>
    </dt>
    <dd>{{% md %}}Whether rotation is enabled or not.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotationlambdaarn_csharp">
<a href="#rotationlambdaarn_csharp" style="color: inherit; text-decoration: inherit;">Rotation<wbr>Lambda<wbr>Arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}Rotation Lambda function Amazon Resource Name (ARN) if rotation is enabled.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotationrules_csharp">
<a href="#rotationrules_csharp" style="color: inherit; text-decoration: inherit;">Rotation<wbr>Rules</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsecretrotationrule">List&lt;Get<wbr>Secret<wbr>Rotation<wbr>Rule&gt;</a></span>
    </dt>
    <dd>{{% md %}}Rotation rules if rotation is enabled.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}Tags of the secret.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="arn_go">
<a href="#arn_go" style="color: inherit; text-decoration: inherit;">Arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}A description of the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="kmskeyid_go">
<a href="#kmskeyid_go" style="color: inherit; text-decoration: inherit;">Kms<wbr>Key<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The Key Management Service (KMS) Customer Master Key (CMK) associated with the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="policy_go">
<a href="#policy_go" style="color: inherit; text-decoration: inherit;">Policy</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The resource-based policy document that's attached to the secret.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotationenabled_go">
<a href="#rotationenabled_go" style="color: inherit; text-decoration: inherit;">Rotation<wbr>Enabled</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#boolean">bool</a></span>
    </dt>
    <dd>{{% md %}}Whether rotation is enabled or not.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotationlambdaarn_go">
<a href="#rotationlambdaarn_go" style="color: inherit; text-decoration: inherit;">Rotation<wbr>Lambda<wbr>Arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}Rotation Lambda function Amazon Resource Name (ARN) if rotation is enabled.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotationrules_go">
<a href="#rotationrules_go" style="color: inherit; text-decoration: inherit;">Rotation<wbr>Rules</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsecretrotationrule">[]Get<wbr>Secret<wbr>Rotation<wbr>Rule</a></span>
    </dt>
    <dd>{{% md %}}Rotation rules if rotation is enabled.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}Tags of the secret.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="arn_nodejs">
<a href="#arn_nodejs" style="color: inherit; text-decoration: inherit;">arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}A description of the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="kmskeyid_nodejs">
<a href="#kmskeyid_nodejs" style="color: inherit; text-decoration: inherit;">kms<wbr>Key<wbr>Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The Key Management Service (KMS) Customer Master Key (CMK) associated with the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="policy_nodejs">
<a href="#policy_nodejs" style="color: inherit; text-decoration: inherit;">policy</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The resource-based policy document that's attached to the secret.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotationenabled_nodejs">
<a href="#rotationenabled_nodejs" style="color: inherit; text-decoration: inherit;">rotation<wbr>Enabled</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/boolean">boolean</a></span>
    </dt>
    <dd>{{% md %}}Whether rotation is enabled or not.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotationlambdaarn_nodejs">
<a href="#rotationlambdaarn_nodejs" style="color: inherit; text-decoration: inherit;">rotation<wbr>Lambda<wbr>Arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}Rotation Lambda function Amazon Resource Name (ARN) if rotation is enabled.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotationrules_nodejs">
<a href="#rotationrules_nodejs" style="color: inherit; text-decoration: inherit;">rotation<wbr>Rules</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsecretrotationrule">Get<wbr>Secret<wbr>Rotation<wbr>Rule[]</a></span>
    </dt>
    <dd>{{% md %}}Rotation rules if rotation is enabled.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}Tags of the secret.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="arn_python">
<a href="#arn_python" style="color: inherit; text-decoration: inherit;">arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}A description of the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="kms_key_id_python">
<a href="#kms_key_id_python" style="color: inherit; text-decoration: inherit;">kms_<wbr>key_<wbr>id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The Key Management Service (KMS) Customer Master Key (CMK) associated with the secret.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="policy_python">
<a href="#policy_python" style="color: inherit; text-decoration: inherit;">policy</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The resource-based policy document that's attached to the secret.
{{% /md %}}</dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotation_enabled_python">
<a href="#rotation_enabled_python" style="color: inherit; text-decoration: inherit;">rotation_<wbr>enabled</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">bool</a></span>
    </dt>
    <dd>{{% md %}}Whether rotation is enabled or not.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotation_lambda_arn_python">
<a href="#rotation_lambda_arn_python" style="color: inherit; text-decoration: inherit;">rotation_<wbr>lambda_<wbr>arn</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}Rotation Lambda function Amazon Resource Name (ARN) if rotation is enabled.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property- property-deprecated"
            title=", Deprecated">
        <span id="rotation_rules_python">
<a href="#rotation_rules_python" style="color: inherit; text-decoration: inherit;">rotation_<wbr>rules</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getsecretrotationrule">List[Get<wbr>Secret<wbr>Rotation<wbr>Rule]</a></span>
    </dt>
    <dd>{{% md %}}Rotation rules if rotation is enabled.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}Use the aws_secretsmanager_secret_rotation data source instead{{% /md %}}</p></dd>

    <dt class="property-"
            title="">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, str]</span>
    </dt>
    <dd>{{% md %}}Tags of the secret.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Supporting Types


<h4 id="getsecretrotationrule">Get<wbr>Secret<wbr>Rotation<wbr>Rule</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#GetSecretRotationRule">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/v3/go/aws/secretsmanager?tab=doc#GetSecretRotationRule">output</a> API doc for this type.
{{% /choosable %}}
{{% choosable language csharp %}}
> See the   <a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.SecretsManager.Outputs.GetSecretRotationRule.html">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="automaticallyafterdays_csharp">
<a href="#automaticallyafterdays_csharp" style="color: inherit; text-decoration: inherit;">Automatically<wbr>After<wbr>Days</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">int</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="automaticallyafterdays_go">
<a href="#automaticallyafterdays_go" style="color: inherit; text-decoration: inherit;">Automatically<wbr>After<wbr>Days</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#integer">int</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="automaticallyafterdays_nodejs">
<a href="#automaticallyafterdays_nodejs" style="color: inherit; text-decoration: inherit;">automatically<wbr>After<wbr>Days</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/integer">number</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="automaticallyafterdays_python">
<a href="#automaticallyafterdays_python" style="color: inherit; text-decoration: inherit;">automatically<wbr>After<wbr>Days</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">float</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws">https://github.com/pulumi/pulumi-aws</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>This Pulumi package is based on the [`aws` Terraform Provider](https://github.com/terraform-providers/terraform-provider-aws).</dd>
</dl>

