---
title: Определить, какая версия Exchange Server в профиле Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: 'Последнее изменение: 03 июля 2012 г.'
ms.openlocfilehash: b6c1482554cfb1e756266eb31f992b81bc34bb51
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575898"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a><span data-ttu-id="fef60-103">Определить, какая версия Exchange Server в профиле Outlook</span><span class="sxs-lookup"><span data-stu-id="fef60-103">Detect the version of Exchange Server in an Outlook profile</span></span>

<span data-ttu-id="fef60-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fef60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fef60-105">В этом разделе приводится пример кода c++, который показано, как использовать свойство **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** и свойство **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** для получения сведений о версии сервера Microsoft Exchange Server, который является активной учетной записи подключение.</span><span class="sxs-lookup"><span data-stu-id="fef60-105">This topic includes a code sample in C++ that shows how to use the **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** property and **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** property to obtain version information of the Microsoft Exchange Server that the active account is connected to.</span></span> 
  
<span data-ttu-id="fef60-106">`GetProfileServiceVersion` Функции в образце кода принимает профиль в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="fef60-106">The  `GetProfileServiceVersion` function in the code sample accepts a profile as an input parameter.</span></span> <span data-ttu-id="fef60-107">В зависимости от того, является ли свойство **PR_PROFILE_SERVER_VERSION** и свойство **PR_PROFILE_SERVER_FULL_VERSION** существует в заданного профиля функция возвращает каждого свойства и возвращает соответствующую версию данных в качестве выходных данных параметры.</span><span class="sxs-lookup"><span data-stu-id="fef60-107">Depending on whether the **PR_PROFILE_SERVER_VERSION** property and the **PR_PROFILE_SERVER_FULL_VERSION** property exist in the given profile, the function gets each property and returns the appropriate version information as output parameters.</span></span> 
  
<span data-ttu-id="fef60-108">`GetProfileServiceVersion`Сначала вызывается функция **[MAPIAdminProfiles](mapiadminprofiles.md)** для создания объекта администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="fef60-108">`GetProfileServiceVersion` first calls the **[MAPIAdminProfiles](mapiadminprofiles.md)** function to create a profile administration object.</span></span> <span data-ttu-id="fef60-109">Затем объект администрирования профилей используется для вызова **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** , чтобы получить объект администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="fef60-109">It then uses the profile administration object to call **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** to obtain a message service administration object.</span></span> <span data-ttu-id="fef60-110">С помощью объекта message службы администрирования, он вызывает **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** для получения части текущего профиля, а затем вызывает **[HrGetOneProp](hrgetoneprop.md)** , чтобы проверить, существует ли каждый из двух свойств в данном разделе профиль и если да, наборов сведений о версии в соответствующие выходные параметры.</span><span class="sxs-lookup"><span data-stu-id="fef60-110">Using the message service administration object, it calls **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** to obtain a section of the current profile, and then calls **[HrGetOneProp](hrgetoneprop.md)** to verify if each of the two properties exists in that section of the profile, and if so, sets the version information in the appropriate output parameters.</span></span> 
  
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


