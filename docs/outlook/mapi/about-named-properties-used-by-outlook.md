---
title: Сведения об именованных свойствах, используемых в Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: aa4d52d25f120e8b3e2a4c0dcaa4845ad576127a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566231"
---
# <a name="about-named-properties-used-by-outlook"></a>Сведения об именованных свойствах, используемых в Outlook

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI предоставляет возможность назначения имен определенным свойствам для привязки этих имен к уникальным идентификаторам и сохранения этой карты сопоставления названий и идентификаторов для всех сессий. Именованные свойства определяются по имени и глобальному уникальному идентификатору (GUID) для набора свойств. Имя может представлять собой число или строку. Для Microsoft Outlook 2013 или Microsoft Outlook 2010 набор свойств часто представляет собой пространство имен, определенное Outlook 2013 или Outlook 2010, например, **PSETID_Appointment**. 
  
Именованные свойства управляются с помощью функции [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и функции [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). Имя, а также набор свойств GUID, передаются функции [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения идентификатора свойства, который действует для текущей сессии MAPI. Поскольку этот идентификатор свойства может различаться на разных компьютерах, единственным надежным способом доступа к именованному свойству состоит в получении его имени и набора свойств GUID. Значения идентификаторов всегда находятся в диапазоне от 0x8000 до 0xFFFE. 
  
Любой объект, который использует интерфейс[IMAPIProp: IUnknown](imapipropiunknown.md), поддерживает именованные свойства. В частности, поставщик услуг MAPI или клиент MAPI обязан использовать [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значений именованных свойств. Конфигурация именованных свойств, которые используются Outlook 2013 или Outlook 2010, не поддерживается из-за риска повреждения данных, которые используются совместно с другими поставщиками услуг или клиентами MAPI. 
  
Outlook 2013 и Outlook 2010 используют именованный свойства MAPI для реализации множества своих функций, например, обеспечение безопасности вложений и встречные предложения для встречи. Помимо этих базовых данных Outlook 2013 и Outlook 2010 отображает некоторые из этих свойств в качестве свойств элементов в объектных моделях Outlook 2013 и Outlook 2010. Например, свойство **Email1Address** объекта **ContactItem** в объектной модели соответствует именованному [общепринятому свойству PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) в пространстве имен**PSETID_Address**. Но как правило, из-за проблем обеспечения совместимости и целостности данных многие свойства MAPI, которые используются Outlook 2013 и Outlook 2010, не используются в объектной модели. 
  
Эта справочная информация описывает количество именованных свойств, указанные в списке ниже.
  
В пространстве имен **PSETID_Address** используются следующие именованные свойства: 
  
- [Каноническое свойство PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)
    
- [Каноническое свойство PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)
    
- [Каноническое свойство PidLidEmail1OriginalEntryId](pidlidemail1originalentryid-canonical-property.md)
    
- [Каноническое свойство PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)
    
- [Каноническое свойство PidLidEmail2DisplayName](pidlidemail2displayname-canonical-property.md)
    
- [Каноническое свойство PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)
    
- [Каноническое свойство PidLidEmail2OriginalDisplayName](pidlidemail2originaldisplayname-canonical-property.md)
    
- [Каноническое свойство PidLidEmail2OriginalEntryId](pidlidemail2originalentryid-canonical-property.md)
    
- [Каноническое свойство PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)
    
- [Каноническое свойство PidLidEmail3DisplayName](pidlidemail3displayname-canonical-property.md)
    
- [Каноническое свойство PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)
    
- [Каноническое свойство PidLidEmail3OriginalDisplayName](pidlidemail3originaldisplayname-canonical-property.md)
    
- [Каноническое свойство PidLidEmail3OriginalEntryId](pidlidemail3originalentryid-canonical-property.md)
    
- [Каноническое свойство PidLidEmail1DisplayName](pidlidemail1displayname-canonical-property.md)
    
- [Каноническое свойство PidLidEmail1OriginalDisplayName](pidlidemail1originaldisplayname-canonical-property.md)
    
- [Каноническое свойство PidLidFileUnder](pidlidfileunder-canonical-property.md)
    
- [Каноническое свойство PidLidInstantMessagingAddress](pidlidinstantmessagingaddress-canonical-property.md)
    
- [Каноническое свойство PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)
    
- [Каноническое свойство PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)
    
- [Каноническое свойство PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)
    
- [Каноническое свойство PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [Каноническое свойство PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)
    
- [Каноническое свойство PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)
    
- [Каноническое свойство PidLidYomiCompanyName](pidlidyomicompanyname-canonical-property.md)
    
- [Каноническое свойство PidLidYomiFirstName](pidlidyomifirstname-canonical-property.md)
    
- [Каноническое свойство PidLidYomiLastName](pidlidyomilastname-canonical-property.md)
    
В пространстве имен **PSETID_Appointment** используются следующие именованные свойства: 
  
- [Каноническое свойство PidLidAllAttendeesString](pidlidallattendeesstring-canonical-property.md)
    
- [Каноническое свойство PidLidAppointmentCounterProposal](pidlidappointmentcounterproposal-canonical-property.md)
    
- [Каноническое свойство PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)
    
- [Каноническое свойство PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)
    
- [Каноническое свойство PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)
    
- [Каноническое свойство PidLidBusyStatus](pidlidbusystatus-canonical-property.md)
    
- [Каноническое свойство PidLidCcAttendeesString](pidlidccattendeesstring-canonical-property.md)
    
- [Каноническое свойство PidLidLocation](pidlidlocation-canonical-property.md)
    
- [Каноническое свойство PidLidRecurring](pidlidrecurring-canonical-property.md)
    
- [Каноническое свойство PidLidToAttendeesString](pidlidtoattendeesstring-canonical-property.md)
    
В пространстве имен **PSETID_Common** используются следующие именованные свойства: 
  
- [Каноническое свойство PidLidCommonEnd](pidlidcommonend-canonical-property.md)
    
- [Каноническое свойство PidLidCommonStart](pidlidcommonstart-canonical-property.md)
    
- [Каноническое свойство PidLidCompanies](pidlidcompanies-canonical-property.md)
    
- [Каноническое свойство PidLidContacts](pidlidcontacts-canonical-property.md)
    
- [Каноническое свойство PidLidCustomFlag](pidlidcustomflag-canonical-property.md)
    
- [Каноническое свойство PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Каноническое свойство PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Каноническое свойство PidLidHeaderItem](pidlidheaderitem-canonical-property.md)
    
- [Каноническое свойство PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Каноническое свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)
    
- [Каноническое свойство PidLidReminderSet](pidlidreminderset-canonical-property.md)
    
- [Каноническое свойство PidLidReminderTime](pidlidremindertime-canonical-property.md)
    
- [Каноническое свойство PidLidFlagRequest](pidlidflagrequest-canonical-property.md)
    
- [Каноническое свойство PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
- [Каноническое свойство PidLidSmartNoAttach](pidlidsmartnoattach-canonical-property.md)
    
- [Каноническое свойство PidLidToDoTitle](pidlidtodotitle-canonical-property.md)
    
- [Каноническое свойство PidLidUseTnef](pidlidusetnef-canonical-property.md)
    
В пространстве имен **PSETID_Meeting** используются следующие именованные свойства: 
  
- [Каноническое свойство PidLidMeetingType](pidlidmeetingtype-canonical-property.md)
    
В пространстве имен **PSETID_Task** используются следующие именованные свойства: 
  
- [Каноническое свойство PidLidTaskActualEffort](pidlidtaskactualeffort-canonical-property.md)
    
- [Каноническое свойство PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
    
- [Каноническое свойство PidLidTaskEstimatedEffort](pidlidtaskestimatedeffort-canonical-property.md)
    
- [Каноническое свойство PidLidTaskFRecurring](pidlidtaskfrecurring-canonical-property.md)
    
- [Каноническое свойство PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)
    
- [Каноническое свойство PidLidTaskStatus](pidlidtaskstatus-canonical-property.md)
    
В пространстве имен **PS_INTERNET_HEADERS** используются следующие именованные свойства: 
  
- [Каноническое свойство PidTagInternetReturnPath](pidtaginternetreturnpath-canonical-property.md)
    
В пространстве имен **PSETID_Log** используются следующие именованные свойства: 
  
- [Каноническое свойство PidLidLogDuration](pidlidlogduration-canonical-property.md)
    
- [Каноническое свойство PidLidLogEnd](pidlidlogend-canonical-property.md)
    
- [Каноническое свойство PidLidLogStart](pidlidlogstart-canonical-property.md)
    
- [Каноническое свойство PidLidLogType](pidlidlogtype-canonical-property.md)
    
В пространстве имен **PS_PUBLIC_STRINGS** используются следующие именованные свойства: 
  
- [Каноническое свойство PidNameKeywords](pidnamekeywords-canonical-property.md)
    
- [Каноническое свойство PidNameExchangeJunkEmailMoveStamp](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>См. также



[Константы MAPI](mapi-constants.md)
  
[Определение того, скачан ли в Outlook только заголовок сообщения](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[Получение электронного адреса элемента контакта](how-to-get-the-email-address-of-a-contact-item.md)
  
[Удаление определения настраиваемой формы, сохраненного с сообщением](how-to-remove-custom-form-definition-saved-with-a-message.md)

