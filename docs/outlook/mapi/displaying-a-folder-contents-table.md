---
title: Отображение таблицу содержимого папки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 30099e9fe645f810e08ba331717cff975f69b313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808321"
---
# <a name="displaying-a-folder-contents-table"></a>Отображение таблицу содержимого папки

**Применимо к**: Outlook 
  
В таблице содержимое папки содержит сводную информацию обо всех его сообщения. В таблице содержимое папки получения для класса сообщения отображается сводная информация о новых входящих сообщений. Чтобы сделать эту информацию для пользователей, получения таблицы и отображения столбцов и строк соответствующим образом.
  
**Для отображения содержимого папки**
  
1. Вызовите [IMsgStore::OpenEntry](imsgstore-openentry.md), передав идентификатор записи папки, содержащей таблицу.
    
2. Вызовите метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папки, чтобы открыть его содержимое в таблице. 
    
3. Ограничьте Просмотр содержимого таблицы при желании путем вызова метода [IMAPITable::SetColumns](imapitable-setcolumns.md) таблицы для указания определенных столбцов. 
    
4. Ограничьте Просмотр содержимого таблицы при желании путем вызова метода [IMAPITable::Restrict](imapitable-restrict.md) таблицы для фильтрации конкретной строки. Если, например требуется показать только сообщения с определенным классом сообщения, для которых еще не требуется прочитать: 
    
    1. Создайте ограничение свойства в структуре [SPropertyRestriction](spropertyrestriction.md) , соответствующее свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) с помощью класса сообщений. 
        
    2. Создайте ограничение битовой маски в структуре [SBitMaskRestriction](sbitmaskrestriction.md) , использующий **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) в качестве тега свойства и значения MSGFLAG_UNREAD как маски.
        
    3. Создания ограничения в структуре [SAndRestriction](sandrestriction.md) , объединяющий ограничения свойств и битовую маску. 
    
5. Сортировка в таблице содержимое при желании путем вызова метода [IMAPITable::SortTable](imapitable-sorttable.md) таблицы. 
    
6. Вызовите [IMAPITable::QueryRows](imapitable-queryrows.md) , чтобы получить все строки из таблицы содержимого для обработки. 
    

