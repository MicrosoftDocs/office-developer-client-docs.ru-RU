---
title: XML для действий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: В этом разделе содержится пример сценария, который показывает поставщика Outlook Social Connector (OSC) API расширяемости звонков, при которых реализует поставщика OSC и OSC делает для получения сведений о действиях. Сведения представлены в строки XML, которые соответствуют XML-схему поставщика OSC.
ms.openlocfilehash: 44f74d9e72eec3ff6da7f9967315fc9d75191584
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812852"
---
# <a name="xml-for-activities"></a>XML для действий

В этом разделе содержится пример сценария, который показывает поставщика Outlook Social Connector (OSC) API расширяемости звонков, при которых реализует поставщика OSC и OSC делает для получения сведений о действиях. Сведения представлены в строки XML, которые соответствуют XML-схему поставщика OSC.
  
Схема XML поставщика OSC позволяет поставщика OSC определение действия. Информация о действия может включать социальных сетей, где веб-канала активности элементов была создана, сведения о каждого элемента веб-канал активности (такие как владелец, введите и дата действия публикации) и шаблон для отображения действия. Чтобы обеспечить поддержку действий отображение в области пользователей или в карточке контакта, поставщика OSC социальной сети необходимо реализовать и возвращает правильный действия XML. Пример активности веб-канала XML, пример [XML веб-канала активности](activity-feed-xml-example.md). Дополнительные сведения о синхронизации друзей действий можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md). Полное определение схемы XML поставщика OSC, включая, какие элементы являются обязательный или необязательный см в [Outlook Social Connector поставщика XML-схему](outlook-social-connector-provider-xml-schema.md). 
  
В следующем сценарии OSC динамически синхронизирует действий для человека, выбранного в области пользователей и возвращает подробные сведения об этом человеке:
  
1. Поставщика OSC, которая поддерживает синхронизацию по требованию действий указывает, что для OSC с помощью элементов **getActivities** и **dynamicActivitiesLookupEx** . Поставщика OSC также задает элемент **hashFunction** . Все три элемента являются дочерними элементами **возможностей**. 
    
2. Поставщика OSC реализует методы **ISocialProvider::GetCapabilities** и [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . 
    
3. Вызовов OSC **ISocialProvider::GetCapabilities** для проверки значения **getActivities** и **dynamicActivitiesLookupEx** чтобы убедиться, что поставщика OSC поддерживает синхронизацию по требованию действий. OSC также указывается значение элемента **hashFunction** , поддерживаемых поставщиком OSC. 
    
4. OSC обновляет области пользователей или карточки контакта, чтобы позволить пользователю видеть последние действия выбранного пользователя. OSC шифрует его SMTP-адреса с помощью хэш-функции, заданная в элементе **hashFunction** формирование XML-строка, которая соответствует определение схемы XML для элемента **hashedAddresses** . 
    
5. OSC вызывает **ISocialSession2::GetActivitiesEx**, предоставление XML-строка хэш адреса в качестве параметра _hashedAddresses_ , чтобы получить текущий набор операций этого контакта с помощью параметра _действия_ . Строки _действий_ параметра соответствует определение схемы XML в элемент **activityFeed** . 
    
6. На основании определения схемы XML для **activityFeed**, OSC дальнейшей анализирует строку _действия_ , которую нужно получить тип, публикация Дата и другие сведения о каждой операции и способ отображения действия. 
    
7. Чтобы получить подробные сведения о выбранного пользователя, OSC вызывает [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md), предоставляя же XML-строка хэш адресов в качестве аргумента для параметра _personsAddresses_ . Подробные сведения об этом человеке возвращаются в параметре _personsCollection_ . Эти сведения могут включать **firstName**, **lastName**и **emailAddress**. Параметр _personsCollection_ соответствует определение схемы XML для элемента **контакта** . 
    
Можно найти дополнительные сведения о настройке XML для действия в следующих разделах в этом разделе:
  
- [Общие сведения о XML-код для действия элемента веб-канала](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails элемент](activitydetails-element.md)
    
- [activityTemplateContainer элемент](activitytemplatecontainer-element.md)
    
- [Переменные шаблона](template-variables.md)
    
- [Рекомендации для правильного отображения действий](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>См. также

- [Пример XML веб-канала активности](activity-feed-xml-example.md)  
- [Синхронизация друзей и действия](synchronizing-friends-and-activities.md) 
- [XML-код для возможности](xml-for-capabilities.md)  
- [XML-код для друзей](xml-for-friends.md)
- [Разработка поставщика с использованием схемы XML для OSC](developing-a-provider-with-the-osc-xml-schema.md)

