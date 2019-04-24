---
title: Программное создание профиля в Outlook
manager: soliver
ms.date: 06/02/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a8561a9-df09-453a-b415-c45910625870
description: В этой статье описано, как программно обновить профиль в Outlook 2016, добавив свойство MAPI в раздел emsuid объекта Profile.
ms.openlocfilehash: 85d084705c1e36f5fe3b0ed268094f86b38d6383
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345943"
---
# <a name="programmatically-create-a-profile-in-outlook"></a><span data-ttu-id="2b4a8-103">Программное создание профиля в Outlook</span><span class="sxs-lookup"><span data-stu-id="2b4a8-103">Programmatically create a profile in Outlook</span></span>

<span data-ttu-id="2b4a8-104">**Относится к**: Office 365 | Outlook | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b4a8-104">**Applies to**: Office 365 | Outlook | Outlook 2016</span></span> 

<span data-ttu-id="2b4a8-105">В этой статье описано, как программно обновить профиль в Outlook 2016, добавив свойство MAPI в раздел **emsuid** объекта Profile.</span><span class="sxs-lookup"><span data-stu-id="2b4a8-105">This topic describes how to programmatically update a profile in Outlook 2016 by adding a MAPI property to the **emsuid** section of the Profile object.</span></span> 

<span data-ttu-id="2b4a8-106">В MAPI можно обновить профиль, задав свойство **PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)**, как описано ранее.</span><span class="sxs-lookup"><span data-stu-id="2b4a8-106">In MAPI, you can update a profile by setting the property **PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)**, as indicated in the procedure below.</span></span> 
  
### <a name="set-the-property-for-outlook-2016"></a><span data-ttu-id="2b4a8-107">Задание свойства для Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b4a8-107">Set the property for Outlook 2016</span></span>

1. <span data-ttu-id="2b4a8-108">Убедитесь, что свойство для Outlook 2016 настроено.</span><span class="sxs-lookup"><span data-stu-id="2b4a8-108">Make sure Outlook 2016 is property configured.</span></span>
    
