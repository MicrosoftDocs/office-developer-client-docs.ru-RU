---
title: Типичные последовательности вызовов OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: В этом разделе описаны типичные последовательности вызовов Outlook Social Connector (OSC) для членов в интерфейсах extensibility поставщика OSC, которые реализует поставщик OSC.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413614"
---
# <a name="osc-typical-calling-sequences"></a>Типичные последовательности вызовов OSC

В этом разделе описаны типичные последовательности вызовов Outlook Social Connector (OSC) для членов в интерфейсах extensibility поставщика OSC, которые реализует поставщик OSC. Типичные последовательности вызовов иллюстрируют, как и когда OSC использует такие интерфейсы и методы, чтобы лучше определить, как реализовать заданный член в интерфейсе extensibility поставщика. Фактическая последовательность вызовов может отличаться в зависимости от возможностей, возвращаемого методом [ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md) Примеры возможностей: 
  
- Поддержка поставщика для получения, кэшинга или динамического получения друзей и действий из социальной сети.
    
- Пользовательский интерфейс, который osC должен отображать для пользователя.
    
- Тип проверки подлинности (например, проверка подлинности на основе форм), который должен использовать OSC.
    
## <a name="in-this-section"></a>В этом разделе:

- [Обычная проверка](basic-authentication.md)подлинности : описывает типичную последовательность вызовов OSC для поддержки пользователя Office, который входит в социальные сети, если поставщик OSC поддерживает обычную проверку подлинности.
    
- [Проверка](forms-based-authentication.md)подлинности на основе форм : описывает типичную последовательность вызовов OSC для поддержки пользователя Office, который входит в социальные сети, если поставщик OSC поддерживает проверку подлинности на основе форм.
    
- [Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.
    
- [Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.
    
## <a name="reference"></a>Справка

- [Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Связанные разделы

- [Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Примеры шаблонов OSC](osc-sample-templates.md)
  
- [Разработка поставщика с помощью схемы OSC XML](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Отладка поставщика](debugging-a-provider.md)
  
- [Развертывание поставщика](deploying-a-provider.md)
  
- [Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)

