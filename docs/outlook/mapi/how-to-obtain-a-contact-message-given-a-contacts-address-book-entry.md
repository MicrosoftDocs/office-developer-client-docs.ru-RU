---
title: Получение контактного сообщения с учетом записи адресной книги контактов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Последнее изменение: 13 августа 2013 г.'
ms.openlocfilehash: be988a3036c2d882f65e2e588cc9a40bfda146a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437793"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>Получение контактного сообщения с учетом записи адресной книги контактов

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе содержится пример в C++, который показывает, как использовать структуру CONTAB_ENTRYID, которая определяет запись в адресной книге Контактов для получения связанного сообщения `HrOpenContact` контакта MAPI. [](contab_entryid.md) 
  
`HrOpenContact` имеет следующие параметры: 
  
-  *lpSession —*  это параметр ввода, представляющий текущий сеанс. **LPMAPISESSION** определяется в файле mapix.h заголовщика MAPI в качестве указателя [на IMAPISession: IUnknown](imapisessioniunknown.md).
    
-  *cbEntryID* — это параметр ввода, представляющий размер идентификатора записи, связанного с *lpEntryID.* 
    
-  *lpEntryID*  — это параметр ввода, представляющий указатель на идентификатор записи записи в контактной адресной книге. 
    
-  *ulFlags —*  это параметр ввода, представляющий битмаску, содержащую флаги доступа объектов к сообщению контакта MAPI. 
    
-  *lpContactMessage*  — это выходной параметр, представляющий указатель на сообщение контакта MAPI. 
    
Чтобы открыть в основном сообщении контакта MAPI, сначала задав `HrOpenContact` *lpEntryID* в указатель для **CONTAB_ENTRYID.** Затем он вызывает [IMAPISession::OpenEntry,](imapisession-openentry.md) чтобы получить сообщение контакта MAPI, передав в качестве параметров поля  *cbeid*  и  *abeid*  записи в адресной книге Контактов, определяющие соответственно размер идентификатора записи и идентификатор входа сообщения контакта MAPI. 
  
```cpp
TZDEFINITION* BinToTZDEFINITION(ULONG cbDef, LPBYTE lpbDef) 
{ 
    if (!lpbDef) return NULL; 
 
    // Update this if parsing code is changed. 
    // This checks the size up to the flag member. 
    if (cbDef &lt; 2*sizeof(BYTE) + 2*sizeof(WORD)) return NULL; 
 
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
 
    // We only understand if &gt;= TZ_BIN_VERSION_MINOR 
    if (TZ_BIN_VERSION_MINOR &gt; bMinorVersion) return NULL; 
 
    lpPtr += sizeof(WORD); 
 
    tzDef.wFlags = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
 
    if (TZDEFINITION_FLAG_VALID_GUID &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(GUID)) return NULL; 
        tzDef.guidTZID = *((GUID*)lpPtr); 
        lpPtr += sizeof(GUID); 
    } 
 
    if (TZDEFINITION_FLAG_VALID_KEYNAME &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
        cchKeyName = *((WORD*)lpPtr); 
        lpPtr += sizeof(WORD); 
        if (cchKeyName) 
        { 
            if (lpbDef + cbDef - lpPtr &lt; (BYTE)sizeof(WORD)*cchKeyName) return NULL; 
            szKeyName = (WCHAR*)lpPtr; 
            lpPtr += cchKeyName*sizeof(WORD); 
        } 
    } 
 
    if (lpbDef+ cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
    tzDef.cRules = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
    if (tzDef.cRules) 
    { 
        lpRules = new TZRULE[tzDef.cRules]; 
        if (!lpRules) return NULL; 
 
        LPBYTE lpNextRule = lpPtr; 
        BOOL bRuleOK = false; 

```

## <a name="see-also"></a>См. также

- [IMAPISession::OpenEntry](imapisession-openentry.md)

