---
title: �� ����������� �������, ������������ � Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: aa4d52d25f120e8b3e2a4c0dcaa4845ad576127a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566231"
---
# <a name="about-named-properties-used-by-outlook"></a>�� ����������� �������, ������������ � Outlook

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
MAPI ������������� �������� ��� ���������� ���� ��� ������������ ������� ��� ������������� ���� ���� � ����������� ���������������� � ������������ ����-� ������������� ����� ������������� ������������ ����� ��������. ����������� �������� ���������������� �� ����� � ���������� ���������� ������������� (GUID) ��� ������ �������. ��� ����� ������� ����� ��� ������. ��� Microsoft Outlook 2013 ��� Microsoft Outlook 2010 ����� ������� ���� ����� ������������ ����, ������������ � Outlook�2013 ��� Outlook�2010, ����� ��� **PSETID_Appointment**. 
  
Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range. 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook�2013 or Outlook�2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients. 
  
Outlook�2013 and Outlook�2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook�2013 and Outlook�2010 expose some of these properties as item properties in their Outlook�2013 and Outlook�2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [������������ �������� PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook�2013 and Outlook�2010 are not exposed in the object model. 
  
� ���� ������� ������� ���������� ����������� �������, ������� ����������� ����.
  
���� ������������ ����������� ������� � ������������ ���� **PSETID_Address**. 
  
- [������������ �������� PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)
    
- [������������ �������� PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)
    
- [������������ �������� PidLidEmail1OriginalEntryId](pidlidemail1originalentryid-canonical-property.md)
    
- [������������ �������� PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)
    
- [������������ �������� PidLidEmail2DisplayName](pidlidemail2displayname-canonical-property.md)
    
- [������������ �������� PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)
    
- [������������ �������� PidLidEmail2OriginalDisplayName](pidlidemail2originaldisplayname-canonical-property.md)
    
- [������������ �������� PidLidEmail2OriginalEntryId](pidlidemail2originalentryid-canonical-property.md)
    
- [������������ �������� PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)
    
- [������������ �������� PidLidEmail3DisplayName](pidlidemail3displayname-canonical-property.md)
    
- [������������ �������� PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)
    
- [������������ �������� PidLidEmail3OriginalDisplayName](pidlidemail3originaldisplayname-canonical-property.md)
    
- [������������ �������� PidLidEmail3OriginalEntryId](pidlidemail3originalentryid-canonical-property.md)
    
- [������������ �������� PidLidEmail1DisplayName](pidlidemail1displayname-canonical-property.md)
    
- [������������ �������� PidLidEmail1OriginalDisplayName](pidlidemail1originaldisplayname-canonical-property.md)
    
- [������������ �������� PidLidFileUnder](pidlidfileunder-canonical-property.md)
    
- [������������ �������� PidLidInstantMessagingAddress](pidlidinstantmessagingaddress-canonical-property.md)
    
- [������������ �������� PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)
    
- [������������ �������� PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)
    
- [������������ �������� PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)
    
- [������������ �������� PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [������������ �������� PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)
    
- [������������ �������� PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)
    
- [������������ �������� PidLidYomiCompanyName](pidlidyomicompanyname-canonical-property.md)
    
- [������������ �������� PidLidYomiFirstName](pidlidyomifirstname-canonical-property.md)
    
- [������������ �������� PidLidYomiLastName](pidlidyomilastname-canonical-property.md)
    
���� ������������ ����������� ������� � ������������ ���� **PSETID_Appointment**. 
  
- [������������ �������� PidLidAllAttendeesString](pidlidallattendeesstring-canonical-property.md)
    
- [������������ �������� PidLidAppointmentCounterProposal](pidlidappointmentcounterproposal-canonical-property.md)
    
- [������������ �������� PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)
    
- [������������ �������� PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)
    
- [������������ �������� PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)
    
- [������������ �������� PidLidBusyStatus](pidlidbusystatus-canonical-property.md)
    
- [������������ �������� PidLidCcAttendeesString](pidlidccattendeesstring-canonical-property.md)
    
- [������������ �������� PidLidLocation](pidlidlocation-canonical-property.md)
    
- [������������ �������� PidLidRecurring](pidlidrecurring-canonical-property.md)
    
- [������������ �������� PidLidToAttendeesString](pidlidtoattendeesstring-canonical-property.md)
    
���� ������������ ����������� ������� � ������������ ���� **PSETID_Common**. 
  
- [������������ �������� PidLidCommonEnd](pidlidcommonend-canonical-property.md)
    
- [������������ �������� PidLidCommonStart](pidlidcommonstart-canonical-property.md)
    
- [������������ �������� PidLidCompanies](pidlidcompanies-canonical-property.md)
    
- [������������ �������� PidLidContacts](pidlidcontacts-canonical-property.md)
    
- [������������ �������� PidLidCustomFlag](pidlidcustomflag-canonical-property.md)
    
- [������������ �������� PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [������������ �������� PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [������������ �������� PidLidHeaderItem](pidlidheaderitem-canonical-property.md)
    
- [������������ �������� PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [������������ �������� PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)
    
- [������������ �������� PidLidReminderSet](pidlidreminderset-canonical-property.md)
    
- [������������ �������� PidLidReminderTime](pidlidremindertime-canonical-property.md)
    
- [������������ �������� PidLidFlagRequest](pidlidflagrequest-canonical-property.md)
    
- [������������ �������� PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
- [������������ �������� PidLidSmartNoAttach](pidlidsmartnoattach-canonical-property.md)
    
- [������������ �������� PidLidToDoTitle](pidlidtodotitle-canonical-property.md)
    
- [������������ �������� PidLidUseTnef](pidlidusetnef-canonical-property.md)
    
���� ������������ ����������� ������� � ������������ ���� **PSETID_Meeting**. 
  
- [������������ �������� PidLidMeetingType](pidlidmeetingtype-canonical-property.md)
    
���� ������������ ����������� ������� � ������������ ���� **PSETID_Task**. 
  
- [������������ �������� PidLidTaskActualEffort](pidlidtaskactualeffort-canonical-property.md)
    
- [������������ �������� PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
    
- [������������ �������� PidLidTaskEstimatedEffort](pidlidtaskestimatedeffort-canonical-property.md)
    
- [������������ �������� PidLidTaskFRecurring](pidlidtaskfrecurring-canonical-property.md)
    
- [������������ �������� PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)
    
- [������������ �������� PidLidTaskStatus](pidlidtaskstatus-canonical-property.md)
    
���� ������������ ����������� ������� � ������������ ���� **PS_INTERNET_HEADERS**. 
  
- [������������ �������� PidTagInternetReturnPath](pidtaginternetreturnpath-canonical-property.md)
    
���� ������������ ����������� ������� � ������������ ���� **PSETID_Log**. 
  
- [������������ �������� PidLidLogDuration](pidlidlogduration-canonical-property.md)
    
- [������������ �������� PidLidLogEnd](pidlidlogend-canonical-property.md)
    
- [������������ �������� PidLidLogStart](pidlidlogstart-canonical-property.md)
    
- [������������ �������� PidLidLogType](pidlidlogtype-canonical-property.md)
    
���� ������������ ����������� ������� � ������������ ���� **PS_PUBLIC_STRINGS**. 
  
- [������������ �������� PidNameKeywords](pidnamekeywords-canonical-property.md)
    
- [������������ �������� PidNameExchangeJunkEmailMoveStamp](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>��. �����



[��������� MAPI](mapi-constants.md)
  
[Определение того, скачан ли в Outlook только заголовок сообщения](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[Получение электронного адреса элемента контакта](how-to-get-the-email-address-of-a-contact-item.md)
  
[Удаление определения настраиваемой формы, сохраненного с сообщением](how-to-remove-custom-form-definition-saved-with-a-message.md)

