---
title: XML для возможностей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Элемент capabilities в XML-схеме поставщика (OSC) позволяет поставщика OSC указать его функциональные возможности. Такая функциональная возможность включает в себя следующее:'
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812838"
---
# <a name="xml-for-capabilities"></a>XML для возможностей

Элемент **capabilities** в XML-схеме поставщика (OSC) позволяет поставщика OSC указать его функциональные возможности. Такая функциональная возможность включает в себя следующее: 
  
- Поддерживает ли поставщик начало, кэширование или динамически поиск друзей и действия из социальных сетей.
    
- OSC отображение определенных пользовательских интерфейсов входа в систему.
    
- Ли OSC следует использовать проверку подлинности на основе форм или автоматической настройки социальной сети и журналы на пользователя в социальных сетях.
    
XML-схемы для **возможности** крайне важна, так как он определяет для OSC функциональных возможностей, поддерживаемых поставщиком. Поставщика OSC необходимо реализовать метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , который возвращает _результирующую_ строку. OSC вызывает **ISocialProvider::GetCapabilities** для получения сведений о возможностях поставщика OSC в _результирующую_ строку, которой соответствует определение схемы XML для элемента **capabilities** . Эта информация включает последующие вызовы из OSC поставщика OSC для правильной работы. 
  
Чтобы указать возможности поставщика OSC в качестве выходного параметра метода **ISocialProvider::GetCapabilities** , должен соответствовать типу схемы XML возможности расширения поставщика OSC. На следующем рисунке показана XML-структура **возможностей** . 
  
**На рисунке 1. \<возможности\> XML-структура**

![XML-структура возможностей](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
Подробное описание дочерние элементы элемента **capabilities** в разделе [Возможности XML-элементы](capabilities-xml-elements.md). [Пример XML возможности](capabilities-xml-example.md) **возможности** XML, см. Полное определение схемы XML поставщика OSC, включая, какие элементы являются обязательный или необязательный см в [Outlook Social Connector поставщика XML-схему](outlook-social-connector-provider-xml-schema.md).
  
## <a name="see-also"></a>См. также

- [Пример возможности XML](capabilities-xml-example.md)  
- [Синхронизация друзей и действия](synchronizing-friends-and-activities.md)  
- [XML-код для друзей](xml-for-friends.md)  
- [XML-код для действия](xml-for-activities.md)
- [Разработка поставщика с использованием схемы XML для OSC](developing-a-provider-with-the-osc-xml-schema.md)