2. <span data-ttu-id="2b4a8-109">С помощью интерфейса [IMAPIProp](https://msdn.microsoft.com/library/cc815525.aspx) перейдите к разделу "Профиль Outlook".</span><span class="sxs-lookup"><span data-stu-id="2b4a8-109">Using the [IMAPIProp](https://msdn.microsoft.com/library/cc815525.aspx) interface, go to the Outlook Profile section.</span></span> 
    
   <span data-ttu-id="2b4a8-p101">Это может быть сложно в MAPI Outlook, так как в версии 2010 и более поздних больше нет раздела глобального профиля. Чтобы найти раздел профиля, найдите свойство PR_EMSMDB_SECTION_UID (0x3D150102). Значением будет идентификатор GUID раздела профиля, сохраненный в двоичной форме, который будет использоваться при выполнении последующих шагов. Это значение нужно записать.</span><span class="sxs-lookup"><span data-stu-id="2b4a8-p101">This can be difficult in Outlook's MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. You will need to remember this value.</span></span> 
    
3. <span data-ttu-id="2b4a8-114">Добавьте свойство **PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W**.</span><span class="sxs-lookup"><span data-stu-id="2b4a8-114">Add the property **PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W**.</span></span> 
    
4. <span data-ttu-id="2b4a8-115">Задайте свойство **0x6641001F** для магазина и укажите раздел **emsuid** для всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="2b4a8-115">Set the property **0x6641001F** on the store and the **emsuid** section for all providers.</span></span> 
    
5. <span data-ttu-id="2b4a8-116">Задайте свойство **PR_DISPLAY_NAME**.</span><span class="sxs-lookup"><span data-stu-id="2b4a8-116">Set the property **PR_DISPLAY_NAME**.</span></span> 
    
## <a name="code-example"></a><span data-ttu-id="2b4a8-117">Пример кода</span><span class="sxs-lookup"><span data-stu-id="2b4a8-117">Code example</span></span>

```cpp
// CreateProfile.cpp : Defines the entry point for the console application.
//
#include "stdafx.h"
#include <Windows.h>
#include <MAPIX.h>
#include <MAPIUtil.h>
#include <EdkMdb.h>
#include <iostream>
#include <vector>
#include <map>
using namespace std;
#define PR_PROFILE_USER_SMTP_EMAIL_ADDRESS                  PROP_TAG(PT_TSTRING, pidProfileMin+0x41)
#define PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W                PROP_TAG(PT_UNICODE, pidProfileMin+0x41)
#define PR_EMSMDB_SECTION_UID                               PROP_TAG(PT_BINARY, 0x3D15)
#define MAPI_FORCE_ACCESS                                   0x80000
STDMETHODIMP GetGlobalProfileSection(LPSERVICEADMIN lpSvcAdmin, LPMAPIUID lpMapiUid, ULONG ulFlags, LPPROFSECT * lppProfSect);
STDMETHODIMP GetEMSMDBVarProfileSection(LPSERVICEADMIN lpSvcAdmin, LPPROFSECT lpGlobalProfSection, LPPROFSECT * lppProfSect);
std::map<ULONG, LPWSTR> PropValueMap
{
    {
        PR_DISPLAY_NAME_W,
        L"Anthony"
    },
    {
        PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W,
        L"=SMTP:anthony@contoso.com"
    }
};
int _tmain(int argc, _TCHAR* argv[])
{
    HRESULT             hRes = S_OK;            // Result from MAPI calls.
    LPPROFADMIN         lpProfAdmin = NULL;     // Profile Admin object.
    LPSERVICEADMIN      lpSvcAdmin = NULL;      // Service Admin object.
    LPMAPITABLE         lpMsgSvcTable = NULL;   // Table to hold services.
    LPSRowSet           lpSvcRows = NULL;       // Rowset to hold results of table query.
    vector<SPropValue>  rgvals;
    SRestriction        sres;                   // Restriction structure.
    SPropValue          SvcProps;               // Property structure for restriction.
    LPPROFSECT          lpGlobalProfSection = nullptr;
    LPPROFSECT          lpEmsMdbVarProfSect = nullptr;
    SPropValue          spvSmtpAddressW;
    SPropValue          spvDisplayName;
    // This indicates columns we want returned from HrQueryAllRows.
    enum { iSvcName, iSvcUID, cptaSvc };
    SizedSPropTagArray(cptaSvc, sptCols) = { cptaSvc, PR_SERVICE_NAME, PR_SERVICE_UID };
    string ProfileName = "MAPIProfile";
    // Initialize MAPI.
    if (FAILED(hRes = MAPIInitialize(NULL)))
    {
        cout << "Error initializing MAPI.";
        goto error;
    }
    // Get an IProfAdmin interface.
    if (FAILED(hRes = MAPIAdminProfiles(0,              // Flags.
        &lpProfAdmin))) // Pointer to new IProfAdmin.
    {
        cout << "Error getting IProfAdmin interface.";
        goto error;
    }
    // Create a new profile.
    if (FAILED(hRes = lpProfAdmin->CreateProfile((LPTSTR)ProfileName.c_str(),     // Name of new profile.
                                                    nullptr,          // Password for profile.
                                                    0,          // Handle to parent window.
                                                    0)))        // Flags.
    {
        cout << "Error creating profile.";
        goto error;
    }
    // Get an IMsgServiceAdmin interface off of the IProfAdmin interface.
    if (FAILED(hRes = lpProfAdmin->AdminServices((LPTSTR)ProfileName.c_str(),     // Profile that we want to modify.
                                                    nullptr,          // Password for that profile.
                                                    0,          // Handle to parent window.
                                                    0,             // Flags.
                                                    &lpSvcAdmin))) // Pointer to new IMsgServiceAdmin.
    {
        cout << "Error getting IMsgServiceAdmin interface.";
        goto error;
    }
    // Create the new message service for Exchange.
    if (FAILED(hRes = lpSvcAdmin->CreateMsgService("MSEMS",     // Name of service from MAPISVC.INF.
                                                    NULL,        // Display name of service.
                                                    NULL,        // Handle to parent window.
                                                    NULL)))      // Flags.
    {
        cout << "Error creating Exchange message service.";
        goto error;
    }
    // You now have to obtain the entry id for the new service.
    // You can do this by getting the message service table
    // and getting the entry that corresponds to the new service.
    if (FAILED(hRes = lpSvcAdmin->GetMsgServiceTable(0,                 // Flags.
                                                    &lpMsgSvcTable)))  // Pointer to table.
    {
        cout << "Error getting Message Service Table.";
        goto error;
    }
    // Set up restriction to query table.
    sres.rt = RES_CONTENT;
    sres.res.resContent.ulFuzzyLevel = FL_FULLSTRING;
    sres.res.resContent.ulPropTag = PR_SERVICE_NAME;
    sres.res.resContent.lpProp = &SvcProps;
    SvcProps.ulPropTag = PR_SERVICE_NAME;
    SvcProps.Value.lpszA = "MSEMS";
    // Query the table to obtain the entry for the newly created message service.
    if (FAILED(hRes = HrQueryAllRows(lpMsgSvcTable,
                                        (LPSPropTagArray)&sptCols,
                                        &sres,
                                        NULL,
                                        0,
                                        &lpSvcRows)))
    {
        cout << "Error querying table for new message service.";
        goto error;
    }
    ZeroMemory(&spvSmtpAddressW, sizeof(spvSmtpAddressW));
    spvSmtpAddressW.ulPropTag = PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W;
    spvSmtpAddressW.Value.lpszW = PropValueMap[PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W];
    rgvals.push_back(spvSmtpAddressW);
    // Configure the message service by using the previous properties.
    //if (FAILED(hRes = lpSvcAdmin->ConfigureMsgService(
    //                                                  (LPMAPIUID)lpSvcRows->aRow->lpProps[iSvcUID].Value.bin.lpb, // Entry ID of service to configure.
    //                                                  NULL,                                                       // Handle to parent window.
    //                                                  0,                                                          // Flags.
    //                                                  rgvals.size(),                                                          // Number of properties we are setting.
    //                                                  rgvals.data())))                                                    // Pointer to SPropValue array.
    //{
    //  cout << "Error configuring message service.";
    //  goto error;
    //}
    if (FAILED(hRes = GetGlobalProfileSection(
                                                    lpSvcAdmin, 
                                                    (LPMAPIUID)lpSvcRows->aRow->lpProps[iSvcUID].Value.bin.lpb, 
                                                    MAPI_MODIFY, 
                                                    &lpGlobalProfSection)))
    {
        cout << "Error attempting to get the Global Profile Section.";
        goto error;
    }
    if (FAILED(hRes = lpGlobalProfSection->SetProps(
                                                    rgvals.size(),
                                                    rgvals.data(),
                                                    nullptr)))
    {
        cout << "Error attempting to set the smtp address.";
        goto error;
    }
    if (FAILED(hRes = lpGlobalProfSection->SaveChanges(
                                                        KEEP_OPEN_READWRITE)))
    {
        cout << "Error attempting to save after setting the smtp address";
        goto error;
    }
    if (FAILED(hRes = GetEMSMDBVarProfileSection(lpSvcAdmin, lpGlobalProfSection, &lpEmsMdbVarProfSect)))
    {
        goto error;
    }
    ZeroMemory(&spvDisplayName, sizeof(spvDisplayName));
    spvDisplayName.ulPropTag = PR_DISPLAY_NAME_W;
    spvDisplayName.Value.lpszW = PropValueMap[PR_DISPLAY_NAME_W];
    rgvals.push_back(spvDisplayName);
    if (FAILED(hRes = lpEmsMdbVarProfSect->SetProps(
                                                    rgvals.size(),
                                                    rgvals.data(),
                                                    nullptr)))
    {
        cout << "Error call set props on the ems mdb var prof sect using the smtp address";
        goto error;
    }
    if (FAILED(hRes = lpEmsMdbVarProfSect->SaveChanges(
                                                        KEEP_OPEN_READWRITE)))
    {
        cout << "Error attempting to save after setting the smtp address on the ems mdb var prof sect";
        goto error;
    }
cleanup:
    // Clean up
    if (lpEmsMdbVarProfSect) lpEmsMdbVarProfSect->Release();
    if (lpGlobalProfSection) lpGlobalProfSection->Release();
    if (lpSvcRows) FreeProws(lpSvcRows);
    if (lpMsgSvcTable) lpMsgSvcTable->Release();
    if (lpSvcAdmin) lpSvcAdmin->Release();
    if (lpProfAdmin) lpProfAdmin->Release();
    MAPIUninitialize();
    return 0;
error:
    cout << " hRes = 0x" << hex << hRes << dec << endl;
    goto cleanup;
}
STDMETHODIMP GetGlobalProfileSection(LPSERVICEADMIN lpSvcAdmin, LPMAPIUID lpMapiUid, ULONG ulFlags, LPPROFSECT * lppProfSect)
{
    HRESULT         hRes = MAPI_E_CALL_FAILED;
    LPPROFSECT      lpProfSect = nullptr;
    LPPROFSECT      lpEmsMdbVarProfSect = nullptr;
    ULONG           cValues = 0;
    LPSPropValue    lpProps = nullptr;
    SizedSPropTagArray(1, spta) = { 1, { PR_EMSMDB_SECTION_UID } };
    *lppProfSect = nullptr;
    hRes = lpSvcAdmin->OpenProfileSection(lpMapiUid,
        0,
        MAPI_FORCE_ACCESS,
        &lpProfSect);
    if (FAILED(hRes) || lpProfSect == nullptr)
    {
        return hRes;
    }
    hRes = lpProfSect->GetProps((LPSPropTagArray)&spta, 0, &cValues, &lpProps);
    if (FAILED(hRes) || lpProps == nullptr || cValues == 0)
    {
        return hRes;
    }
    if (lpProps[0].ulPropTag != PR_EMSMDB_SECTION_UID)
    {
        hRes = lpProps[0].Value.err;
        goto Cleanup;
    }
    hRes = lpSvcAdmin->OpenProfileSection((LPMAPIUID)lpProps->Value.bin.lpb, 0, ulFlags, &lpEmsMdbVarProfSect);
    if (FAILED(hRes) || lpEmsMdbVarProfSect == nullptr)
    {
        goto Cleanup;
    }
    *lppProfSect = lpEmsMdbVarProfSect;
Cleanup:
    if (lpProps)
    {
        MAPIFreeBuffer(lpProps);
    }
    if (lpProfSect)
    {
        lpProfSect->Release();
    }
    return hRes;
}
STDMETHODIMP GetEMSMDBVarProfileSection(LPSERVICEADMIN lpSvcAdmin, LPPROFSECT lpGlobalProfSection, LPPROFSECT * lppProfSect)
{
    HRESULT hRes = MAPI_E_CALL_FAILED;
    SizedSPropTagArray(1, sptaStoreProviders) = { 1, { PR_STORE_PROVIDERS } };
    ULONG               cValues = 0;
    LPSPropValue        lpProps = nullptr;
    LPPROFSECT          lpProfSect = nullptr;
    if (!lpSvcAdmin || !lpGlobalProfSection || !lppProfSect)
        return E_INVALIDARG;
    *lppProfSect = nullptr;
    if (FAILED(hRes = lpGlobalProfSection->GetProps(
        (LPSPropTagArray)&sptaStoreProviders,
        0,
        &cValues,
        &lpProps)) || cValues == 0 || lpProps == nullptr)
    {
        cout << "Error attempting to get the PR_STORE_PROVIDERS property " << endl;
        goto Cleanup;
    }
    if (lpProps->ulPropTag != sptaStoreProviders.aulPropTag[0])
    {
        hRes = lpProps->Value.err;
        goto Cleanup;
    }
    if (FAILED(hRes = lpSvcAdmin->OpenProfileSection(
        (LPMAPIUID)lpProps->Value.bin.lpb,
        0,
        MAPI_FORCE_ACCESS | MAPI_MODIFY,
        &lpProfSect)) || lpProfSect == nullptr)
    {
        cout << "Could not open the profile section using the PR_STORE_PROVIDERS property " << endl;
        goto Cleanup;
    }
    *lppProfSect = lpProfSect;
Cleanup:
    if (lpProps)
    {
        MAPIFreeBuffer(lpProps);
        lpProps = nullptr;
    }
    return hRes;
}
```

## <a name="use-mfcmapi-to-configure-outlook-profiles"></a><span data-ttu-id="2b4a8-118">Настройка профилей Outlook с помощью MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2b4a8-118">Use MFCMAPI to configure Outlook profiles</span></span>

<span data-ttu-id="2b4a8-119">[MFCMAPI](https://mfcmapi.codeplex.com) предоставляет доступ к магазинам MAPI для изучения проблем с Exchange и Outlook, а также для предоставления разработчикам поддержки по MAPI.</span><span class="sxs-lookup"><span data-stu-id="2b4a8-119">[MFCMAPI](https://mfcmapi.codeplex.com) provides access to MAPI stores to facilitate investigation of Exchange and Outlook issues and to provide developers support for MAPI development.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b4a8-120">См. также</span><span class="sxs-lookup"><span data-stu-id="2b4a8-120">See also</span></span>

- [<span data-ttu-id="2b4a8-121">Создание профиля Outlook с помощью MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2b4a8-121">Create an Outlook profile using MFCMAPI</span></span>](https://msdn.microsoft.com/library/office/mt723322.aspx)
  

