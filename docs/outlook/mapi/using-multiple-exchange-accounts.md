---
title: ������������� ���������� ������� ������� Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723063"
---
# <a name="using-multiple-exchange-accounts"></a>������������� ���������� ������� ������� Exchange

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 и Microsoft Outlook 2013 поддерживает интеграцию с несколькими учетными записями электронной почты exchange. � Outlook�2010 ��� Outlook�2013 ������������ ����� �������� ��� ������� ������� exchange ��� ������ ������� � ��-�������� ������� �������� ����������� � ����������� ������� Exchange, �������� �������������� ����������� ������ ������� (GAL), Exchange-���������� ������������ � ����� ������ � �����.
  
Эти знакомы с разделами профилей MAPI для Microsoft Office Outlook 2007 и более ранних версий знать, что параметры Exchange, такие как имя пользователя электронной почты и имя сервера, хранятся в основных раздела глобального профиля Exchange, **pbGlobalProfileSectionGuid**. � Outlook�2010 � Outlook�2013 ������ ������� ������ Exchange ��������� ����������� ������ ������� ��� �������� ����������, ����������� **pbGlobalProfileSectionGuid**. 
  
Outlook�2010 and Outlook�2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [������������ �������� PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.
  
Outlook�2010 � Outlook�2013 ������������ **PidTagExchangeProfileSectionId** � �������� ����������� �������������� ��� �������� ������� ������ Exchange. ��� ������������� ����� �������, ���� ���������� ������������� ���������� **emsmdbUID**. ��� ��������� �������� MAPI � Outlook **emsmdbUID** ����� ������������� �������, ����� ������� ������ Exchange ������� ������������ ��� ��������. 
  
In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser: IMAPIProp](imailuserimapiprop.md) and [IDistList: IMAPIContainer](idistlistimapicontainer.md) with one of the following functions. 
  
- [HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
    
- [HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
    
- [HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
    
- [HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
    
- [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
    
- [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
    
- [HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
    
- [HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
    
- [HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a>��������� �����������

��� ������� MAPI, ���������� ����� ��������� ���� ����� ������ **emsmdbUID** ��-�������� ��������������. ��� ������� ����� ���������� ��� ��������� ���������� ����, **pbGlobalProfileSectionGuid**. ������� ��� ����� ������� ����� ���������������� � ����� ���������� ������� ������ Exchange, ������� ������������ ������� ������� ������. ������� ������, ������� ������������ ������� ������ ������ ����� ����������, ��������� ������� ������ ��������� � ���������� ������� ��� PR_EMSMDB_LEGACY. ������ ���� ������ ��������� ����� ����� ��� �������� true � ��� **PidTagExchangeProfileSectionId** ���������� ������� ������ **emsmdbUID**.
  
> [!NOTE]
> [!����������] ������������� ��������� MAPI, ����� ��� ��������� �� ��������� � ������� ������ �� ��������� �� ��������� �������� �������, �� ������� ������� ������ ������������ ������ ������� ������. �� ������� ������ ������� ������, ������� ������������ ������ ������� ������. 
  
**emsmdbUID** ������� ������ ������� ������ ���������� � Outlook ����������� ������� �������. ���� ��� �������� �� ����������, ������ ��� ������� ����� ��������� ����� ����������, ����� ������� ������ �������� ���������� ������� ������ � ������� �������� � Outlook ����������� ������� �������. 
  
���������� �����, Outlook ����������� ������� ������� ���������� �� ����������� ������� ������� Exchange, � � Outlook�2010 � Outlook�2013 ����������� ������� ������� Exchange ������ �� ������������� ���������� ��������� ������� ��������� ������� ������� Exchange. Outlook ������ ���������� ������� �������� �������� � Outlook, ����� ��� ��������� ����� MRU ��� ��������� ���������� �����������.
  
## <a name="address-book-account-contexts"></a>�������� ����� ���������� ������� ������

����� ��������� ������ ��������� � ����������� �������� �������� Exchange, ����������� ����� �������, ����������� �������� ������� ������, ����� ������ � �������� ����� ����� ���������� ������� ������ Exchange.
  
��������� ���������� �������� ����� API-���������� ���� ����������, ��������� API-����������, �� ��������������� ��������� ��������� Exchange. � ���� ��������� ������� ������ ������ �������� **emsmdbUID**.
  
� ���������� � **emsmdbUID** **emsabpUID**����� ����� ��������� ������� ������� Exchange.
  
1. �������� **emsmdbUID** ���������� �������� ������� ������. 
    
2. �������� **emsabpUID** ���������� ���������� Exchange �������� ����. 
    
The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient. 
  
���� �� ������ ���������� �������� **emsabpUID** ��� ������������� **emsmdbUID**, �������� ������ ������� ��� **emsmdbUID** � �������� �������� **PR_EMSABP_USER_UID** (0x0x3D1A0102). 
  
If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.
  
������� �������� �������� ���������� ���������� ������� ������� Exchange �������� ��������� �������:
  
- �������� ���������� ������������� ������, ��� ��������� � ������� ��������� ���������, ������� �������������, � ��� ���� �������� **PR_SERVICE_UID**. ������ ����� ���������� ���������� **PR_MDB_PROVIDER**. ��� ������ �������� ������ ���������������� ��������.
    
- �������� **emsmdbUID**, ��� ��������� � ������� ����� ��������� ��� ������, ������� ������������� **PidTagExchangeProfileSectionId**, ������� ������������� **emsmdbUID**.
    
## <a name="see-also"></a>��. �����



[HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
  
[HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
  
[HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
  
[HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
  
[HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
  
[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
  
[HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
  
[HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
  
[HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
  
[HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
  
[������������ �������� PidTagExchangeProfileSectionId](pidtagexchangeprofilesectionid-canonical-property.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

