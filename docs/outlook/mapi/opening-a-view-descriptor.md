---
title: Открытие представления дескриптора
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 680d80c0827399f3b7a0ea5819e51be654a05810
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592481"
---
# <a name="opening-a-view-descriptor"></a>Открытие представления дескриптора
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Большое число папок могут быть открыты в обычном режиме, представление по умолчанию или любое количество личных представлений. Представление описывает способ отображения содержимого папки. Стандартное представление используется, когда нет альтернативные представления и при открытии папки в первый раз. При альтернативное представление существует, его необходимо использовать для откройте папку.
  
Представление описан в сообщении, называемый дескриптором представления. Просмотр дескрипторы обычно создаются в качестве связанного сообщения и может отображаться в папках распространенных или личном представлении или в любой папке IPM.
  
### <a name="to-open-a-view-descriptor"></a>Чтобы открыть представление дескриптора
  
1. Вызов [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) для получения таблицы связанного содержимого папки. 
    
2. Создание ограничение, которое находит только сообщения с классом сообщения, зарезервировано для представления дескрипторов и вызова [IMAPITable::Restrict](imapitable-restrict.md) для ограничения в таблице и [IMAPITable::QueryRows](imapitable-queryrows.md) для получения соответствующих строк или...
    
   Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) папки для получения его свойство **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)). **PR_DEFAULT_VIEW_ENTRYID** содержит идентификатор записи на сообщение, содержащее дескриптор представления по умолчанию для папки. Этот звонок будет выполнено, если папка поддерживает использование флаг MAPI_ASSOCIATED на вызовы [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) и [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
3. Вызов [IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором записи дескриптора представление, чтобы открыть его. 
    

