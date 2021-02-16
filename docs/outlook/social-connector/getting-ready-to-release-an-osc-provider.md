---
title: Getting ready to release an OSC provider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: В этом разделе предлагаются тесты, которые можно сделать перед выпуском поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414664"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Getting ready to release an OSC provider

В этом разделе предлагаются тесты, которые можно сделать перед выпуском поставщика Outlook Social Connector (OSC). Вы можете начать со ссылками на разделы этого раздела и выполнить некоторые из этих тестов на этапах разработки и тестирования, но эти тесты должны быть выполнены к моменту выпуска. 

Эти тесты проверяют базовую функциональность реализации интерфейсов поставщика OSC в отношении возможностей, указанных для поставщика OSC. Кроме того, несмотря на то что OSC является функцией, совместно используемой несколькими клиентские приложения Office, в этих тестах используется Outlook в качестве клиента для тестирования основных функций. Необходимо определить, необходимы ли другие тесты для функций, характерных для вашего поставщика.
  
## <a name="in-this-section"></a>В этом разделе:

- [Тестирование развертывания](testing-deployment.md): описываются сценарии, на которые следует проверить установку и установку поставщика OSC.
    
- [Тестирование возможностей, проверки](testing-capabilities-authentication-and-configuration.md)подлинности и конфигурации : описывает тесты для получения возможностей и сценарии настройки учетной записи и проверки подлинности пользователя в социальной сети.
    
- [Testing Following and Stop-Following Persons](testing-following-and-stop-following-persons.md): Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network. 
    
- [Тестирование друзей](testing-friends.md): описывает тесты и сценарии, чтобы убедиться, что поставщик OSC правильно возвращает данные друзей и других пользователей, где это применимо, в зависимости от режима синхронизации, поддерживаемого поставщиком.
    
- [Действия](testing-activities.md)по тестированию : описываются тесты и сценарии для проверки того, что поставщик OSC правильно возвращает действия друзей и других, если применимо, в зависимости от режима синхронизации, поддерживаемого поставщиком.
    
## <a name="reference"></a>Справка

- [Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Связанные разделы

- [Примеры шаблонов OSC](osc-sample-templates.md)
  
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)
  
- [Разработка поставщика с помощью схемы OSC XML](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Отладка поставщика](debugging-a-provider.md)
  
- [Развертывание поставщика](deploying-a-provider.md)
  

