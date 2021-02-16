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
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Многие папки можно открыть с обычным представлением, представлением по умолчанию или любым количеством персонализированных представлений. В представлении описывается, как отобразить содержимое папки. Обычное представление используется при отсутствие альтернативного представления и при первом открытии папки. Если альтернативное представление существует, его необходимо использовать для открытия папки.
  
Представление описывается в сообщении, известном как дескриптор представления. Дескрипторы представления обычно создаются как связанные сообщения и могут отображаться в общих или личных папках представления или в любой папке IPM.
  
### <a name="to-open-a-view-descriptor"></a>Открытие дескриптора представления
  
1. Вызовите [IMAPIContainer::GetContentsTable,](imapicontainer-getcontentstable.md) чтобы получить связанную таблицу содержимого для папки. 
    
2. Создайте ограничение, которое находит только сообщения с классом сообщения, зарезервированным для дескрипторов представления, и вызывать [IMAPITable::Restrict,](imapitable-restrict.md) чтобы ограничить таблицу и [IMAPITable::QueryRows](imapitable-queryrows.md) для получения соответствующих строк или...
    
   Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) папки, чтобы получить **ее PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId).](pidtagdefaultviewentryid-canonical-property.md) **PR_DEFAULT_VIEW_ENTRYID** содержит идентификатор записи для сообщения, содержащего дескриптор представления по умолчанию для папки. Этот вызов будет успешным, если папка поддерживает использование флага MAPI_ASSOCIATED при вызовах [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) и [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
3. Вызовите [IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором записи дескриптора представления, чтобы открыть его. 
    

