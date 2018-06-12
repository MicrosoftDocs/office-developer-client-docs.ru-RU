---
title: Получение контактных сообщения, присвоенное записи контактов адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Последнее изменение: 13 августа 2013 г.'
ms.openlocfilehash: 346e6bc471f5257aacb34c2e7d02a0aade1bb46e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808618"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>Получение контактных сообщения, присвоенное записи контактов адресной книги

**Применимо к**: Outlook 
  
В этом разделе содержится пример в C++ `HrOpenContact`, показано, как использовать структуру [CONTAB_ENTRYID](contab_entryid.md) , идентифицирующее запись в адресной книге контакты для получения связанного сообщения контакту MAPI. 
  
`HrOpenContact`имеет следующие параметры: 
  
-  *lpSession* — это входного параметра, представляющий текущего сеанса. **LPMAPISESSION** определяется в mapix.h файл заголовка MAPI как указатель на [IMAPISession: IUnknown](imapisessioniunknown.md).
    
-  *cbEntryID* — это входного параметра, представляющее размер идентификатор записи, связанные с *lpEntryID* . 
    
-  *lpEntryID* — это входного параметра, представляющее указатель на идентификатор операции записи в адресную книгу в контакт. 
    
-  *ulFlags* — это входного параметра, представляющее битовую маску, содержащий объект флаги доступа к сообщению контакт MAPI. 
    
-  *lpContactMessage* — это выходной параметр, представляющее указатель сообщения контакту MAPI. 
    
Открытие базового сообщение MAPI контакт `HrOpenContact` сначала выполняется приведение *lpEntryID* указатель на **CONTAB_ENTRYID**. После этого вызывается [IMAPISession::OpenEntry](imapisession-openentry.md) для получения передачи как параметры *cbeid* *abeid* поля и записи в адресной книге контакты, чтобы указать соответственно размер идентификатор записи сообщений MAPI контакта и Идентификатор записи сообщения контакту MAPI. 
  
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

