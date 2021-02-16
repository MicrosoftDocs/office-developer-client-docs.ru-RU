---
title: Краткое руководство по разработке поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: В этом разделе предлагается несколько действий, чтобы узнать о разработке поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424219"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Краткое руководство по разработке поставщика

Чтобы разработать поставщика OSC, необходимо выполнить следующие общие действия:
  
- Реализуют четыре обязательных интерфейса: [ISocialProvider,](isocialprovideriunknown.md) [ISocialSession,](isocialsessioniunknown.md) [ISocialProfile](isocialprofileisocialperson.md)и [ISocialPerson.](isocialpersoniunknown.md) В зависимости от поддержки вашей социальной сети для кэшации учетных данных для входа, после пользователя в социальной сети или динамической синхронизации друзей и их действий, может потребоваться реализовать [интерфейс ISocialSession2.](isocialsession2iunknown.md) 
    
- Параллельно с реализацией интерфейсов протестировать и отлалать поставщика OSC. 

- Развертывание поставщика OSC.  

- Завершите тестирование перед выпуском.
    
## <a name="step-a-implementing-interfaces"></a>Шаг А. Реализация интерфейсов

Поставщик OSC реализует интерфейсы, чтобы osC могли использовать эти интерфейсы для получения необходимой информации о социальных сетях или из нее через поставщика OSC. К таким сведениям относятся следующие:
  
- Как представить пользователю диалоговое окно для учетной записи для пользователя.    
- Поддерживает ли поставщик отображение друзей или действий в социальных сетях.    
- Отображение друзей и действий в карточке контакта или области людей Outlook.     
- Когда обновлять сведения о друзьях или действиях на карточке контакта или в области "Люди".
    
Как правило, сведения передаются от поставщика в OSC в виде строк XML в качестве выходных параметров методов интерфейса. OsC и поставщик OSC соответствуют XML-схеме поставщика OSC. Поэтому в процессе реализации интерфейсов необходимо хорошо понимать, как схема XML позволяет указать сведения, указанные выше. 

В следующих ресурсах объясняется, как указать XML для возможностей поставщика, друзей и действий:
  
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)    
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md)    
- [XML-пример возможностей](capabilities-xml-example.md)   
- [XML для возможностей](xml-for-capabilities.md)    
- [Пример XML-разных друзей](friends-xml-example.md)    
- [XML для друзей](xml-for-friends.md)   
- [Пример XML-канала активности](activity-feed-xml-example.md)   
- [XML для действий](xml-for-activities.md)
    
Перед началом реализации также проконсультируйтесь со следующими разделами, чтобы сэкономить время в процессе отладки:
  
- [Технические требования](technical-requirements.md)    
- [Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md)    
- [Примеры шаблонов OSC](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Шаг Б. Отладка

В разделе ["Отладка поставщика"](debugging-a-provider.md) предложены процедуры отладки, которые можно использовать при разработке поставщика OSC. 
  
Во время разработки вы также можете сослаться на статью "Готовность к выпуску поставщика [OSC",](getting-ready-to-release-an-osc-provider.md) чтобы лучше понять ожидаемое поведение в определенных сценариях (например, при базовой и проверке подлинности на основе форм). 
  
## <a name="step-c-deploying"></a>Шаг C. Развертывание

Чтобы узнать о требованиях к развертыванию, см. следующие разделы:
  
- [Развертывание поставщика](deploying-a-provider.md)    
- [Регистрация поставщика](registering-a-provider.md)   
- [Контрольный список установки](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Шаг D. Окончательное тестирование перед выпуском

В зависимости от социальной сети и поставщика OSC обычно существуют специальные тесты, которые необходимо выполнить перед выпуском поставщика. Рекомендуемый список тестов см. в [подготовии к выпуску поставщика OSC.](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a>См. также

- [Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

