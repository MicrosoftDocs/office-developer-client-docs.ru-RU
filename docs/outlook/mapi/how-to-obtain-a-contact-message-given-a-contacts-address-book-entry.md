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
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a><span data-ttu-id="9d618-103">Получение контактных сообщения, присвоенное записи контактов адресной книги</span><span class="sxs-lookup"><span data-stu-id="9d618-103">Obtain a contact message given a contacts address book entry</span></span>

<span data-ttu-id="9d618-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d618-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d618-105">В этом разделе содержится пример в C++ `HrOpenContact`, показано, как использовать структуру [CONTAB_ENTRYID](contab_entryid.md) , идентифицирующее запись в адресной книге контакты для получения связанного сообщения контакту MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d618-105">This topic contains an example in C++, `HrOpenContact`, that shows how to use the [CONTAB_ENTRYID](contab_entryid.md) structure that identifies an entry in a Contacts Address Book to obtain the associated MAPI Contact message.</span></span> 
  
<span data-ttu-id="9d618-106">`HrOpenContact`имеет следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="9d618-106">`HrOpenContact` has the following parameters:</span></span> 
  
-  <span data-ttu-id="9d618-107">*lpSession* — это входного параметра, представляющий текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="9d618-107">*lpSession*  is an input parameter representing the current session.</span></span> <span data-ttu-id="9d618-108">**LPMAPISESSION** определяется в mapix.h файл заголовка MAPI как указатель на [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="9d618-108">**LPMAPISESSION** is defined in the MAPI header file mapix.h as a pointer to [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span>
    
-  <span data-ttu-id="9d618-109">*cbEntryID* — это входного параметра, представляющее размер идентификатор записи, связанные с *lpEntryID* .</span><span class="sxs-lookup"><span data-stu-id="9d618-109">*cbEntryID*  is an input parameter representing the size of the entry identifier associated with  *lpEntryID*  .</span></span> 
    
-  <span data-ttu-id="9d618-110">*lpEntryID* — это входного параметра, представляющее указатель на идентификатор операции записи в адресную книгу в контакт.</span><span class="sxs-lookup"><span data-stu-id="9d618-110">*lpEntryID*  is an input parameter representing a pointer to the entry identifier of an entry in a Contact Address Book.</span></span> 
    
-  <span data-ttu-id="9d618-111">*ulFlags* — это входного параметра, представляющее битовую маску, содержащий объект флаги доступа к сообщению контакт MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d618-111">*ulFlags*  is an input parameter representing a bitmask containing object access flags to the MAPI Contact message.</span></span> 
    
-  <span data-ttu-id="9d618-112">*lpContactMessage* — это выходной параметр, представляющее указатель сообщения контакту MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d618-112">*lpContactMessage*  is an output parameter representing a pointer to the MAPI Contact message.</span></span> 
    
<span data-ttu-id="9d618-113">Открытие базового сообщение MAPI контакт `HrOpenContact` сначала выполняется приведение *lpEntryID* указатель на **CONTAB_ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="9d618-113">To open the underlying MAPI Contact message,  `HrOpenContact` first casts  *lpEntryID*  to a pointer to **CONTAB_ENTRYID**.</span></span> <span data-ttu-id="9d618-114">После этого вызывается [IMAPISession::OpenEntry](imapisession-openentry.md) для получения передачи как параметры *cbeid* *abeid* поля и записи в адресной книге контакты, чтобы указать соответственно размер идентификатор записи сообщений MAPI контакта и Идентификатор записи сообщения контакту MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d618-114">It then calls [IMAPISession::OpenEntry](imapisession-openentry.md) to obtain the MAPI Contact message, passing as parameters the  *cbeid*  and  *abeid*  fields of the entry in the Contacts Address Book that identify respectively the size of the entry identifier and the entry identifier of the MAPI Contact message.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="9d618-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9d618-115">See also</span></span>

- [<span data-ttu-id="9d618-116">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="9d618-116">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)

