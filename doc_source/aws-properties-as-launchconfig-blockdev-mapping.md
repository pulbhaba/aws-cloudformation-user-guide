# AWS::AutoScaling::LaunchConfiguration BlockDeviceMapping<a name="aws-properties-as-launchconfig-blockdev-mapping"></a>

 `BlockDeviceMapping` is a property of [LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html) that describes a block device mapping for an Amazon EC2 Auto Scaling group\.

Each instance that is launched has an associated root device volume, either an Amazon EBS volume or an instance store volume\. You can use block device mappings to specify additional EBS volumes or instance store volumes to attach to an instance when it is launched\. 

For more information, see [Example Block Device Mapping](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/block-device-mapping-concepts.html#block-device-mapping-ex) in the *Amazon EC2 User Guide for Linux Instances*\.

## Syntax<a name="aws-properties-as-launchconfig-blockdev-mapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-as-launchconfig-blockdev-mapping-syntax.json"></a>

```
{
  "[DeviceName](#cfn-as-launchconfig-blockdev-mapping-devicename)" : String,
  "[Ebs](#cfn-as-launchconfig-blockdev-mapping-ebs)" : [BlockDevice](aws-properties-as-launchconfig-blockdev-template.md),
  "[NoDevice](#cfn-as-launchconfig-blockdev-mapping-nodevice)" : Boolean,
  "[VirtualName](#cfn-as-launchconfig-blockdev-mapping-virtualname)" : String
}
```

### YAML<a name="aws-properties-as-launchconfig-blockdev-mapping-syntax.yaml"></a>

```
  [DeviceName](#cfn-as-launchconfig-blockdev-mapping-devicename): String
  [Ebs](#cfn-as-launchconfig-blockdev-mapping-ebs): 
    [BlockDevice](aws-properties-as-launchconfig-blockdev-template.md)
  [NoDevice](#cfn-as-launchconfig-blockdev-mapping-nodevice): Boolean
  [VirtualName](#cfn-as-launchconfig-blockdev-mapping-virtualname): String
```

## Properties<a name="aws-properties-as-launchconfig-blockdev-mapping-properties"></a>

`DeviceName`  <a name="cfn-as-launchconfig-blockdev-mapping-devicename"></a>
The device name exposed to the EC2 instance \(for example, `/dev/sdh` or `xvdh`\)\. For more information, see [Device Naming on Linux Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/device_naming.html) in the *Amazon EC2 User Guide for Linux Instances*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ebs`  <a name="cfn-as-launchconfig-blockdev-mapping-ebs"></a>
The information about the Amazon EBS volume\.   
You can specify either `VirtualName` or `Ebs`, but not both\.   
*Required*: No  
*Type*: [BlockDevice](aws-properties-as-launchconfig-blockdev-template.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoDevice`  <a name="cfn-as-launchconfig-blockdev-mapping-nodevice"></a>
Suppresses the device mapping\. The only permitted value for this property is `true`\.  
If this property is set to `true` for the root device, the instance might fail the Amazon EC2 health check\. Amazon EC2 Auto Scaling launches a replacement instance if the instance fails the health check\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VirtualName`  <a name="cfn-as-launchconfig-blockdev-mapping-virtualname"></a>
The name of the virtual device\. The name must be in the form ephemeral*X* where *X* is a number starting from zero \(0\), for example, `ephemeral0`\.  
You can specify either `VirtualName` or `Ebs`, but not both\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-as-launchconfig-blockdev-mapping--seealso"></a>
+ [Amazon EC2 Instance Store](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html) in the *Amazon EC2 User Guide for Linux Instances*
+ [Amazon Elastic Block Store \(Amazon EBS\)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html) in the *Amazon EC2 User Guide for Linux Instances*