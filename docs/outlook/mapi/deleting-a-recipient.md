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
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421048"
---
# <a name="deleting-a-recipient"></a>Удаление получателя

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **Удаление одной или более записей адресной книги из изменяемого контейнера**
  
- Вызовите [метод IABContainer::D eleteEntries, передав](iabcontainer-deleteentries.md) массив идентификаторов записей, которые представляют удаленные записи адресной книги. **DeleteEntries** может вернуть предупреждение, MAPI_W_PARTIAL_COMPLETION, чтобы указать, что он не может удалить одну или несколько записей. Проверьте это возвращаемого значения с помощью **макроса HR_FAILED** и позвоните по методу [IMAPIProp::GetLastError,](imapiprop-getlasterror.md) если требуется дополнительные сведения о проблеме. 
    
При удержании указателя к структуре [ADRENTRY](adrentry.md) удаленной записи в кэше вы все равно сможете получить свойства с помощью идентификатора записи. Это потому, что запись помечена только для удаления. MAPI поддерживает уровень доступа к этим отмеченным записям по дизайну. 
  

