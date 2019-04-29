---
title: Определение версии Exchange Server в профиле Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: 'Дата последнего изменения: 03 июля, 2012'
ms.openlocfilehash: c6aaac128e1a3e1a8d77d3fa8b6c50a335348b71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424450"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a><span data-ttu-id="0e5fa-103">Определение версии Exchange Server в профиле Outlook</span><span class="sxs-lookup"><span data-stu-id="0e5fa-103">Detect the version of Exchange Server in an Outlook profile</span></span>

<span data-ttu-id="0e5fa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e5fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e5fa-105">В этом разделе представлен пример кода на языке C++, в котором показано, как использовать свойство **[пр_профиле_сервер_версион](pidtagprofileserverversion-canonical-property.md)** и свойство **[пр_профиле_сервер_фулл_версион](pidtagprofileserverfullversion-canonical-property.md)** для получения сведений о версии сервера Microsoft Exchange, на котором активна учетная запись подключено к.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-105">This topic includes a code sample in C++ that shows how to use the **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** property and **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** property to obtain version information of the Microsoft Exchange Server that the active account is connected to.</span></span> 
  
<span data-ttu-id="0e5fa-106">`GetProfileServiceVersion` Функция в образце кода принимает профиль в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-106">The  `GetProfileServiceVersion` function in the code sample accepts a profile as an input parameter.</span></span> <span data-ttu-id="0e5fa-107">В зависимости от того, существует ли свойство **пр_профиле_сервер_версион** и свойство **пр_профиле_сервер_фулл_версион** в заданном профиле, функция получает каждое свойство и возвращает в качестве выходных данных соответствующие сведения о версии. параметры.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-107">Depending on whether the **PR_PROFILE_SERVER_VERSION** property and the **PR_PROFILE_SERVER_FULL_VERSION** property exist in the given profile, the function gets each property and returns the appropriate version information as output parameters.</span></span> 
  
<span data-ttu-id="0e5fa-108">`GetProfileServiceVersion`Сначала вызывается функция **[мапиадминпрофилес](mapiadminprofiles.md)** для создания объекта администрирования профиля.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-108">`GetProfileServiceVersion` first calls the **[MAPIAdminProfiles](mapiadminprofiles.md)** function to create a profile administration object.</span></span> <span data-ttu-id="0e5fa-109">Затем с помощью объекта администрирования профиля вызывается метод **[ипрофадмин:: админсервицес](iprofadmin-adminservices.md)** для получения объекта администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-109">It then uses the profile administration object to call **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** to obtain a message service administration object.</span></span> <span data-ttu-id="0e5fa-110">С помощью объекта администрирования службы сообщений вызывается метод **[имсгсервицеадмин:: опенпрофилесектион](imsgserviceadmin-openprofilesection.md)** , чтобы получить раздел текущего профиля, а затем вызывает **[хржетонепроп](hrgetoneprop.md)** , чтобы проверить, существует ли каждое из этих двух свойств в этом разделе профиль и, если это так, задает сведения о версии в соответствующих выходных параметрах.</span><span class="sxs-lookup"><span data-stu-id="0e5fa-110">Using the message service administration object, it calls **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** to obtain a section of the current profile, and then calls **[HrGetOneProp](hrgetoneprop.md)** to verify if each of the two properties exists in that section of the profile, and if so, sets the version information in the appropriate output parameters.</span></span> 
  
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


