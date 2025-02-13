---
title: How to upgrade the Redis version of Azure Cache for Redis
description: Learn how to upgrade the version of Azure Cache for Redis
author: flang-msft

ms.author: franlanglois
ms.service: cache
ms.topic: how-to
ms.date: 12/15/2022
ms.custom: template-how-to
---


# How to upgrade an existing Redis 4 cache to Redis 6

> [!IMPORTANT]
> We are improving the upgrade experience and have temporarily disabled the Redis version upgrade. We recommend that you upgrade your caches after January 20, 2023.

Azure Cache for Redis supports upgrading the version of your Azure Cache for Redis from Redis 4 to Redis 6. Upgrading is similar to regular monthly maintenance. Upgrading follows the same pattern as maintenance: First, the Redis version on the replica node is updated, followed by an update to the primary node. Your client application should treat the upgrade operation exactly like a planned maintenance event.

As a precautionary step, we recommend exporting the data from your existing Redis 4 cache and testing your client application with a Redis 6 cache in a lower environment before upgrading.

For more information on how to export, see [Import and Export data in Azure Cache for Redis](cache-how-to-import-export-data.md).

> [!IMPORTANT]
> As announced in [What's new](cache-whats-new.md#upgrade-your-azure-cache-for-redis-instances-to-use-redis-version-6-by-june-30-2023), we'll retire version 4 for Azure Cache for Redis instances on June 30, 2023. Before that date, you need to upgrade any of your cache instances to version 6.
>
> For more information on the retirement of Redis 4, see [Retirements](cache-retired-features.md).
>

## Prerequisites

- Azure subscription - [create one for free](https://azure.microsoft.com/free/)

### Limitations

- When you upgrade a cache in the Basic tier, it's unavailable for several minutes and results in data loss.
- Upgrading on geo-replicated cache isn't supported. You must manually unlink the cache instances before upgrading.
- Upgrading a cache with a dependency on Cloud Services isn't supported. You should migrate your cache instance to Virtual Machine Scale Set before upgrading. For more information, see [Caches with a dependency on Cloud Services (classic)](./cache-faq.yml) for details on cloud services hosted caches.

### Check the version of a cache

Before you upgrade, check the Redis version of a cache by selecting **Properties** from the Resource menu of the Azure Cache for Redis. We recommend you use Redis 6.

:::image type="content" source="media/cache-how-to-upgrade/cache-version-portal.png" alt-text="Screenshot of properties selected in the Resource menu.":::

## Upgrade using the Azure portal

> [!IMPORTANT]
> We are improving the upgrade experience and have temporarily disabled the Redis version upgrade. We recommend that you upgrade your caches after January 20, 2023.

## Upgrade using Azure CLI

> [!IMPORTANT]
> We are improving the upgrade experience and have temporarily disabled the Redis version upgrade. We recommend that you upgrade your caches after January 20, 2023.

## Upgrade using PowerShell

> [!IMPORTANT]
> We are improving the upgrade experience and have temporarily disabled the Redis version upgrade. We recommend that you upgrade your caches after January 20, 2023.

## Next steps

- To learn more about Azure Cache for Redis versions, see [Set Redis version for Azure Cache for Redis](cache-how-to-version.md)
- To learn more about Redis 6 features, see [Diving Into Redis 6.0 by Redis](https://redis.com/blog/diving-into-redis-6/)
- To learn more about Azure Cache for Redis features: [Azure Cache for Redis Premium service tiers](cache-overview.md#service-tiers)
