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
  
В таблице содержимого папки содержатся сводные сведения обо всех сообщениях. Сводные сведения о новых входящих сообщениях отображаются в таблице содержимого папки получения для класса сообщений. Чтобы сделать эти сведения доступными для пользователей, извлеките таблицу и отобразите столбцы и строки соответствующим образом.
  
**Отображение таблицы содержимого папки**
  
1. Call [IMsgStore:: OpenEntry](imsgstore-openentry.md), передавая идентификатор записи для папки, содержащей таблицу.
    
2. Вызовите метод [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) папки, чтобы открыть его таблицу содержимого. 
    
3. При необходимости ограничьте представление таблицы содержимого, вызвав метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) для указания определенных столбцов. 
    
4. При необходимости ограничьте представление таблицы содержимого, вызвав метод [IMAPITable:: restrict](imapitable-restrict.md) для фильтрации определенных строк. Например, если вы хотите, чтобы отображались только сообщения с определенным классом сообщений, которые еще не прочитаны: 
    
    1. Создайте ограничение свойства в структуре [спропертирестриктион](spropertyrestriction.md) , которая соответствует свойству **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) с нужным классом Message. 
        
    2. Создайте ограничение битовой маски в структуре [сбитмаскрестриктион](sbitmaskrestriction.md) , в которой в качестве тега свойства используется **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)), а в качестве маски — значение MSGFLAG_UNREAD.
        
    3. Создание ограничения в структуре [сандрестриктион](sandrestriction.md) , которая присоединяет ограничения свойств и битовой маски. 
    
5. При необходимости отсортируйте таблицу содержимого, вызвав метод [IMAPITable:: сорттабле](imapitable-sorttable.md) для таблицы. 
    
6. Call [IMAPITable:: QueryRows](imapitable-queryrows.md) , чтобы получить все строки из таблицы содержимое для обработки. 
    

