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
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="a2e11-103">�� ����������� �������, ������������ � Outlook</span><span class="sxs-lookup"><span data-stu-id="a2e11-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="a2e11-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2e11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2e11-p101">MAPI ������������� �������� ��� ���������� ���� ��� ������������ ������� ��� ������������� ���� ���� � ����������� ���������������� � ������������ ����-� ������������� ����� ������������� ������������ ����� ��������. ����������� �������� ���������������� �� ����� � ���������� ���������� ������������� (GUID) ��� ������ �������. ��� ����� ������� ����� ��� ������. ��� Microsoft Outlook 2013 ��� Microsoft Outlook 2010 ����� ������� ���� ����� ������������ ����, ������������ � Outlook�2013 ��� Outlook�2010, ����� ��� **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="a2e11-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="a2e11-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span><span class="sxs-lookup"><span data-stu-id="a2e11-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="a2e11-p103">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook�2013 or Outlook�2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span><span class="sxs-lookup"><span data-stu-id="a2e11-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="a2e11-p104">Outlook�2013 and Outlook�2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook�2013 and Outlook�2010 expose some of these properties as item properties in their Outlook�2013 and Outlook�2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [������������ �������� PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook�2013 and Outlook�2010 are not exposed in the object model.</span><span class="sxs-lookup"><span data-stu-id="a2e11-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="a2e11-120">� ���� ������� ������� ���������� ����������� �������, ������� ����������� ����.</span><span class="sxs-lookup"><span data-stu-id="a2e11-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="a2e11-121">���� ������������ ����������� ������� � ������������ ���� **PSETID_Address**.</span><span class="sxs-lookup"><span data-stu-id="a2e11-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="a2e11-122">������������ �������� PidLidEmail1AddressType</span><span class="sxs-lookup"><span data-stu-id="a2e11-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="a2e11-123">������������ �������� PidLidEmail1EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a2e11-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="a2e11-124">������������ �������� PidLidEmail1OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="a2e11-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="a2e11-125">������������ �������� PidLidEmail2AddressType</span><span class="sxs-lookup"><span data-stu-id="a2e11-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="a2e11-126">������������ �������� PidLidEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="a2e11-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="a2e11-127">������������ �������� PidLidEmail2EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a2e11-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="a2e11-128">������������ �������� PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="a2e11-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="a2e11-129">������������ �������� PidLidEmail2OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="a2e11-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="a2e11-130">������������ �������� PidLidEmail3AddressType</span><span class="sxs-lookup"><span data-stu-id="a2e11-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="a2e11-131">������������ �������� PidLidEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="a2e11-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="a2e11-132">������������ �������� PidLidEmail3EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a2e11-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="a2e11-133">������������ �������� PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="a2e11-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="a2e11-134">������������ �������� PidLidEmail3OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="a2e11-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="a2e11-135">������������ �������� PidLidEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="a2e11-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="a2e11-136">������������ �������� PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="a2e11-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="a2e11-137">������������ �������� PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="a2e11-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="a2e11-138">������������ �������� PidLidInstantMessagingAddress</span><span class="sxs-lookup"><span data-stu-id="a2e11-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="a2e11-139">������������ �������� PidLidWorkAddressCity</span><span class="sxs-lookup"><span data-stu-id="a2e11-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="a2e11-140">������������ �������� PidLidWorkAddressCountry</span><span class="sxs-lookup"><span data-stu-id="a2e11-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="a2e11-141">������������ �������� PidLidWorkAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="a2e11-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="a2e11-142">������������ �������� PidLidWorkAddressPostOfficeBox</span><span class="sxs-lookup"><span data-stu-id="a2e11-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="a2e11-143">������������ �������� PidLidWorkAddressState</span><span class="sxs-lookup"><span data-stu-id="a2e11-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="a2e11-144">������������ �������� PidLidWorkAddressStreet</span><span class="sxs-lookup"><span data-stu-id="a2e11-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="a2e11-145">������������ �������� PidLidYomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="a2e11-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="a2e11-146">������������ �������� PidLidYomiFirstName</span><span class="sxs-lookup"><span data-stu-id="a2e11-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="a2e11-147">������������ �������� PidLidYomiLastName</span><span class="sxs-lookup"><span data-stu-id="a2e11-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="a2e11-148">���� ������������ ����������� ������� � ������������ ���� **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="a2e11-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="a2e11-149">������������ �������� PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="a2e11-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="a2e11-150">������������ �������� PidLidAppointmentCounterProposal</span><span class="sxs-lookup"><span data-stu-id="a2e11-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="a2e11-151">������������ �������� PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="a2e11-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="a2e11-152">������������ �������� PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="a2e11-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="a2e11-153">������������ �������� PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="a2e11-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="a2e11-154">������������ �������� PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="a2e11-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="a2e11-155">������������ �������� PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="a2e11-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="a2e11-156">������������ �������� PidLidLocation</span><span class="sxs-lookup"><span data-stu-id="a2e11-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="a2e11-157">������������ �������� PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="a2e11-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="a2e11-158">������������ �������� PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="a2e11-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="a2e11-159">���� ������������ ����������� ������� � ������������ ���� **PSETID_Common**.</span><span class="sxs-lookup"><span data-stu-id="a2e11-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="a2e11-160">������������ �������� PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="a2e11-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="a2e11-161">������������ �������� PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="a2e11-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="a2e11-162">������������ �������� PidLidCompanies</span><span class="sxs-lookup"><span data-stu-id="a2e11-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="a2e11-163">������������ �������� PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="a2e11-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="a2e11-164">������������ �������� PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="a2e11-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="a2e11-165">������������ �������� PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="a2e11-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="a2e11-166">������������ �������� PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="a2e11-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="a2e11-167">������������ �������� PidLidHeaderItem</span><span class="sxs-lookup"><span data-stu-id="a2e11-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="a2e11-168">������������ �������� PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="a2e11-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="a2e11-169">������������ �������� PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="a2e11-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="a2e11-170">������������ �������� PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="a2e11-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="a2e11-171">������������ �������� PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="a2e11-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="a2e11-172">������������ �������� PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="a2e11-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="a2e11-173">������������ �������� PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="a2e11-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="a2e11-174">������������ �������� PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="a2e11-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="a2e11-175">������������ �������� PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="a2e11-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="a2e11-176">������������ �������� PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="a2e11-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="a2e11-177">���� ������������ ����������� ������� � ������������ ���� **PSETID_Meeting**.</span><span class="sxs-lookup"><span data-stu-id="a2e11-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="a2e11-178">������������ �������� PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="a2e11-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="a2e11-179">���� ������������ ����������� ������� � ������������ ���� **PSETID_Task**.</span><span class="sxs-lookup"><span data-stu-id="a2e11-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="a2e11-180">������������ �������� PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="a2e11-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="a2e11-181">������������ �������� PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="a2e11-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="a2e11-182">������������ �������� PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="a2e11-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="a2e11-183">������������ �������� PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="a2e11-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="a2e11-184">������������ �������� PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="a2e11-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="a2e11-185">������������ �������� PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="a2e11-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="a2e11-186">���� ������������ ����������� ������� � ������������ ���� **PS_INTERNET_HEADERS**.</span><span class="sxs-lookup"><span data-stu-id="a2e11-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="a2e11-187">������������ �������� PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="a2e11-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="a2e11-188">���� ������������ ����������� ������� � ������������ ���� **PSETID_Log**.</span><span class="sxs-lookup"><span data-stu-id="a2e11-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="a2e11-189">������������ �������� PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="a2e11-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="a2e11-190">������������ �������� PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="a2e11-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="a2e11-191">������������ �������� PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="a2e11-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="a2e11-192">������������ �������� PidLidLogType</span><span class="sxs-lookup"><span data-stu-id="a2e11-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="a2e11-193">���� ������������ ����������� ������� � ������������ ���� **PS_PUBLIC_STRINGS**.</span><span class="sxs-lookup"><span data-stu-id="a2e11-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="a2e11-194">������������ �������� PidNameKeywords</span><span class="sxs-lookup"><span data-stu-id="a2e11-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="a2e11-195">������������ �������� PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="a2e11-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="a2e11-196">��. �����</span><span class="sxs-lookup"><span data-stu-id="a2e11-196">See also</span></span>



[<span data-ttu-id="a2e11-197">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="a2e11-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a2e11-198">Определение того, скачан ли в Outlook только заголовок сообщения</span><span class="sxs-lookup"><span data-stu-id="a2e11-198">Determine if Outlook Downloaded Only the Header of a Message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="a2e11-199">Получение электронного адреса элемента контакта</span><span class="sxs-lookup"><span data-stu-id="a2e11-199">Get the Email Address of a Contact Item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="a2e11-200">Удаление определения настраиваемой формы, сохраненного с сообщением</span><span class="sxs-lookup"><span data-stu-id="a2e11-200">Remove Custom Form Definition Saved With a Message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)

