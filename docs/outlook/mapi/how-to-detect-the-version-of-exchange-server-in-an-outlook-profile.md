---
title: Определение версии Exchange Server в профиле Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: 'Последнее изменение: 03 июля 2012 г.'
ms.openlocfilehash: c6aaac128e1a3e1a8d77d3fa8b6c50a335348b71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424450"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a>Определение версии Exchange Server в профиле Outlook

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе содержится пример кода в C++, который показывает, как использовать свойство PR_PROFILE_SERVER_VERSION и **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** для получения сведений о версии Microsoft Exchange Server, к которую подключена активная учетная запись. **[](pidtagprofileserverversion-canonical-property.md)** 
  
Функция в примере кода принимает профиль  `GetProfileServiceVersion` в качестве параметра ввода. В зависимости от  PR_PROFILE_SERVER_VERSION и свойства PR_PROFILE_SERVER_FULL_VERSION  в заданном профиле функция получает каждое свойство и возвращает соответствующую информацию версии в качестве параметров вывода. 
  
`GetProfileServiceVersion` сначала вызывает **[функцию MAPIAdminProfiles](mapiadminprofiles.md)** для создания объекта администрирования профиля. Затем объект администрирования профилей используется для вызова **[объекта администрирования IProfAdmin::AdminServices](iprofadmin-adminservices.md)** для получения объекта администрирования службы сообщений. С помощью объекта администрирования службы сообщений он вызывает **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** для получения раздела текущего профиля, а затем вызывает **[HrGetOneProp,](hrgetoneprop.md)** чтобы проверить, существует ли каждое из двух свойств в этом разделе профиля, и если да, задает сведения о версии в соответствующих параметрах вывода. 
  
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


