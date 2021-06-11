---
title: Открытие дескриптора представления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ce53e5a91f6fa340728872457eae7f6514e287aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413040"
---
# <a name="opening-a-view-descriptor"></a>Открытие дескриптора представления
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Многие папки можно открыть с нормальным представлением, представлением по умолчанию или любым количеством персонализированных представлений. Представление описывает отображение содержимого папки. Обычное представление используется, когда нет альтернативного представления и при первом открытии папки. Если существует альтернативное представление, его необходимо использовать для открытия папки.
  
Представление описывается в сообщении, известном как дескриптор представления. Просмотр дескрипторов обычно создается в качестве связанных сообщений и может отображаться в общих или личных папках представлений или в любой папке IPM.
  
### <a name="to-open-a-view-descriptor"></a>Открытие дескриптора представления
  
1. Вызов [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) для получения связанной таблицы содержимого для папки. 
    
2. Создайте ограничение, которое находит только сообщения с классом сообщений, зарезервированным для дескрипторов просмотра, и вызывайте [IMAPITable::Limit,](imapitable-restrict.md) чтобы ограничить таблицу и [IMAPITable::QueryRows,](imapitable-queryrows.md) чтобы получить соответствующие строки или...
    
   Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) **для** получения свойства [PR_DEFAULT_VIEW_ENTRYID (PidTagDefaultViewEntryId).](pidtagdefaultviewentryid-canonical-property.md) **PR_DEFAULT_VIEW_ENTRYID** содержит идентификатор записи для сообщения, содержащего дескриптор представления по умолчанию для папки. Этот вызов будет успешным, если папка поддерживает использование флага MAPI_ASSOCIATED при звонках [в IMAPIFolder::CreateMessage](imapifolder-createmessage.md) и [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
3. Вызов [IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором входа дескриптора представления, чтобы открыть его. 
    

