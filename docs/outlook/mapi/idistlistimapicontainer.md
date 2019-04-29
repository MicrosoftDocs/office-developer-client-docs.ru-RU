---
title: Идистлист IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431549"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к спискам рассылки в изменяемых контейнерах адресной книги. **Идистлист** позволяет создавать, копировать и удалять списки рассылки, а также выполнять разрешение имен. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объекты списка рассылки  <br/> |
|Реализовано в:  <br/> |Поставщики адресных книг  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_идистлист  <br/> |
|Тип указателя:  <br/> |ЛПДИСТЛИСТ  <br/> |
|Модель транзакции:  <br/> |Транзакции  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

У этого интерфейса нет уникальных методов.
  
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Интерфейс **идистлист** наследуется от [IMAPIContainer](imapicontainerimapiprop.md) и содержит те же методы, что и контейнеры адресных книг. Таким образом, так как методы интерфейса **идистлист** идентичны элементам интерфейса [иабконтаинер](iabcontainerimapicontainer.md) , они не дублируются здесь. 
  
Список рассылки или объект, реализующий **идистлист** — это коллекция объектов пользователя обмена сообщениями или отдельных получателей. Список рассылки может состоять из всех пользовательских объектов обмена сообщениями, а также от некоторых пользователей обмена сообщениями и некоторых списков рассылки. 
  
Обычно существует два типа списков рассылки:
  
- Списки рассылки, развернутые базовой системой обмена сообщениями. Этот тип списка содержит адрес, **пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) и обрабатывается так же, как если бы он был отдельным получателем. 
    
- Списки рассылки, существующие в локальном контейнере и развернутые клиентским приложением.
    
К дополнительным свойствам списка рассылки относятся следующие:
  
- **Пр_ласт_модификатион_тиме** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **Пр_детаилс_табле** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
Обратите внимание, что **пр_аддртипе** является обязательным, но **пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) — нет. Это связано с тем, что список рассылки без адреса электронной почты по-прежнему может получать сообщения, но список его участников должен быть развернут. Если для свойства **пр_аддртипе** задано значение МАПИПДЛ, MAPI выполняет расширение. Если **пр_аддртипе** имеет значение, отличное от мапипдл, то поставщик транспорта выполняет расширение. 
  
Дополнительные сведения об использовании методов **идистлист** приведены в справочных записях для параллельных методов **иабконтаинер**.
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

