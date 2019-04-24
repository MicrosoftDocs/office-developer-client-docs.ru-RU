---
title: Получение контактного сообщения для записи адресной книги контактов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Дата последнего изменения: 13 августа 2013 г.'
ms.openlocfilehash: be988a3036c2d882f65e2e588cc9a40bfda146a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345958"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a><span data-ttu-id="910e0-103">Получение контактного сообщения для записи адресной книги контактов</span><span class="sxs-lookup"><span data-stu-id="910e0-103">Obtain a contact message given a contacts address book entry</span></span>

<span data-ttu-id="910e0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="910e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="910e0-105">В этом разделе содержится пример в C++, `HrOpenContact`в котором показано, как использовать структуру [контаб_ентрид](contab_entryid.md) , которая определяет запись в адресной книге Contacts, чтобы получить связанное Контактное сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="910e0-105">This topic contains an example in C++, `HrOpenContact`, that shows how to use the [CONTAB_ENTRYID](contab_entryid.md) structure that identifies an entry in a Contacts Address Book to obtain the associated MAPI Contact message.</span></span> 
  
<span data-ttu-id="910e0-106">`HrOpenContact`имеет следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="910e0-106">`HrOpenContact` has the following parameters:</span></span> 
  
-  <span data-ttu-id="910e0-107">*лпсессион* является входным параметром, представляющим текущий сеанс.</span><span class="sxs-lookup"><span data-stu-id="910e0-107">*lpSession*  is an input parameter representing the current session.</span></span> <span data-ttu-id="910e0-108">**Лпмаписессион** определяется в файле заголовка MAPI мапикс. h как указатель на [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="910e0-108">**LPMAPISESSION** is defined in the MAPI header file mapix.h as a pointer to [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span>
    
-  <span data-ttu-id="910e0-109">*кбентрид* — это входной параметр, представляющий размер идентификатора записи, связанного с *лпентрид* .</span><span class="sxs-lookup"><span data-stu-id="910e0-109">*cbEntryID*  is an input parameter representing the size of the entry identifier associated with  *lpEntryID*  .</span></span> 
    
-  <span data-ttu-id="910e0-110">*лпентрид* является входным параметром, представляющим указатель на идентификатор записи в адресной книге контакта.</span><span class="sxs-lookup"><span data-stu-id="910e0-110">*lpEntryID*  is an input parameter representing a pointer to the entry identifier of an entry in a Contact Address Book.</span></span> 
    
-  <span data-ttu-id="910e0-111">*ulFlags* является входным параметром, представляющим битовую маску, содержащую флаги доступа к объектам для контактного сообщения MAPI.</span><span class="sxs-lookup"><span data-stu-id="910e0-111">*ulFlags*  is an input parameter representing a bitmask containing object access flags to the MAPI Contact message.</span></span> 
    
-  <span data-ttu-id="910e0-112">*лпконтактмессаже* — выходной параметр, представляющий указатель на сообщение контакта MAPI.</span><span class="sxs-lookup"><span data-stu-id="910e0-112">*lpContactMessage*  is an output parameter representing a pointer to the MAPI Contact message.</span></span> 
    
<span data-ttu-id="910e0-113">Чтобы открыть базовое сообщение с контактом `HrOpenContact` MAPI, сначала приводится *лпентрид* к указателю на **контаб_ентрид**.</span><span class="sxs-lookup"><span data-stu-id="910e0-113">To open the underlying MAPI Contact message,  `HrOpenContact` first casts  *lpEntryID*  to a pointer to **CONTAB_ENTRYID**.</span></span> <span data-ttu-id="910e0-114">Затем вызывается метод [IMAPISession:: OpenEntry](imapisession-openentry.md) для получения контактного сообщения MAPI, передающий в качестве параметров поля *кбеид* и *Абеид* записи в адресной книге Contacts, которые определяют соответственно размер идентификатора записи и Идентификатор записи контактного сообщения MAPI.</span><span class="sxs-lookup"><span data-stu-id="910e0-114">It then calls [IMAPISession::OpenEntry](imapisession-openentry.md) to obtain the MAPI Contact message, passing as parameters the  *cbeid*  and  *abeid*  fields of the entry in the Contacts Address Book that identify respectively the size of the entry identifier and the entry identifier of the MAPI Contact message.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="910e0-115">См. также</span><span class="sxs-lookup"><span data-stu-id="910e0-115">See also</span></span>

- [<span data-ttu-id="910e0-116">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="910e0-116">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)

