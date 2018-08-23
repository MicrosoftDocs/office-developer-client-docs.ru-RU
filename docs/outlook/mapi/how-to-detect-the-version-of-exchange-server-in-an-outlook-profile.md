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
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a>Определить, какая версия Exchange Server в профиле Outlook

**Применимо к**: Outlook 2013 | Outlook 2016 
  
В этом разделе приводится пример кода c++, который показано, как использовать свойство **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** и свойство **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** для получения сведений о версии сервера Microsoft Exchange Server, который является активной учетной записи подключение. 
  
`GetProfileServiceVersion` Функции в образце кода принимает профиль в качестве входного параметра. В зависимости от того, является ли свойство **PR_PROFILE_SERVER_VERSION** и свойство **PR_PROFILE_SERVER_FULL_VERSION** существует в заданного профиля функция возвращает каждого свойства и возвращает соответствующую версию данных в качестве выходных данных параметры. 
  
`GetProfileServiceVersion`Сначала вызывается функция **[MAPIAdminProfiles](mapiadminprofiles.md)** для создания объекта администрирования профилей. Затем объект администрирования профилей используется для вызова **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** , чтобы получить объект администрирования службы сообщений. С помощью объекта message службы администрирования, он вызывает **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** для получения части текущего профиля, а затем вызывает **[HrGetOneProp](hrgetoneprop.md)** , чтобы проверить, существует ли каждый из двух свойств в данном разделе профиль и если да, наборов сведений о версии в соответствующие выходные параметры. 
  
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


