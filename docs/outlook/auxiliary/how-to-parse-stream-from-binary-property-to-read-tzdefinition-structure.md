---
title: Анализ потока из двоичного свойства для считывания структуры TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 039b3a45-bd57-51f5-1485-a3f6d1bde85a
description: В этом разделе показано, как читать структуру TZDEFINITION из сохраняемой формы, хранимой в двоичном свойстве.
ms.openlocfilehash: a685fbfcf918e13aa82ac32799997bb05730184e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434209"
---
# <a name="parse-a-stream-from-a-binary-property-to-read-the-tzdefinition-structure"></a><span data-ttu-id="9d341-103">Анализ потока из двоичного свойства для считывания структуры TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="9d341-103">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>

<span data-ttu-id="9d341-104">В этом разделе показано, как читать структуру [TZDEFINITION](tzdefinition.md) из сохраняемой формы, хранимой в двоичном свойстве.</span><span class="sxs-lookup"><span data-stu-id="9d341-104">This topic shows how to read the [TZDEFINITION](tzdefinition.md) structure from the persisted format stored in a binary property.</span></span> 
  
```cpp
TZDEFINITION* BinToTZDEFINITION(ULONG cbDef, LPBYTE lpbDef) 
{ 
    if (!lpbDef) return NULL; 
 
    // Update this if parsing code is changed. 
    // This checks the size up to the flag member. 
    if (cbDef &amp;lt; 2*sizeof(BYTE) + 2*sizeof(WORD)) return NULL; 
 
    TZDEFINITION tzDef = {0}; 
    TZRULE* lpRules = NULL; 
    LPBYTE lpPtr = lpbDef; 
    WORD cchKeyName = NULL; 
    WCHAR* szKeyName = NULL; 
    WORD i = 0; 
 
    BYTE bMajorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
    BYTE bMinorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
 
    // We only understand TZ_BIN_VERSION_MAJOR 
    if (TZ_BIN_VERSION_MAJOR != bMajorVersion) return NULL; 
 
    // We only understand if &amp;gt;= TZ_BIN_VERSION_MINOR 
    if (TZ_BIN_VERSION_MINOR &amp;gt; bMinorVersion) return NULL; 
 
    lpPtr += sizeof(WORD); 
 
    tzDef.wFlags = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
 
    if (TZDEFINITION_FLAG_VALID_GUID &amp;amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &amp;lt; sizeof(GUID)) return NULL; 
        tzDef.guidTZID = *((GUID*)lpPtr); 
        lpPtr += sizeof(GUID); 
    } 
 
    if (TZDEFINITION_FLAG_VALID_KEYNAME &amp;amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &amp;lt; sizeof(WORD)) return NULL; 
        cchKeyName = *((WORD*)lpPtr); 
        lpPtr += sizeof(WORD); 
        if (cchKeyName) 
        { 
            if (lpbDef + cbDef - lpPtr &amp;lt; (BYTE)sizeof(WORD)*cchKeyName) return NULL; 
            szKeyName = (WCHAR*)lpPtr; 
            lpPtr += cchKeyName*sizeof(WORD); 
        } 
    } 
 
    if (lpbDef+ cbDef - lpPtr &amp;lt; sizeof(WORD)) return NULL; 
    tzDef.cRules = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
    if (tzDef.cRules) 
    { 
        lpRules = new TZRULE[tzDef.cRules]; 
        if (!lpRules) return NULL; 
 
        LPBYTE lpNextRule = lpPtr; 
        BOOL bRuleOK = false; 

```

## <a name="see-also"></a><span data-ttu-id="9d341-105">См. также</span><span class="sxs-lookup"><span data-stu-id="9d341-105">See also</span></span>

- [<span data-ttu-id="9d341-106">Сведения о сохранении TZDEFINITION в потоке для помещения в двоичное свойство</span><span class="sxs-lookup"><span data-stu-id="9d341-106">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)
- [<span data-ttu-id="9d341-107">Считывание свойств часового пояса встречи</span><span class="sxs-lookup"><span data-stu-id="9d341-107">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

