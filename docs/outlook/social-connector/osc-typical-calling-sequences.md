---
title: Типичные последовательности вызовов OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: В этом разделе описываются типичные последовательности вызовов Outlook social Connector (OSC) членов в интерфейсах extensibility поставщика OSC, которые реализует поставщик OSC.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413614"
---
# <a name="osc-typical-calling-sequences"></a>Типичные последовательности вызовов OSC

В этом разделе описываются типичные последовательности вызовов Outlook social Connector (OSC) членов в интерфейсах extensibility поставщика OSC, которые реализует поставщик OSC. Типичные последовательности вызовов иллюстрируют, как и когда OSC использует такие интерфейсы и методы, чтобы лучше определить, как реализовать данный член в интерфейсе extensibility поставщика. Фактическая последовательность вызовов может варьироваться в зависимости от возможностей, возвращаемого методом [ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md) Примеры возможностей включают следующие: 
  
- Поддержка поставщика для получения, кэшинга или динамического получения друзей и действий из социальной сети.
    
- Пользовательский интерфейс, который OSC должен отображать для логоса пользователя.
    
- Тип проверки подлинности (например, проверка подлинности на основе форм), который должен использовать OSC.
    
## <a name="in-this-section"></a>В этом разделе

- [Базовая](basic-authentication.md)проверка подлинности. Описывает типичную последовательность вызовов OSC для поддержки пользователя, который Office, войдя в социальную сеть, если поставщик OSC поддерживает базовую проверку подлинности.
    
- [Проверка](forms-based-authentication.md)подлинности на основе форм. Описывает типичную последовательность вызовов OSC для поддержки пользователя Office, который входит в социальную сеть, если поставщик OSC поддерживает проверку подлинности на основе форм.
    
- [Получение действий](getting-activities.md). Описывает типичную последовательность вызовов OSC для синхронизации действий друзей пользователя Office из социальной сети, если поставщик osc социальной сети поддерживает синхронизацию действий.
    
- [Получение сведений](getting-friends-information.md)о друзьях. Описывает типичную последовательность вызовов OSC для синхронизации списка друзей Office пользователя из социальной сети, если поставщик osc социальной сети поддерживает кэширование контактов.
    
## <a name="reference"></a>Справочные материалы

- [Outlook Справка о поставщике социальных соединители](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Связанные разделы

- [Начало работы с разработкой Outlook поставщика социальных соединители](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Шаблоны образцов OSC](osc-sample-templates.md)
  
- [Разработка поставщика с помощью схемы XML OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Отладка поставщика](debugging-a-provider.md)
  
- [Развертывание поставщика](deploying-a-provider.md)
  
- [Лучшие практики для разработки поставщика](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)

