---
title: Удаление получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 9a3006b43eb9f210603ff3a3d890118e7fd61d7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808268"
---
# <a name="deleting-a-recipient"></a>Удаление получателя

  
  
**Применимо к**: Outlook 
  
 **Чтобы удалить одного или нескольких записей адресной книги из изменяемые контейнера**
  
- Вызовите метод [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) , передав массив идентификаторов записи, которые представляют адресной книги к удалению. **Внешнее** может вернуть предупреждение MAPI_W_PARTIAL_COMPLETION, чтобы указать, что она не удается удалить одну или несколько записей. Тестирование этого возвращаемого значения с помощью макроса **HR_FAILED** и вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) контейнера, если требуется дополнительная информация о проблеме. 
    
Если навести указатель структуру [ADRENTRY](adrentry.md) удаленные записи в кэше по-прежнему можно для извлечения свойств с помощью его идентификатор записи. Это, так как операция только помеченным для удаления. Уровень доступа к эти помеченные записи поддерживает MAPI, разработки. 
  

