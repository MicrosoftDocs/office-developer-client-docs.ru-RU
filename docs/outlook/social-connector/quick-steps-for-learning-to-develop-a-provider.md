---
title: Краткое руководство по разработке поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: В данном разделе приводятся некоторые действия, чтобы узнать о разработки поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 345e8600c704504be091ee23c66b7f85575cde90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812835"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Краткое руководство по разработке поставщика

Разработка поставщика OSC, необходимо выполнить следующие действия:
  
- Реализация четыре обязательные интерфейсы: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)и [ISocialPerson](isocialpersoniunknown.md). В зависимости от поддержки социальной сети для кэширования учетные данные для входа, отслеживание человека на социальные сети, или динамически синхронизации друзей и их действий требуется реализовать интерфейс [ISocialSession2](isocialsession2iunknown.md) . 
    
- В рамках реализации интерфейсов тестирование и отладка поставщика OSC. 

- Развертывание поставщика OSC.  

- Выполните окончательный тестирование перед выпуском.
    
## <a name="step-a-implementing-interfaces"></a>Шаг а: реализация интерфейсов

Поставщика OSC реализует интерфейсы, чтобы OSC могут использовать эти интерфейсы для получения необходимых сведений о или из социальных сетей через поставщика OSC. Такая информация включает в себя следующее:
  
- Как представить диалоговое окно входа в систему учетную запись пользователя.    
- Поставщик поддерживает ли отображение друзей или действия, которые отображаются в социальных сетях.    
- Способ отображения друзей и действий в карточке контакта или области пользователей Outlook.     
- Когда следует обновить данные о друзьях или действия в карточке контакта или в области пользователей.
    
Сведения о обычно передается от поставщика OSC в виде строки XML как выходные параметры методов интерфейса. OSC и поставщика OSC соответствует схеме XML поставщика OSC. Таким образом в реализации интерфейсов, необходимо понять, как XML-схему позволяет указать сведения, как указано выше. 

Ознакомьтесь со следующими ресурсами объясняется, как указать XML для возможности поставщика, друзей и действий:
  
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)    
- [Синхронизация друзей и действия](synchronizing-friends-and-activities.md)    
- [Пример возможности XML](capabilities-xml-example.md)   
- [XML-код для возможности](xml-for-capabilities.md)    
- [Пример XML друзей](friends-xml-example.md)    
- [XML-код для друзей](xml-for-friends.md)   
- [Пример XML веб-канала активности](activity-feed-xml-example.md)   
- [XML-код для действия](xml-for-activities.md)
    
Прежде чем начать реализации, также можно найти следующие разделы для экономии времени в процесс отладки.
  
- [Технические требования](technical-requirements.md)    
- [Рекомендации по разработке поставщика](best-practices-for-developing-a-provider.md)    
- [Шаблоны OSC примера](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Отладка Шаг б.

Раздел [Отладка поставщика](debugging-a-provider.md) предлагает отладку процедур, которые можно использовать при разработке поставщика OSC. 
  
При разработке, также можно обратиться к и [Подготовка к выпуску поставщика OSC](getting-ready-to-release-an-osc-provider.md) лучше понимать поведение характерно для некоторых сценариях (например, основной и на основе форм проверки подлинности). 
  
## <a name="step-c-deploying"></a>Развертывание шаг C:

Содержатся в следующих разделах, чтобы узнать о требованиях к развертыванию:
  
- [Развертывание поставщика](deploying-a-provider.md)    
- [Регистрация поставщика](registering-a-provider.md)   
- [Контрольный список установки](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Шаг D: тестирование перед выпуском последний

В зависимости от социальной сети и поставщика OSC существует обычно поставщика тестов, необходимо выполнить перед выпуском ваш поставщик. Предлагаемые список тестов в разделе [Подготовка к выпуску поставщика OSC](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>См. также

- [Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

