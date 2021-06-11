---
title: IDistList IMAPIContainer
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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к спискам рассылки в изменяемых контейнерах адресной книги. Кроме выполнения разрешения **имен, IDistList** может создавать, копировать и удалять списки рассылки. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |Объекты списка рассылки  <br/> |
|Реализовано в:  <br/> |Поставщики адресных книг  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IDistList  <br/> |
|Тип указателя:  <br/> |LPDISTLIST  <br/> |
|Модель транзакции:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

Этот интерфейс не имеет уникальных методов.
  
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)  <br/> |Чтение и запись  <br/> |
|**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |Чтение и запись  <br/> |
|**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Интерфейс **IDistList** наследуется [от IMAPIContainer](imapicontainerimapiprop.md) и включает те же методы, что и контейнеры адресной книги. Поэтому, поскольку методы интерфейса **IDistList** идентичны методам интерфейса [IABContainer,](iabcontainerimapicontainer.md) они не дублируются здесь. 
  
Список рассылки или объект, реализующий **IDistList,** — это коллекция объектов пользователей обмена сообщениями или отдельных получателей. Список рассылки может состоять из всех объектов пользователей обмена сообщениями, а также некоторых пользователей сообщений и некоторых списков рассылки. 
  
Обычно существует два типа списков рассылки:
  
- Списки рассылки, расширенные системой обмена сообщениями. Этот тип списка имеет адрес **PR_EMAIL_ADDRESS** [(PidTagEmailAddress),](pidtagemailaddress-canonical-property.md)и рассматривается так же, как если бы он был отдельным получателем. 
    
- Списки рассылки, которые существуют в локальном контейнере и расширяются клиентского приложения.
    
Дополнительные свойства списка рассылки включают следующие:
  
- **PR_LAST_MODIFICATION_TIME** [(PidTagLastModificationTime)](pidtaglastmodificationtime-canonical-property.md)
    
- **PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md) 
    
- **PR_DETAILS_TABLE** [(PidTagDetailsTable)](pidtagdetailstable-canonical-property.md) 
    
Обратите **внимание, PR_ADDRTYPE** требуется, **но** PR_EMAIL_ADDRESS [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)нет. Это потому, что список рассылки без адреса электронной почты по-прежнему может получать сообщения, но его список участников должен быть расширен. Если **свойство PR_ADDRTYPE** mapIPDL, MAPI выполняет расширение. Если **PR_ADDRTYPE** значение, помимо MAPIPDL, поставщик транспорта выполняет расширение. 
  
Дополнительные сведения об использовании методов **IDistList** см. в справочных записях для параллельных методов **IABContainer.**
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

