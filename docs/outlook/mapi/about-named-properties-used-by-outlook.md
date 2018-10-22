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
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="72b32-103">Сведения об именованных свойствах, используемых в Outlook</span><span class="sxs-lookup"><span data-stu-id="72b32-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="72b32-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72b32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72b32-p101">MAPI предоставляет возможность назначения имен определенным свойствам для привязки этих имен к уникальным идентификаторам и сохранения этой карты сопоставления названий и идентификаторов для всех сессий. Именованные свойства определяются по имени и глобальному уникальному идентификатору (GUID) для набора свойств. Имя может представлять собой число или строку. Для Microsoft Outlook 2013 или Microsoft Outlook 2010 набор свойств часто представляет собой пространство имен, определенное Outlook 2013 или Outlook 2010, например, **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="72b32-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="72b32-p102">Именованные свойства управляются с помощью функции [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и функции [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). Имя, а также набор свойств GUID, передаются функции [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения идентификатора свойства, который действует для текущей сессии MAPI. Поскольку этот идентификатор свойства может различаться на разных компьютерах, единственным надежным способом доступа к именованному свойству состоит в получении его имени и набора свойств GUID. Значения идентификаторов всегда находятся в диапазоне от 0x8000 до 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="72b32-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="72b32-p103">Любой объект, который использует интерфейс[IMAPIProp: IUnknown](imapipropiunknown.md), поддерживает именованные свойства. В частности, поставщик услуг MAPI или клиент MAPI обязан использовать [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значений именованных свойств. Конфигурация именованных свойств, которые используются Outlook 2013 или Outlook 2010, не поддерживается из-за риска повреждения данных, которые используются совместно с другими поставщиками услуг или клиентами MAPI.</span><span class="sxs-lookup"><span data-stu-id="72b32-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="72b32-p104">Outlook 2013 и Outlook 2010 используют именованный свойства MAPI для реализации множества своих функций, например, обеспечение безопасности вложений и встречные предложения для встречи. Помимо этих базовых данных Outlook 2013 и Outlook 2010 отображает некоторые из этих свойств в качестве свойств элементов в объектных моделях Outlook 2013 и Outlook 2010. Например, свойство **Email1Address** объекта **ContactItem** в объектной модели соответствует именованному [общепринятому свойству PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) в пространстве имен**PSETID_Address**. Но как правило, из-за проблем обеспечения совместимости и целостности данных многие свойства MAPI, которые используются Outlook 2013 и Outlook 2010, не используются в объектной модели.</span><span class="sxs-lookup"><span data-stu-id="72b32-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="72b32-120">Эта справочная информация описывает количество именованных свойств, указанные в списке ниже.</span><span class="sxs-lookup"><span data-stu-id="72b32-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="72b32-121">В пространстве имен **PSETID_Address** используются следующие именованные свойства:</span><span class="sxs-lookup"><span data-stu-id="72b32-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="72b32-122">Каноническое свойство PidLidEmail1AddressType</span><span class="sxs-lookup"><span data-stu-id="72b32-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="72b32-123">Каноническое свойство PidLidEmail1EmailAddress</span><span class="sxs-lookup"><span data-stu-id="72b32-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="72b32-124">Каноническое свойство PidLidEmail1OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="72b32-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="72b32-125">Каноническое свойство PidLidEmail2AddressType</span><span class="sxs-lookup"><span data-stu-id="72b32-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="72b32-126">Каноническое свойство PidLidEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="72b32-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="72b32-127">Каноническое свойство PidLidEmail2EmailAddress</span><span class="sxs-lookup"><span data-stu-id="72b32-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="72b32-128">Каноническое свойство PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="72b32-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="72b32-129">Каноническое свойство PidLidEmail2OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="72b32-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="72b32-130">Каноническое свойство PidLidEmail3AddressType</span><span class="sxs-lookup"><span data-stu-id="72b32-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="72b32-131">Каноническое свойство PidLidEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="72b32-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="72b32-132">Каноническое свойство PidLidEmail3EmailAddress</span><span class="sxs-lookup"><span data-stu-id="72b32-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="72b32-133">Каноническое свойство PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="72b32-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="72b32-134">Каноническое свойство PidLidEmail3OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="72b32-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="72b32-135">Каноническое свойство PidLidEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="72b32-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="72b32-136">Каноническое свойство PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="72b32-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="72b32-137">Каноническое свойство PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="72b32-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="72b32-138">Каноническое свойство PidLidInstantMessagingAddress</span><span class="sxs-lookup"><span data-stu-id="72b32-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="72b32-139">Каноническое свойство PidLidWorkAddressCity</span><span class="sxs-lookup"><span data-stu-id="72b32-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="72b32-140">Каноническое свойство PidLidWorkAddressCountry</span><span class="sxs-lookup"><span data-stu-id="72b32-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="72b32-141">Каноническое свойство PidLidWorkAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="72b32-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="72b32-142">Каноническое свойство PidLidWorkAddressPostOfficeBox</span><span class="sxs-lookup"><span data-stu-id="72b32-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="72b32-143">Каноническое свойство PidLidWorkAddressState</span><span class="sxs-lookup"><span data-stu-id="72b32-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="72b32-144">Каноническое свойство PidLidWorkAddressStreet</span><span class="sxs-lookup"><span data-stu-id="72b32-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="72b32-145">Каноническое свойство PidLidYomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="72b32-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="72b32-146">Каноническое свойство PidLidYomiFirstName</span><span class="sxs-lookup"><span data-stu-id="72b32-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="72b32-147">Каноническое свойство PidLidYomiLastName</span><span class="sxs-lookup"><span data-stu-id="72b32-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="72b32-148">В пространстве имен **PSETID_Appointment** используются следующие именованные свойства:</span><span class="sxs-lookup"><span data-stu-id="72b32-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="72b32-149">Каноническое свойство PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="72b32-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="72b32-150">Каноническое свойство PidLidAppointmentCounterProposal</span><span class="sxs-lookup"><span data-stu-id="72b32-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="72b32-151">Каноническое свойство PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="72b32-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="72b32-152">Каноническое свойство PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="72b32-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="72b32-153">Каноническое свойство PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="72b32-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="72b32-154">Каноническое свойство PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="72b32-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="72b32-155">Каноническое свойство PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="72b32-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="72b32-156">Каноническое свойство PidLidLocation</span><span class="sxs-lookup"><span data-stu-id="72b32-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="72b32-157">Каноническое свойство PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="72b32-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="72b32-158">Каноническое свойство PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="72b32-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="72b32-159">В пространстве имен **PSETID_Common** используются следующие именованные свойства:</span><span class="sxs-lookup"><span data-stu-id="72b32-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="72b32-160">Каноническое свойство PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="72b32-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="72b32-161">Каноническое свойство PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="72b32-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="72b32-162">Каноническое свойство PidLidCompanies</span><span class="sxs-lookup"><span data-stu-id="72b32-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="72b32-163">Каноническое свойство PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="72b32-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="72b32-164">Каноническое свойство PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="72b32-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="72b32-165">Каноническое свойство PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="72b32-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="72b32-166">Каноническое свойство PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="72b32-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="72b32-167">Каноническое свойство PidLidHeaderItem</span><span class="sxs-lookup"><span data-stu-id="72b32-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="72b32-168">Каноническое свойство PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="72b32-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="72b32-169">Каноническое свойство PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="72b32-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="72b32-170">Каноническое свойство PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="72b32-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="72b32-171">Каноническое свойство PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="72b32-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="72b32-172">Каноническое свойство PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="72b32-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="72b32-173">Каноническое свойство PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="72b32-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="72b32-174">Каноническое свойство PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="72b32-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="72b32-175">Каноническое свойство PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="72b32-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="72b32-176">Каноническое свойство PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="72b32-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="72b32-177">В пространстве имен **PSETID_Meeting** используются следующие именованные свойства:</span><span class="sxs-lookup"><span data-stu-id="72b32-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="72b32-178">Каноническое свойство PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="72b32-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="72b32-179">В пространстве имен **PSETID_Task** используются следующие именованные свойства:</span><span class="sxs-lookup"><span data-stu-id="72b32-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="72b32-180">Каноническое свойство PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="72b32-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="72b32-181">Каноническое свойство PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="72b32-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="72b32-182">Каноническое свойство PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="72b32-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="72b32-183">Каноническое свойство PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="72b32-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="72b32-184">Каноническое свойство PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="72b32-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="72b32-185">Каноническое свойство PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="72b32-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="72b32-186">В пространстве имен **PS_INTERNET_HEADERS** используются следующие именованные свойства:</span><span class="sxs-lookup"><span data-stu-id="72b32-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="72b32-187">Каноническое свойство PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="72b32-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="72b32-188">В пространстве имен **PSETID_Log** используются следующие именованные свойства:</span><span class="sxs-lookup"><span data-stu-id="72b32-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="72b32-189">Каноническое свойство PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="72b32-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="72b32-190">Каноническое свойство PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="72b32-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="72b32-191">Каноническое свойство PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="72b32-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="72b32-192">Каноническое свойство PidLidLogType</span><span class="sxs-lookup"><span data-stu-id="72b32-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="72b32-193">В пространстве имен **PS_PUBLIC_STRINGS** используются следующие именованные свойства:</span><span class="sxs-lookup"><span data-stu-id="72b32-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="72b32-194">Каноническое свойство PidNameKeywords</span><span class="sxs-lookup"><span data-stu-id="72b32-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="72b32-195">Каноническое свойство PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="72b32-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="72b32-196">См. также</span><span class="sxs-lookup"><span data-stu-id="72b32-196">See also</span></span>



[<span data-ttu-id="72b32-197">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="72b32-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="72b32-198">Определение того, скачан ли в Outlook только заголовок сообщения</span><span class="sxs-lookup"><span data-stu-id="72b32-198">Determine if Outlook downloaded only the header of a message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="72b32-199">Получение электронного адреса элемента контакта</span><span class="sxs-lookup"><span data-stu-id="72b32-199">Get the email address of a Contact item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="72b32-200">Удаление определения настраиваемой формы, сохраненного с сообщением</span><span class="sxs-lookup"><span data-stu-id="72b32-200">Remove custom form definition saved with a message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)

