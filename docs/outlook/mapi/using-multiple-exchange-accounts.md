---
title: ������������� ���������� ������� ������� Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 3c0392cd6a885900c1a305cd1cd816a5925745a7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398593"
---
# <a name="using-multiple-exchange-accounts"></a><span data-ttu-id="9ef7c-103">������������� ���������� ������� ������� Exchange</span><span class="sxs-lookup"><span data-stu-id="9ef7c-103">Using Multiple Exchange Accounts</span></span>

  
  
<span data-ttu-id="9ef7c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ef7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ef7c-105">Microsoft Outlook 2010 и Microsoft Outlook 2013 поддерживает интеграцию с несколькими учетными записями электронной почты exchange.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-105">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange email accounts.</span></span> <span data-ttu-id="9ef7c-106">� Outlook�2010 ��� Outlook�2013 ������������ ����� �������� ��� ������� ������� exchange ��� ������ ������� � ��-�������� ������� �������� ����������� � ����������� ������� Exchange, �������� �������������� ����������� ������ ������� (GAL), Exchange-���������� ������������ � ����� ������ � �����.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-106">In Outlook 2010 or Outlook 2013, a user could add two exchange accounts to the same profile and still enjoy rich Exchange features such as the published global address list (GAL), Exchange Out-of-Office configuration, and folder sharing.</span></span>
  
<span data-ttu-id="9ef7c-107">Эти знакомы с разделами профилей MAPI для Microsoft Office Outlook 2007 и более ранних версий знать, что параметры Exchange, такие как имя пользователя электронной почты и имя сервера, хранятся в основных раздела глобального профиля Exchange, **pbGlobalProfileSectionGuid**.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-107">Those familiar with the MAPI profile sections for Microsoft Office Outlook 2007 and earlier know that Exchange settings, such as the email user name and server name, are stored in the fixed Exchange Global Profile section, **pbGlobalProfileSectionGuid**.</span></span> <span data-ttu-id="9ef7c-108">�������������� �������� � ���������� ������� Exchange ����� [�������� ����������� ������� �������](https://support.microsoft.com/kb/188482).</span><span class="sxs-lookup"><span data-stu-id="9ef7c-108">For more information about the Exchange Global Profile, see [How To Open the Global Profile Section](https://support.microsoft.com/kb/188482).</span></span> <span data-ttu-id="9ef7c-109">� Outlook�2010 � Outlook�2013 ������ ������� ������ Exchange ��������� ����������� ������ ������� ��� �������� ����������, ����������� **pbGlobalProfileSectionGuid**.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-109">In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the **pbGlobalProfileSectionGuid** obsolete.</span></span> 
  
