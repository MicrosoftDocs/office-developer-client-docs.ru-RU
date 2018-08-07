---
title: Типичные последовательности вызовов OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: В этом разделе описываются типичные последовательности вызовов Outlook Social Connector (OSC) членов в интерфейсы возможности расширения поставщика OSC, которые реализует поставщика OSC.
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812828"
---
# <a name="osc-typical-calling-sequences"></a>Типичные последовательности вызовов OSC

В этом разделе описываются типичные последовательности вызовов Outlook Social Connector (OSC) членов в интерфейсы возможности расширения поставщика OSC, которые реализует поставщика OSC. Как и когда иллюстрируют типичные последовательности вызовов OSC используются такие интерфейсы и методы, позволяющие лучше определить, как реализовать данный элемент на интерфейс расширения поставщика. Фактическая последовательность вызова могут различаться в зависимости от возможностей, возвращенный методом [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) . Примеры возможностей: 
  
- Поставщик поддерживает для получения, кэширование и динамически поиск друзей и действия из социальных сетей.
    
- Пользовательский интерфейс, который OSC должны отображать для входа пользователя в систему.
    
- Тип проверки подлинности (например, на основе форм проверки подлинности), который следует использовать OSC.
    
## <a name="in-this-section"></a>В этой статье

- [Обычная проверка подлинности](basic-authentication.md): описывается типичное вызывающего последовательность OSC для поддержки для Office пользователя, вошедшего в социальной сети, если поставщик OSC поддерживает обычную проверку подлинности.
    
- [Проверка подлинности на основе форм](forms-based-authentication.md): описание типичная последовательность вызовов OSC для поддержки для Office пользователя, вошедшего в социальной сети, если поставщик OSC поддерживает проверку подлинности на основе форм.
    
- [Начало действий](getting-activities.md): описывает типичное вызывающего последовательность OSC для синхронизации действий пользователя Office друзей из социальных сетей, если поставщика OSC социальной сети поддерживает синхронизацию действий.
    
- [Получение сведений о друзьях](getting-friends-information.md): описывает типичное вызывающего последовательность OSC синхронизировать список друзей пользователя Office из социальных сетей, если поставщика OSC социальной сети поддерживает кэшированные синхронизации контактов.
    
## <a name="reference"></a>Справочные материалы

- [Справочник поставщика по Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Связанные разделы

- [Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Шаблоны OSC примера](osc-sample-templates.md)
  
- [Разработка поставщика с использованием схемы XML для OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Отладка поставщика](debugging-a-provider.md)
  
- [Развертывание поставщика](deploying-a-provider.md)
  
- [Рекомендации по разработке поставщика](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>См. также

- [XML-код для возможности](xml-for-capabilities.md)

