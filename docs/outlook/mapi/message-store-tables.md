---
title: Таблицы хранилища сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405354"
---
# <a name="message-store-tables"></a>Таблицы хранилища сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Таблица "хранилище сообщений" содержит сведения о поставщиках хранилища сообщений в текущем профиле. Для каждого сеанса MAPI существует одна таблица хранилища сообщений, реализованная MAPI и используемая клиентами. Клиенты могут использовать эту таблицу, например, для обнаружения всех экземпляров определенного поставщика или для обнаружения определенного хранилища сообщений. 
  
Таблица хранилища сообщений является динамической. Если пользователь клиентского приложения изменяет профиль, изменяя хранилище сообщений по умолчанию, например, значения свойств **пр_дефаулт_сторе** для соответствующих хранилищ сообщений немедленно обновляются. 
  
Клиенты обращаются к таблице хранилища сообщений, вызывая метод [IMAPISession:: жетмсгсторестабле](imapisession-getmsgstorestable.md) . 
  
Следующие свойства составляют обязательный набор столбцов в таблице хранилища сообщений:
  
|||
|:-----|:-----|
|**Пр_дефаулт_сторе** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**Пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**Пр_мдб_провидер** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**Пр_провидер_дисплай** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**Пр_ресаурце_флагс** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**Пр_ресаурце_типе** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

