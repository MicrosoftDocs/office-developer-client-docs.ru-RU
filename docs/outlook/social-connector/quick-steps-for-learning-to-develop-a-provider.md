---
title: Краткое руководство по разработке поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: В этом разделе предлагается несколько действий, чтобы узнать о разработке поставщика Outlook social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424219"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Краткое руководство по разработке поставщика

Чтобы разработать поставщика OSC, необходимо выполнить следующие общие действия:
  
- Реализация четырех обязательных интерфейсов: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)и [ISocialPerson](isocialpersoniunknown.md). В зависимости от поддержки вашей социальной сети для кэшации учетных данных с логотипами, после пользователя в социальной сети или динамической синхронизации друзей и их действий можно реализовать интерфейс [ISocialSession2.](isocialsession2iunknown.md) 
    
- Параллельно с реализацией интерфейсов тестировать и отлагировать поставщика OSC. 

- Развертывание поставщика OSC.  

- Сделайте окончательное тестирование перед выпуском.
    
## <a name="step-a-implementing-interfaces"></a>Шаг A. Реализация интерфейсов

Поставщик OSC реализует интерфейсы, чтобы osC могли использовать эти интерфейсы для получения необходимой информации о социальной сети или из нее через поставщика OSC. Такие сведения включают в себя следующие сведения:
  
- Как представить пользователю диалоговое окно логотипа учетной записи.    
- Поддерживает ли поставщик показ друзей или действия, отображаемые в социальной сети.    
- Отображение друзей и действий в контактной карте или Outlook области.     
- При обновлении сведений о друзьях или действиях на контактной карте или в области людей.
    
Как правило, информация передается от поставщика в OSC в виде строк XML в качестве выходных параметров методов интерфейса. И OSC, и поставщик OSC соответствуют схеме XML поставщика OSC. Поэтому в процессе реализации интерфейсов необходимо хорошо понимать, как схема XML позволяет указывать сведения, указанные выше. 

В следующих ресурсах объясняется, как указать XML для возможностей, друзей и действий поставщика:
  
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)    
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md)    
- [Пример XML возможностей](capabilities-xml-example.md)   
- [XML для возможностей](xml-for-capabilities.md)    
- [Пример XML Friends](friends-xml-example.md)    
- [XML для друзей](xml-for-friends.md)   
- [Пример ленты действий XML](activity-feed-xml-example.md)   
- [XML для действий](xml-for-activities.md)
    
Прежде чем приступить к реализации, также проконсультируйтесь со следующими разделами, чтобы сэкономить время в процессе отладки:
  
- [Технические требования](technical-requirements.md)    
- [Лучшие практики для разработки поставщика](best-practices-for-developing-a-provider.md)    
- [Шаблоны образцов OSC](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Шаг B. Отладка

В разделе [Отладка](debugging-a-provider.md) поставщика предлагает отладку процедур, которые можно использовать при разработке поставщика OSC. 
  
Во время разработки можно также сослаться на статью [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behaviour in certain scenarios (for example, basic and forms-based authentication). 
  
## <a name="step-c-deploying"></a>Шаг C. Развертывание

См. следующие разделы, чтобы узнать о требованиях к развертыванию:
  
- [Развертывание поставщика](deploying-a-provider.md)    
- [Регистрация поставщика](registering-a-provider.md)   
- [Контрольный список установки](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Шаг D. Окончательное тестирование перед выпуском

В зависимости от вашей социальной сети и поставщика OSC обычно существуют тесты, определенные для поставщика, которые необходимо выполнить перед выпуском поставщика. Список предлагаемых тестов см. в примере [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>См. также

- [Начало работы с разработкой Outlook поставщика социальных соединители](getting-started-with-developing-an-outlook-social-connector-provider.md)

