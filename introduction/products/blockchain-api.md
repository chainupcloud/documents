---
description: Learn what APIs are available via ChainUp Cloud and how to use them
---

# ⛓ Blockchain API

ChainUp Cloud supports each network's common APIs so you can focus on building while benefiting from the same endpoints and methods available at the node level. There are no lock-ins, simply benefit from high scalability while we take care of maintaining the level of service necessary for your product to thrive.

The common network APIs should only be the beginning of the journey for Web3 developers. ChainUp Cloud is developing Advanced APIs to help developers unlock the unique features and attributes of Web3 protocols. Our suite of Advanced APIs allows developers to create powerful applications at a fraction of the cost, with the potential to capitalize on blockchain-native use cases.

Advanced APIs complement the common APIs to give its users superpowers in order to create the Web3's killer apps.

## Difference Between Quotas and Rate Limits

A Quota measures how many total requests you can make across _all your services_ in one day.

A Rate Limit measures how many requests you can make against a _specific endpoint_ in one second.

If you go over your Quota for the day, you'll need to upgrade your plan.

If you hit a Rate Limit for an endpoint, you'll need to retry your requests.

The goal of a Quota is to allow customers to pay for what they use, similar to a cell phone plan.

The goal of a Rate Limit is to ensure quality of service, and most users will never come close to hitting a Rate Limit.

## How Do I Know When I've Hit My Quota?

ChainUp Cloud will return status code `HTTP 429` "Too Many Requests" when you exceed your Quota.

To confirm this, you can view your current Quota usage on your ChainUp Cloud Dashboard.

![Quota usage](../../.gitbook/assets/chainupcloudapilimit.png)

You can upgrade your plan to increase your Quota.

## How Do I Know When I'm Getting Rate Limited?

ChainUp Cloud will return status code `HTTP 429` "Too Many Requests" when you are getting rate limited for a specific endpoint.

If this happens, you can confirm on your ChainUp Cloud Dashboard that you are not over your Quota and that you are instead getting rate limited.

If you are getting rate limited, you will need to retry your requests in your application. Since Rate Limits are measured per second, you could simply wait for a second and try again.

If you need more information about quotas and rate limits, join [**our community**](https://t.me/ChainUp2022) and one of our experts will help you out!
