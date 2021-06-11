---
title: Удаление записей адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425262"
---
# <a name="removing-address-book-entries"></a>Удаление записей адресной книги
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Для удаления одного или более получателей вызван [метод IABContainer::D eleteEntries.](iabcontainer-deleteentries.md) **DeleteEntries** имеет два параметра: массив идентификаторов записей, представляющих удаленных получателей, и зарезервированное значение флагов. Удаление получателя влияет на содержимое таблицы контейнера; Помимо удаления получателя, контейнер должен удалить строку таблицы содержимого, которая представляет получателя. Когда строка удалена из таблицы, контейнер должен выдавать уведомление о таблице каждому зарегистрированного клиента. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>Реализация IABContainer::D eleteEntries
  
1. Удаление каждого получателя, представленного идентификатором записи из контейнера.
    
2. Если таблица содержимого контейнера открыта:
    
   - Отправьте  _уведомление fnevTableModified_ с набором **участника ulTableEvent** TABLE_ROW_DELETED зарегистрированным клиентам для каждой строки таблицы удаленного контента. Если поставщик использует утилиту уведомлений, позвоните [в службу IMAPISupport::Notify](imapisupport-notify.md) для отправки этих уведомлений. 
    
   - Если поставщик поддерживает объектные уведомления, также отправьте _уведомление fnevObjectDeleted._ 
    

