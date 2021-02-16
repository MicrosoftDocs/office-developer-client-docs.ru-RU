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
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Метод [IABContainer::D eleteEntries](iabcontainer-deleteentries.md) вашего контейнера используется для удаления одного или более получателей. **DeleteEntries** имеет два параметра: массив идентификаторов записей, представляющих удаляемых получателей, и зарезервированное значение флагов. Удаление получателя влияет на содержимое таблицы контейнера; Помимо удаления получателя контейнер должен удалить строку таблицы содержимого, представляюную получателя. После удаления строки из таблицы контейнер должен издать уведомление о таблице для каждого зарегистрированного клиента. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>Реализация IABContainer::D eleteEntries
  
1. Удалите из контейнера каждого получателя, представленного идентификатором записи.
    
2. Если таблица содержимого контейнера открыта:
    
   - Отправьте  _уведомление fnevTableModified_ с установленным для члена **ulTableEvent** TABLE_ROW_DELETED зарегистрированным клиентам для каждой удаленной строки таблицы содержимого. Если поставщик использует совладелйку уведомлений, вызовите [IMAPISupport::Notify,](imapisupport-notify.md) чтобы отправить эти уведомления. 
    
   - Если поставщик поддерживает уведомления об объектах, отправьте уведомление _fnevObjectDeleted._ 
    

