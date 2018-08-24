---
title: Удаление получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 03917ad52f1dc1ce4d0b59cd54fe33f58f352061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582947"
---
# <a name="deleting-a-recipient"></a>Удаление получателя

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 **Чтобы удалить одного или нескольких записей адресной книги из изменяемые контейнера**
  
- Вызовите метод [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) , передав массив идентификаторов записи, которые представляют адресной книги к удалению. **Внешнее** может вернуть предупреждение MAPI_W_PARTIAL_COMPLETION, чтобы указать, что она не удается удалить одну или несколько записей. Тестирование этого возвращаемого значения с помощью макроса **HR_FAILED** и вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) контейнера, если требуется дополнительная информация о проблеме. 
    
Если навести указатель структуру [ADRENTRY](adrentry.md) удаленные записи в кэше по-прежнему можно для извлечения свойств с помощью его идентификатор записи. Это, так как операция только помеченным для удаления. Уровень доступа к эти помеченные записи поддерживает MAPI, разработки. 
  

