---
title: XML для возможностей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Элемент capabilities в XML-схеме поставщика OSC позволяет поставщику OSC указывать его функции. К таким функциям относятся следующие:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435007"
---
# <a name="xml-for-capabilities"></a>XML для возможностей

Элемент **capabilities** в XML-схеме поставщика OSC позволяет поставщику OSC указывать его функции. К таким функциям относятся следующие: 
  
- Поддерживает ли поставщик получение, кэшинг или динамический поиск друзей и действий из социальной сети.
    
- Как OSC должен отображать определенные пользовательские интерфейсы для логотипа.
    
- Должен ли OSC использовать проверку подлинности на основе форм или автоматически настраивать социальные сети и журналы пользователя в социальной сети.
    
Схема XML для  возможностей имеет критическое значение, так как она определяет для OSC функции, поддерживаемые поставщиком. Поставщик OSC должен реализовать метод [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md) который возвращает строку _результата._ OsC вызывает **ISocialProvider::GetCapabilities** для получения сведений о возможностях  поставщика OSC в строке результата, которая соответствует определению схемы XML для элемента **возможностей.** Эти сведения обеспечивают правильную работу последующих вызовов из OSC к поставщику OSC. 
  
Чтобы указать возможности поставщика OSC в качестве выходного параметра метода **ISocialProvider::GetCapabilities,** необходимо соблюдать XML-схему extensibility поставщика OSC. На следующем рисунке **показана XML-структура** возможностей. 
  
**Рисунок 1. \<capabilities \> Структура XML**

![XML-структура возможностей](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Подробные описания child elements элемента **capabilities** см. в описании [XML-элементов Capabilities.](capabilities-xml-elements.md) Пример возможностей XML **см. в** [XML-примере](capabilities-xml-example.md)возможностей. Полное определение XML-схемы поставщика OSC, включая элементы, которые являются обязательными или необязательными, см. в XML-схеме поставщика [Outlook Social Connector.](outlook-social-connector-provider-xml-schema.md)
  
## <a name="see-also"></a>См. также

- [XML-пример возможностей](capabilities-xml-example.md)  
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md)  
- [XML для друзей](xml-for-friends.md)  
- [XML для действий](xml-for-activities.md)
- [Разработка поставщика с помощью схемы OSC XML](developing-a-provider-with-the-osc-xml-schema.md)

