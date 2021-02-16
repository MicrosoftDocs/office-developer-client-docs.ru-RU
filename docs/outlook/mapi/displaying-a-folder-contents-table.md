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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Таблица содержимого папки содержит сводную информацию обо всех сообщениях. Сводная информация о новых входящих сообщениях отображается в таблице содержимого папки получения для класса сообщений. Чтобы сделать эти сведения доступными для пользователей, извлекать таблицу и отображать столбцы и строки соответствующим образом.
  
**Отображение таблицы содержимого папки**
  
1. Вызовите [IMsgStore::OpenEntry,](imsgstore-openentry.md)передав идентификатор записи папки, содержащей таблицу.
    
2. Вызовите метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папки, чтобы открыть таблицу содержимого. 
    
3. При желании ограничьте представление таблицы содержимого путем вызова метода [IMAPITable::SetColumns](imapitable-setcolumns.md) для указания определенных столбцов. 
    
4. При желании ограничьте представление таблицы содержимого путем вызова метода [IMAPITable::Restrict](imapitable-restrict.md) таблицы для фильтрации определенных строк. Например, если вы хотите показывать только сообщения с определенным классом сообщений, которые еще не прочитано: 
    
    1. Создайте ограничение свойства в [структуре SPropertyRestriction,](spropertyrestriction.md) **которое соответствует** свойству PR_MESSAGE_CLASS ([PidTagMessageClass)](pidtagmessageclass-canonical-property.md)с нужным классом сообщения. 
        
    2. Создайте ограничение битовых масок в структуре [SBitMaskRestriction,](sbitmaskrestriction.md) которая использует **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)в качестве тега свойства и значение MSGFLAG_UNREAD в качестве маски.
        
    3. Создайте ограничение в [структуре SAndRestriction,](sandrestriction.md) которое присоединяется к свойству и ограничениям битовыхmask. 
    
5. При желании сортировать таблицу содержимого путем вызова метода [IMAPITable::SortTable таблицы.](imapitable-sorttable.md) 
    
6. Вызовите [IMAPITable::QueryRows,](imapitable-queryrows.md) чтобы извлечь все строки из таблицы содержимого для обработки. 
    

