# AWS::Macie Construct Library
<!--BEGIN STABILITY BANNER-->

---

![cfn-resources: Stable](https://img.shields.io/badge/cfn--resources-stable-success.svg?style=for-the-badge)

> All classes with the `Cfn` prefix in this module ([CFN Resources]) are always stable and safe to use.
>
> [CFN Resources]: https://docs.aws.amazon.com/cdk/latest/guide/constructs.html#constructs_lib

---

<!--END STABILITY BANNER-->

This module is part of the [AWS Cloud Development Kit](https://github.com/aws/aws-cdk) project.

```ts
import macie = require('@aws-cdk/aws-macie');
```

Enable Macie

```ts
import * as cdk from '@aws-cdk/core';
import * as macie from '@aws-cdk/aws-macie';

export class MacieStack extends cdk.Stack {
  constructor(scope: cdk.Construct, id: string, props?: cdk.StackProps) {
    super(scope, id, props);

    const enableMacie = new macie.CfnSession(this, "macie-cdk", {
      findingPublishingFrequency: "FIFTEEN_MINUTES",
      status: "ENABLED"
    });
  }
}
```
