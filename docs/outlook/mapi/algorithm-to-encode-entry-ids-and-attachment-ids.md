---
title: Алгоритм кодирования ИД входа и Вложений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6c39fe513be122f265fdc316629a3e64a156fdc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420138"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Алгоритм кодирования ИД входа и Вложений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поставщик магазина может отправить в рамках единого локатора ресурсов MAPI (URL-адрес) ID записи и ID вложения в обработчик протокола MAPI, чтобы определить объект, готовый к индексации. Поставщик магазина кодирует ID записи и код вложения как строки Юникод. В этом разделе показан алгоритм, который создает компактное представление ID или ID вложения.
  
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



[Индексация Notification-Based магазина](about-notification-based-store-indexing.md)
  
[О URL-адресах MAPI для Notification-Based индексации](about-mapi-urls-for-notification-based-indexing.md)

