---
title: XML для возможностей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Элемент возможностей в схеме XML поставщика OSC позволяет поставщику OSC указать его функциональность. Такие функции включают в себя следующие функции:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435007"
---
# <a name="xml-for-capabilities"></a>XML для возможностей

Элемент **возможностей в** схеме XML поставщика OSC позволяет поставщику OSC указать его функциональность. Такие функции включают в себя следующие функции: 
  
- Поддерживает ли поставщик получение, кэшинг или динамическое поиск друзей и действий из социальной сети.
    
- Как OSC должен отображать определенные пользовательские интерфейсы с логотипом.
    
- Следует ли osc использовать проверку подлинности на основе форм или автоматически настраивать социальную сеть и журналы пользователя в социальной сети.
    
Схема XML для  возможностей имеет решающее значение, так как определяет для OSC функции, поддерживаемые поставщиком. Поставщик OSC должен реализовать метод [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md) который возвращает _строку результатов._ OsC вызывает **ISocialProvider::GetCapabilities** для получения сведений о возможностях  поставщика OSC в строке результатов, которая  соответствует определению схемы XML для элемента возможностей. Эта информация позволяет последующим звонкам из OSC к поставщику OSC работать правильно. 
  
Чтобы указать возможности поставщика OSC в качестве выходного параметра метода **ISocialProvider::GetCapabilities,** необходимо соответствовать схеме XML-схемы поставщика OSC. На следующем рисунке показаны **возможности** структуры XML. 
  
**Рис. 1. \<возможности \> Структура XML**

![XML-структура возможностей](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Подробные описания детских элементов элемента **возможностей** см. в рублях [Capabilities XML Elements.](capabilities-xml-elements.md) Пример возможностей XML **см.** в [примере Capabilities XML.](capabilities-xml-example.md) Полное определение схемы XML-схемы поставщика OSC, в том числе необходимых или необязательных элементов, см. в Outlook [social Connector Provider XML Schema.](outlook-social-connector-provider-xml-schema.md)
  
## <a name="see-also"></a>См. также

- [Пример XML возможностей](capabilities-xml-example.md)  
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md)  
- [XML для друзей](xml-for-friends.md)  
- [XML для действий](xml-for-activities.md)
- [Разработка поставщика с помощью схемы XML OSC](developing-a-provider-with-the-osc-xml-schema.md)

