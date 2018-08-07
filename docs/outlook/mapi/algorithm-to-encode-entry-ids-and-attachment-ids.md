---
title: Алгоритм шифрования идентификаторов записей и идентификаторов вложений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 710ba5173dcce6e948e1f49c7d82e46bc83b8200
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808054"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Алгоритм шифрования идентификаторов записей и идентификаторов вложений

  
  
**Относится к**: Outlook 
  
Поставщик хранения можно отправить как часть из MAPI универсальный код ресурса по URL-идентификатор записи и идентификатор вложения обработчик протокола MAPI для идентификации объекта, который будет готов для индексации. Поставщик хранения кодирует запись идентификатор и идентификатор вложения Юникод. В этом разделе показано алгоритм, который создает compact представление идентификатор входа или идентификатор вложения.
  
```cpp
const WORD kwBaseOffset = 0xAC00;  // Hangul char range (AC00-D7AF) 
LPWSTR EncodeID(ULONG cbEID, LPENTRYID rgbID) 
{ 
    ULONG   i = 0; 
    LPWSTR  pwzDst = NULL; 
    LPBYTE  pbSrc = NULL; 
    LPWSTR  pwzIDEncoded = NULL; 
 
    // rgbID is the item Entry ID or the attachment ID 
    // cbID is the size in bytes of rgbID 
 
    // Allocate memory for pwzIDEncoded 
    pwzIDEncoded = new WCHAR[cbEID]; 
    if (!pwzIDEncoded) return NULL; 
 
    for (i = 0, pbSrc = (LPBYTE)rgbID, pwzDst = pwzIDEncoded; 
        i < cbEID; 
        i++, pbSrc++, pwzDst++) 
    { 
        *pwzDst = (WCHAR) (*pbSrc + kwBaseOffset); 
    } 
 
    // Ensure NULL terminated 
    *pwzDst = L'\0'; 
 
    // pwzIDEncoded now contains the entry ID encoded. 
    return pwzIDEncoded; 
}
```

## <a name="see-also"></a>См. также



[Сведения об индексировании хранилищ на основе уведомлений](about-notification-based-store-indexing.md)
  
[Сведения об URL-адресах MAPI для индексирования на основе уведомлений](about-mapi-urls-for-notification-based-indexing.md)