<span data-ttu-id="9ef7c-p103">Outlook�2010 and Outlook�2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [������������ �������� PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span></span>
  
<span data-ttu-id="9ef7c-p104">Outlook�2010 � Outlook�2013 ������������ **PidTagExchangeProfileSectionId** � �������� ����������� �������������� ��� �������� ������� ������ Exchange. ��� ������������� ����� �������, ���� ���������� ������������� ���������� **emsmdbUID**. ��� ��������� �������� MAPI � Outlook **emsmdbUID** ����� ������������� �������, ����� ������� ������ Exchange ������� ������������ ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-p104">Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account. When used in this manner, this unique identifier is known as the **emsmdbUID**. For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation.</span></span> 
  
<span data-ttu-id="9ef7c-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser: IMAPIProp](imailuserimapiprop.md) and [IDistList: IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span></span> 
  
- [<span data-ttu-id="9ef7c-119">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="9ef7c-119">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
    
- [<span data-ttu-id="9ef7c-120">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="9ef7c-120">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
    
- [<span data-ttu-id="9ef7c-121">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="9ef7c-121">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
    
- [<span data-ttu-id="9ef7c-122">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="9ef7c-122">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
    
- [<span data-ttu-id="9ef7c-123">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="9ef7c-123">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
    
- [<span data-ttu-id="9ef7c-124">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="9ef7c-124">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
    
- [<span data-ttu-id="9ef7c-125">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="9ef7c-125">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
    
- [<span data-ttu-id="9ef7c-126">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="9ef7c-126">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
    
- [<span data-ttu-id="9ef7c-127">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="9ef7c-127">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
    
- [<span data-ttu-id="9ef7c-128">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="9ef7c-128">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a><span data-ttu-id="9ef7c-129">��������� �����������</span><span class="sxs-lookup"><span data-stu-id="9ef7c-129">Legacy support</span></span>

<span data-ttu-id="9ef7c-p106">��� ������� MAPI, ���������� ����� ��������� ���� ����� ������ **emsmdbUID** ��-�������� ��������������. ��� ������� ����� ���������� ��� ��������� ���������� ����, **pbGlobalProfileSectionGuid**. ������� ��� ����� ������� ����� ���������������� � ����� ���������� ������� ������ Exchange, ������� ������������ ������� ������� ������. ������� ������, ������� ������������ ������� ������ ������ ����� ����������, ��������� ������� ������ ��������� � ���������� ������� ��� PR_EMSMDB_LEGACY. ������ ���� ������ ��������� ����� ����� ��� �������� true � ��� **PidTagExchangeProfileSectionId** ���������� ������� ������ **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-p106">Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported. These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**. Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries. The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY. Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9ef7c-p107">[!����������] ������������� ��������� MAPI, ����� ��� ��������� �� ��������� � ������� ������ �� ��������� �� ��������� �������� �������, �� ������� ������� ������ ������������ ������ ������� ������. �� ������� ������ ������� ������, ������� ������������ ������ ������� ������.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-p107">Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls. The account that handles the legacy calls cannot be configured.</span></span> 
  
<span data-ttu-id="9ef7c-p108">**emsmdbUID** ������� ������ ������� ������ ���������� � Outlook ����������� ������� �������. ���� ��� �������� �� ����������, ������ ��� ������� ����� ��������� ����� ����������, ����� ������� ������ �������� ���������� ������� ������ � ������� �������� � Outlook ����������� ������� �������.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-p108">The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section. If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section.</span></span> 
  
<span data-ttu-id="9ef7c-p109">���������� �����, Outlook ����������� ������� ������� ���������� �� ����������� ������� ������� Exchange, � � Outlook�2010 � Outlook�2013 ����������� ������� ������� Exchange ������ �� ������������� ���������� ��������� ������� ��������� ������� ������� Exchange. Outlook ������ ���������� ������� �������� �������� � Outlook, ����� ��� ��������� ����� MRU ��� ��������� ���������� �����������.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-p109">To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts. The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.</span></span>
  
## <a name="address-book-account-contexts"></a><span data-ttu-id="9ef7c-141">�������� ����� ���������� ������� ������</span><span class="sxs-lookup"><span data-stu-id="9ef7c-141">Address Book Account Contexts</span></span>

<span data-ttu-id="9ef7c-142">����� ��������� ������ ��������� � ����������� �������� �������� Exchange, ����������� ����� �������, ����������� �������� ������� ������, ����� ������ � �������� ����� ����� ���������� ������� ������ Exchange.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-142">To resolve addresses correctly with multiple Exchange accounts, use the new functions that take an account context so that calls to the address book search the correct Exchange account.</span></span>
  
<span data-ttu-id="9ef7c-p110">��������� ���������� �������� ����� API-���������� ���� ����������, ��������� API-����������, �� ��������������� ��������� ��������� Exchange. � ���� ��������� ������� ������ ������ �������� **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-p110">Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable. This account context is usually an **emsmdbUID**.</span></span>
  
<span data-ttu-id="9ef7c-145">� ���������� � **emsmdbUID** **emsabpUID**����� ����� ��������� ������� ������� Exchange.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-145">In addition to the **emsmdbUID**, multiple Exchange accounts also have an **emsabpUID**.</span></span>
  
1. <span data-ttu-id="9ef7c-146">�������� **emsmdbUID** ���������� �������� ������� ������.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-146">The **emsmdbUID** value identifies the account context.</span></span> 
    
2. <span data-ttu-id="9ef7c-147">�������� **emsabpUID** ���������� ���������� Exchange �������� ����.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-147">The **emsabpUID** value identifies an Exchange address book provider.</span></span> 
    
<span data-ttu-id="9ef7c-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span></span> 
  
<span data-ttu-id="9ef7c-151">���� �� ������ ���������� �������� **emsabpUID** ��� ������������� **emsmdbUID**, �������� ������ ������� ��� **emsmdbUID** � �������� �������� **PR_EMSABP_USER_UID** (0x0x3D1A0102).</span><span class="sxs-lookup"><span data-stu-id="9ef7c-151">If you want to determine the **emsabpUID** value for a particular **emsmdbUID**, open up the profile section for the **emsmdbUID** and get the **PR_EMSABP_USER_UID** (0x0x3D1A0102) property.</span></span> 
  
<span data-ttu-id="9ef7c-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span></span>
  
<span data-ttu-id="9ef7c-155">������� �������� �������� ���������� ���������� ������� ������� Exchange �������� ��������� �������:</span><span class="sxs-lookup"><span data-stu-id="9ef7c-155">A simple description of the process for resolving multiple Exchange accounts is as follows:</span></span>
  
- <span data-ttu-id="9ef7c-p113">�������� ���������� ������������� ������, ��� ��������� � ������� ��������� ���������, ������� �������������, � ��� ���� �������� **PR_SERVICE_UID**. ������ ����� ���������� ���������� **PR_MDB_PROVIDER**. ��� ������ �������� ������ ���������������� ��������.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-p113">Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have. From there, you can determine the correct **PR_MDB_PROVIDER**. This row contains the appropriate store.</span></span>
    
- <span data-ttu-id="9ef7c-159">�������� **emsmdbUID**, ��� ��������� � ������� ����� ��������� ��� ������, ������� ������������� **PidTagExchangeProfileSectionId**, ������� ������������� **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="9ef7c-159">Given an **emsmdbUID**, your code looks in the message services table for the row that exposes the **PidTagExchangeProfileSectionId** that matches the **emsmdbUID**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ef7c-160">��. �����</span><span class="sxs-lookup"><span data-stu-id="9ef7c-160">See also</span></span>



[<span data-ttu-id="9ef7c-161">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="9ef7c-161">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
  
[<span data-ttu-id="9ef7c-162">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="9ef7c-162">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
  
[<span data-ttu-id="9ef7c-163">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="9ef7c-163">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
  
[<span data-ttu-id="9ef7c-164">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="9ef7c-164">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
  
[<span data-ttu-id="9ef7c-165">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="9ef7c-165">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
  
[<span data-ttu-id="9ef7c-166">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="9ef7c-166">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
  
[<span data-ttu-id="9ef7c-167">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="9ef7c-167">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
  
[<span data-ttu-id="9ef7c-168">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="9ef7c-168">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
  
[<span data-ttu-id="9ef7c-169">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="9ef7c-169">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
  
[<span data-ttu-id="9ef7c-170">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="9ef7c-170">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
  
[<span data-ttu-id="9ef7c-171">������������ �������� PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="9ef7c-171">PidTagExchangeProfileSectionId Canonical Property</span></span>](pidtagexchangeprofilesectionid-canonical-property.md)


[<span data-ttu-id="9ef7c-172">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="9ef7c-172">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

