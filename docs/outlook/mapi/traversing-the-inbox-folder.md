---
title: Просмотр папки "Входящие"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356583"
---
# <a name="traversing-the-inbox-folder"></a>Просмотр папки "Входящие"

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **Циклическое переключение между всеми сообщениями в папке "Входящие"**
  
1. Call [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md) для получения идентификатора записи папки "Входящие". 
    
2. Call **IMAPIFolder:: OpenEntry** для открытия папки "Входящие". 
    
3. ВыЗовите метод [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) из папки "Входящие" для получения таблицы содержимого. 
    
4. ВыЗовите таблицу содержимого, выЗовите метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) , чтобы ограничить набор столбцов значением **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и любыми другими нужными столбцами. 
    
5. Call [IMAPITable:: QueryRows](imapitable-queryrows.md) , чтобы получить группу строк. 
    
6. Пока в таблице содержимого больше нет строк:
    
1. Call [IMsgStore:: OpenEntry](imsgstore-openentry.md) , чтобы открыть сообщение, представленное идентификатором записи, из каждой строки. 
    
2. Назначьте параметр _лппунк_ указателю на локальный интерфейс **iMessage** . 
    
3. Работать со свойствами сообщения.
    
4. ОтПустите указатель, на который указывает параметр _лппунк_ . 
    
5. Call [IMAPITable:: QueryRows](imapitable-queryrows.md) для получения следующей группы строк. 
    
7. Освободите таблицу содержимого.
    

