---
title: Определение новых свойств MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 666ee413319765e39e25d586208f764afc93ae6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425017"
---
# <a name="defining-new-mapi-properties"></a>Определение новых свойств MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Несмотря на богатство свойств, предоставленных MAPI для использования клиентами и поставщиками услуг, MAPI позволяет при необходимости создавать новые свойства. К числу допустимого сценария определения новых общедоступных свойств относятся клиент, создающий свойства для поддержки нового класса сообщений, и поставщик услуг, создающий новые свойства для размещения уникальных функций системы обмена сообщениями.
  
Обычно поставщику услуг не нужно определять новые свойства для существующего объекта MAPI или класса сообщений. Одно из основных преимуществ использования MAPI состоит в том, что устанавливаются стандартные идентификаторы и форматы для большого количества элементов системы обмена сообщениями, что позволяет пользователям легко смешивать поставщиков услуг и соответствовать их. Поставщики услуг, которые используют нестандартные свойства, также не работают с другими поставщиками услуг. 
  
Клиенты могут создавать свойства контента для новых классов сообщений с помощью:
  
- Использование идентификаторов свойств в определенном диапазоне для свойств контента определенного класса сообщений.
    
    - Или -
    
- Использование именных свойств. 
    
Первый вариант предпочтительный, так как не все поставщики услуг поддерживают названные свойства. MAPI определяет два отдельных диапазона, которые клиенты могут использовать для новых свойств контента класса сообщений:
  
- 0x6800 0x7BFF для передаваемых свойств
    
- 0x7C00 0x7FFF для нетрансмитируемых свойств
    
Идентификаторы свойств должны подпадать в заранее определенные диапазоны, чтобы предотвратить столкновения между свойствами, определенными различными поставщиками или пользователями. Однако пользователи свойств в этих диапазонах не могут делать предположения о поведении свойств. Каждый клиент, создав новый класс сообщений, имеет доступ к этим диапазонам; свойство с идентификатором  _xxxx может_ означать одно поведение для одного класса сообщений, а другое поведение для другого класса сообщений. 
  
Названные свойства используются для того, чтобы гарантировать, что определенное свойство уникально для класса сообщений. Идентификаторы имени свойств начинаются в 0x8000 диапазоне. Клиенты определяют одно или несколько имен, а затем звонят по методу [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) чтобы связать идентификатор с каждым именем. Названные свойства могут использоваться клиентами или поставщиками услуг для определения новых свойств для любого объекта только в том случае, если владелец объекта поддерживает названные свойства. Пользователи этих свойств называют **GetIDsFromNames** и связанный с ними метод **IMAPIProp** [GetNamesFromIDs,](imapiprop-getnamesfromids.md)чтобы составить карту между именем и его идентификатором.
  
Все свойства, новые или существующие, должны использовать набор предопределенных типов свойств. Новые типы свойств не могут быть добавлены, а существующие типы не могут быть изменены или удалены. Простые, маленькие свойства, такие как одноимужные или 16-разрядные свойства, можно хранить в любом соответствующем типе. Например, integers можно хранить как **ULONG** и строки могут храниться как **PT_STRING8**. 
  
Используйте тип **PT_BINARY,** чтобы указать подсчитываемого массива byte. Этот тип свойств полезен для расширения типов данных, которые могут храниться в объекте. Bytes are transmitted in sequence and no assumptions are made about the meaning of the data. Когда клиентская заявка считыет данные из такого свойства, данные не изменяются от того, как они хранились. При перемещении данных по процессорам клиент должен выполнять любые необходимые обмены данными. 
  
## <a name="see-also"></a>См. также



[Обзор свойств MAPI](mapi-property-overview.md)

