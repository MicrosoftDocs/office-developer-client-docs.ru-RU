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
ms.openlocfilehash: 1fb7224e110bbee6844cf2820782aac8be213ba3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812110"
---
# <a name="removing-address-book-entries"></a>Удаление записей адресной книги
  
**Относится к**: Outlook 
  
Метод [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) контейнера вызывается для удаления одного или нескольких получателей. **Внешнее** имеет два параметра: массив идентификаторов записи, представляющее получателей для удаления и значение зарезервировано флагов. Удаление получателя влияет на таблицу содержимого контейнера; Помимо удаления получателя, контейнера необходимо удалить строку в таблице содержимое, представляющий получателя. При удалении строку из таблицы контейнера выполнить уведомление о таблице для каждого зарегистрированных клиентов. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>Для реализации IABContainer::DeleteEntries
  
1. Удаление каждого получателя, представленное идентификатор записи из контейнера.
    
2. Если открыта таблицу содержимого контейнера:
    
   - Отправьте уведомление о _fnevTableModified_ с **ulTableEvent** набор элементов для TABLE_ROW_DELETED зарегистрированным пользователям для каждой строки в таблице удаленное содержимое. Если ваш поставщик использует служебная программа уведомлений, вызовите [IMAPISupport::Notify](imapisupport-notify.md) для отправки этих уведомлений. 
    
   - Если ваш поставщик поддерживает объект уведомлений, отправьте уведомление о _fnevObjectDeleted_ . 
    

