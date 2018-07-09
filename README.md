# aws_sns `fastlane` plugin

[![fastlane Plugin Badge](https://rawcdn.githack.com/fastlane/fastlane/master/fastlane/assets/plugin-badge.svg)](https://rubygems.org/gems/fastlane-plugin-aws_sns)

## Getting Started

This project is a [fastlane](https://github.com/fastlane/fastlane) plugin. To get started with `fastlane-plugin-aws_sns`, add it to your project by running:

```bash
fastlane add_plugin aws_sns
```

## About aws_sns

[AWS SNS](https://aws.amazon.com/sns/) is fully managed push notification service. This plugin updates an AWS SNS platform application for iOS and Android apps.

iOS app are updated by uploading a private key (p12) to AWS SNS - which can easily be created with [PEM](https://github.com/fastlane/fastlane/tree/master/pem)

Android apps are updated by sending up a GCM Api Key to AWS SNS - obtained through your [Google Cloud Platform dashboard](https://console.cloud.google.com)


## Example

### iOS
```ruby
aws_sns(
  platform: 'APNS',
  platform_application_arn: 'your_application_platform_arn',
  platform_apns_private_key_path: 'path/to/cert.p12',

  # Optional private key password
  # platform_apns_private_key_password: 'joshissupercool'
)
```

### Android
```ruby
aws_sns(
  platform: 'GCM',
  platform_application_arn: 'your_application_platform_arn',
  platform_gcm_api_key: 'your_gcm_api_key'
)
```

## Run tests for this plugin

To run both the tests, and code style validation, run

```
rake
```

To automatically fix many of the styling issues, use
```
rubocop -a
```

## Issues and Feedback

For any other issues and feedback about this plugin, please submit it to this repository.

## Troubleshooting

If you have trouble using plugins, check out the [Plugins Troubleshooting](https://github.com/fastlane/fastlane/blob/master/fastlane/docs/PluginsTroubleshooting.md) doc in the main `fastlane` repo.

## Using `fastlane` Plugins

For more information about how the `fastlane` plugin system works, check out the [Plugins documentation](https://github.com/fastlane/fastlane/blob/master/fastlane/docs/Plugins.md).

## About `fastlane`

`fastlane` is the easiest way to automate beta deployments and releases for your iOS and Android apps. To learn more, check out [fastlane.tools](https://fastlane.tools).

## Author

Josh Holtz, josh@rokkincat.com, [@joshdholtz](https://twitter.com/joshdholtz)

I'm available for freelance work (Fastlane, iOS, and Android development) :muscle:
Feel free to contact me :rocket:
