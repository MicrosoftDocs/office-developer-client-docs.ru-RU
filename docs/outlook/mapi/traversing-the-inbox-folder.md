---
title: Навигация по папке "Входящие"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5e93dbed0fe56ada5fc41c3e2e51aa3d0c3bef6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594490"
---
# <a name="traversing-the-inbox-folder"></a>Навигация по папке "Входящие"

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
 **Чтобы просмотреть все сообщения в папке "Входящие"**
  
1. Вызовите [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , чтобы получить идентификатор записи из папки «Входящие». 
    
2. Вызовите **IMAPIFolder::OpenEntry** , чтобы открыть папку "Входящие". 
    
3. Вызов метода [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папке "Входящие" для получения содержимого таблицы. 
    
4. Вызовите метод [IMAPITable::SetColumns](imapitable-setcolumns.md) таблицы для ограничения столбец, задайте значение **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и другие столбцы, которые требуется содержимое. 
    
5. Вызов [IMAPITable::QueryRows](imapitable-queryrows.md) для извлечения группы строк. 
    
6. Пока не больше не существует все строки в таблице содержимого:
    
1. Вызовите [IMsgStore::OpenEntry](imsgstore-openentry.md) , чтобы открыть сообщение, представленное идентификатор записи из каждой строки. 
    
2. Назначьте параметр _lppUnk_ локального указатель интерфейса **IMessage** . 
    
3. Работа со свойствами сообщения.
    
4. Выпуск указатель, на который указывает параметр _lppUnk_ . 
    
5. Вызов [IMAPITable::QueryRows](imapitable-queryrows.md) для получения следующей группы строк. 
    
7. Выпуск таблицу содержимого.
    

