---
title: Обход папки "Входящие"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406558"
---
# <a name="traversing-the-inbox-folder"></a>Обход папки "Входящие"

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 **Циклия всех сообщений в почтовой ящике**
  
1. Вызовите [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы получить идентификатор записи для входящих сообщений. 
    
2. Вызовите **IMAPIFolder::OpenEntry,** чтобы открыть "Входящие". 
    
3. Вызовите метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) для извлечения таблицы содержимого. 
    
4. Вызовите метод [IMAPITable::SetColumns](imapitable-setcolumns.md) таблицы содержимого, чтобы ограничить набор столбцов PR_ENTRYID **(** [PidTagEntryId)](pidtagentryid-canonical-property.md)и любыми другими требуемыми столбцами. 
    
5. Вызов [IMAPITable::QueryRows](imapitable-queryrows.md) для получения группы строк. 
    
6. Пока в таблице содержимого больше нет строк:
    
1. Вызовите [IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть сообщение, представленное идентификатором записи из каждой строки. 
    
2. _Назначьте параметр lppUnk_ локальному указателю интерфейса **IMessage.** 
    
3. Работа со свойствами сообщения.
    
4. Отпустите указатель, на который указывает параметр _lppUnk._ 
    
5. Вызовите [IMAPITable::QueryRows,](imapitable-queryrows.md) чтобы получить следующую группу строк. 
    
7. Отпустите таблицу содержимого.
    

