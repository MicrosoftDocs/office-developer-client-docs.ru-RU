---
title: Отображение таблицы содержимого папки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412396"
---
# <a name="displaying-a-folder-contents-table"></a>Отображение таблицы содержимого папки

**Область применения**: Outlook 2013 | Outlook 2016 
  
В таблице содержимого папки содержатся сводные сведения обо всех ее сообщениях. Сводная информация о новых входящих сообщениях отображается в таблице содержимого папки получения для класса сообщений. Чтобы сделать эти сведения доступными для пользователей, извлекаем таблицу и отображаем столбцы и строки по мере необходимости.
  
**Отображение таблицы содержимого папки**
  
1. Позвоните [в IMsgStore::OpenEntry,](imsgstore-openentry.md)передав идентификатор записи папки, содержащей таблицу.
    
2. Чтобы открыть таблицу содержимого, вызовите метод [IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md) 
    
3. Ограничить представление таблицы содержимого при желании, назвав метод [IMAPITable::SetColumns](imapitable-setcolumns.md) для указания определенных столбцов. 
    
4. Ограничите представление таблицы содержимого при желании, назвав метод [IMAPITable:::Limit](imapitable-restrict.md) для фильтрации определенных строк. Если, например, необходимо показывать только сообщения с определенным классом сообщений, которые еще не прочитано: 
    
    1. Создайте ограничение свойств в структуре [SPropertyRestriction,](spropertyrestriction.md) которое соответствует **свойству PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)с нужным классом сообщений. 
        
    2. Создайте ограничение битмаски в структуре [SBitMaskRestriction,](sbitmaskrestriction.md) которая использует **PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)в качестве тега свойства и MSGFLAG_UNREAD в качестве маски.
        
    3. Создайте ограничение в [структуре SAndRestriction,](sandrestriction.md) которая присоединяется к ограничениям свойства и bitmask. 
    
5. Сортировка таблицы содержимого при желании путем вызова метода [IMAPITable::SortTable таблицы.](imapitable-sorttable.md) 
    
6. Вызов [IMAPITable::QueryRows](imapitable-queryrows.md) для получения всех строк из таблицы содержимого для обработки. 
    

