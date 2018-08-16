---
title: Имена свойств и наборы свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c586d70054542e8d20c90a8caceafabbbb408de8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812108"
---
# <a name="property-names-and-property-sets"></a>Имена свойств и наборы свойств

  
  
**Относится к**: Outlook 
  
Имя каждого именованного свойства состоит из двух частей:
  
- Глобальный уникальный идентификатор, или идентификатор GUID, определяющий набор свойств.
    
- Строка Юникода символ или числовое значение 32-разрядная версия. 
    
Имена именованных свойств, описаны с помощью структуры [MAPINAMEID](mapinameid.md) . Эта структура содержит членом набора свойств, члена для указания имени в формате числовое или строковое и члена для идентификации используется формат. Так как набор свойств является частью имя свойства, не необязательно. MAPI определил несколько наборов свойств для использования клиентами и поставщиков услуг, но если существующий набором свойств не подходит, можно определить новый набор свойств. Клиенты и поставщиков услуг можно определить собственные наборы свойств с помощью вызова функции [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) . Обычно эти наборы свойств создаются для пользовательских клиентских приложений. 
  
Наборы свойств MAPI представлены следующие константы:
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
Набор свойств PS_MAPI зарезервирован; используется поставщиками услуг для создания имен для свойств с идентификаторами ниже диапазона именованное свойство. Набор свойств PS_PUBLIC_STRINGS используется клиентами для именованных свойств сообщения IPM. Так как имя свойства в набор свойств PS_PUBLIC_STRINGS отображаются в пользовательский интерфейс клиента, невидимый сообщения, такие как те, которые относятся к классу сообщения производственных Издержек следует избегать создания именованных свойств с набором свойств. Вместо этого они создают свойства в диапазоне конкретного класса сообщений, 0x6800 через 0x7FFF.
  
Другие наборы свойств удержание именованного свойства, описывающие получателей, которые обычно являются членами маршрутизации списка. Содержащий же тип данных как свойства, связанные со свойствами получателя списка свойств в эти наборы свойств распознаются шлюзов требуется сопоставление для целевой системы обмена сообщениями. Поскольку существует пять типов данных, содержащие свойства, MAPI определенные наборы пяти различных свойств. Задает отправке сообщение, в котором необходимо включить для его маршрутизации элементы списка адресов и тип адреса назначает именованного свойства для каждого элемента в PS_ROUTING_EMAIL_ADDRESSES и свойство PS_ROUTING_ADDRTYPE клиента. Это гарантирует, что адрес и тип адреса остаются приемлемым при отправке внешнюю систему обмена сообщениями.
  
## <a name="see-also"></a>См. также



[Именованные свойства MAPI](mapi-named-properties.md)
