---
title: XML для возможностей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Элемент capabilities в схеме XML поставщика (OSC) позволяет поставщику OSC указать его функциональность. К таким функциям относятся следующие:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435007"
---
# <a name="xml-for-capabilities"></a>XML для возможностей

Элемент **capabilities** в схеме XML поставщика (OSC) позволяет поставщику OSC указать его функциональность. К таким функциям относятся следующие: 
  
- Поддерживает ли поставщик возможность получения, кэширования или динамического поиска друзей и действий из социальных сетей.
    
- Как OSC должен отображать определенные пользовательские интерфейсы входа в систему.
    
- Должен ли OSC использовать проверку подлинности на основе форм или автоматически настраивать социальные сети и выполнять вход в систему пользователя в социальной сети.
    
Схема XML для **возможностей** очень важна, так как она указывает на OSC функции, поддерживаемые поставщиком. Поставщик OSC должен реализовать метод [исоЦиалпровидер:: Capabilities](isocialprovider-getcapabilities.md) , который возвращает строку _результата_ . OSC вызывает метод **исоЦиалпровидер::-Capabilities** для получения сведений о возможностях поставщика OSC в _результирующей_ строке, которая соответствует определению схемы XML для элемента **capabilities** . Эта информация позволяет последующим вызовам из OSC в поставщик OSC работать правильно. 
  
Чтобы указать возможности поставщика OSC в качестве выходного параметра метода **исоЦиалпровидер::-Capabilities** , необходимо соответствовать схеме расширяемости поставщика OSC XML. На следующем рисунке показана структура XML **возможностей** . 
  
**Рис. 1. \<структура\> XML возможностей**

![XML-структура возможностей](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Подробное описание дочерних элементов элемента **capabilities** представлено в статье [Elements XML Elements](capabilities-xml-elements.md). Пример XML-кода **возможностей** представлен в статье [пример возможностей XML](capabilities-xml-example.md). Полное определение XML-схемы поставщика OSC, в том числе элементов, обязательных или необязательных, можно найти в статье [схема XML поставщика социальных соединителей Outlook](outlook-social-connector-provider-xml-schema.md).
  
## <a name="see-also"></a>См. также

- [Пример XML-кода возможностей](capabilities-xml-example.md)  
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md)  
- [XML для друзей](xml-for-friends.md)  
- [XML для действий](xml-for-activities.md)
- [Разработка поставщика с помощью XML-схемы OSC](developing-a-provider-with-the-osc-xml-schema.md)

