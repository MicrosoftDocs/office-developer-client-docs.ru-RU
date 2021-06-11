---
title: Обзор XML для элемента веб-канала активности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Канал действий состоит из одной или нескольких действий, происходящих в социальной сети. Каждая лента действий представлена элементом activityFeed и характеризуется этими тремя частями информации:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439949"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Обзор XML для элемента веб-канала активности

Канал действий состоит из одной или нескольких действий, происходящих в социальной сети. Каждая лента действий представлена элементом **activityFeed** и характеризуется этими тремя частями информации: 
  
- **network**—Name of the social network from which the activities originated.
    
- **действия**— контейнер для действий, происходящих в учетной записи пользователя в этой социальной сети.
    
- **шаблоны**— контейнер для шаблонов, используемых для отображения соответствующего элемента активности в **действиях.**
    
Чтобы создать элемент ленты действий, необходимо соответствовать схеме XML Outlook поставщика Outlook (OSC). На рисунке 1 показана структура XML-канала активности.
  
**Рис. 1. Структура XML-канала активности**

![XML-структура новостей](media/odc_ol14_ta_OSC_Fig06.gif)
  
Для каждого элемента ленты действий наиболее важными частями этой схемы являются элементы **activityDetails** и **activityTemplateContainer:** 
  
- Элемент **activityDetails** хранит определенные сведения для каждого элемента ленты действий, например имя владельца действия или URL-адрес для загруженных изображений. 
    
- Элемент **activityTemplateContainer** сохраняет формат или макет для каждого элемента ленты действий. Он состоит из шаблонов, представленных отдельными элементами **activityTemplate,** которые можно повторно использовать для нескольких элементов питания. 
    
Для отдельного элемента ленты действий элемент **activityTemplate** указывает следующие четыре части информации: 
  
- **значок**— указывает URL-адрес для значка для отображения элемента ленты действий.
    
- **заголовок**—Описывает элемент ленты действий.
    
- **тип**— указывает тип действий, таких как обновление состояния, фотографии или документа.
    
- **данные**— указывает любую дополнительную информацию, отображаемую с помощью элемента ленты действий.
    
> [!TIP]
> Значок, отображаемый в ленте действий, всегда такой же, как и значок поставщика, возвращенный свойством **ISocialProvider::SocialNetworkIcon.** 
  
Дополнительные сведения о элементе **activityDetails,** **элементе activityTemplateContainer,** маркерах шаблонов и переменных шаблонов см. ниже. 
  
- [элемент activityDetails](activitydetails-element.md)
    
- [элемент activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Переменные шаблона](template-variables.md)
    
- [Рекомендации для правильного отображения действий](guidelines-for-properly-displaying-activities.md)
    
Пример XML-канала активности см. в [примере Activity Feed XML.](activity-feed-xml-example.md)
  
## <a name="see-also"></a>См. также

- [XML для действий](xml-for-activities.md) 
- [Outlook Схема поставщика социальных соединителем XML](outlook-social-connector-provider-xml-schema.md)
- [Разработка поставщика с помощью схемы XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

