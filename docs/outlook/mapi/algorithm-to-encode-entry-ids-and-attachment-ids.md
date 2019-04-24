---
title: Алгоритм кодирования идентификаторов записей и идентификаторов вложений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6c39fe513be122f265fdc316629a3e64a156fdc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318181"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a><span data-ttu-id="eb41b-103">Алгоритм кодирования идентификаторов записей и идентификаторов вложений</span><span class="sxs-lookup"><span data-stu-id="eb41b-103">Algorithm to Encode Entry IDs and Attachment IDs</span></span>

  
  
<span data-ttu-id="eb41b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb41b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb41b-105">Поставщик хранилища может отправляться в качестве части URL-адреса записи и идентификатора вложения в обработчик протокола MAPI для определения объекта, готового к индексированию.</span><span class="sxs-lookup"><span data-stu-id="eb41b-105">A store provider can send as part of a MAPI Uniform Resource Locator (URL) an entry ID and an attachment ID to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="eb41b-106">Поставщик хранилища кодирует идентификатор записи и идентификатор вложения в виде строк Юникода.</span><span class="sxs-lookup"><span data-stu-id="eb41b-106">The store provider encodes the entry ID and attachment ID as Unicode strings.</span></span> <span data-ttu-id="eb41b-107">В этом разделе показан алгоритм, который создает компактное представление идентификатора записи или идентификатора вложения.</span><span class="sxs-lookup"><span data-stu-id="eb41b-107">This topic shows an algorithm that generates a compact representation of the entry ID or attachment ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="eb41b-108">См. также</span><span class="sxs-lookup"><span data-stu-id="eb41b-108">See also</span></span>



[<span data-ttu-id="eb41b-109">Об индексировании хранилищ на основе уведомлений</span><span class="sxs-lookup"><span data-stu-id="eb41b-109">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
  
[<span data-ttu-id="eb41b-110">Сведения об URL-адресах MAPI для индексирования на основе уведомлений</span><span class="sxs-lookup"><span data-stu-id="eb41b-110">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)

