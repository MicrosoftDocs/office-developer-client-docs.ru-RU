---
title: ����������� ����� MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2aa2376-b293-4d05-9104-218cc1fe1758
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: fa221510a5f6a8c8be24b4869960d1770cef5882
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410926"
---
# <a name="mapi-special-folders"></a>����������� ����� MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI ���������� ��������� �����, ������� �������� �������, ��������� ��� ����� �������������� �������������� ������������ ���� � �������� ����� �� ��������� ��� ������������ ����� ���������. ��������� ����������� ����� ������ �� ����� ���� ������, � � ��� ����������� ������ �������������� ��������.
  
���������� ������ ����������� �����, ���������, ������� �������� ������ ��������� ����������� ����� � ��� ��������� (IPM). MAPI ������� ���� �����, ������ ��� ������ �������� ������ � ��������� ���������, ����� ���� �������, ����� ������� �����, ��� �������������. ��������� ���������� ��������� ��������� ��������� ��������, � ��������� � ���. � ��������� ������� ����������� ��� �����.
  
**����� MAPI**

|**�����**|**��������**|
|:-----|:-----|
|����� ����������  <br/> |�������� ��������� ��������� IPM.  <br/> |
|����� "���������"  <br/> |�������� IPM ���������, ���������� ��� ��������.  <br/> |
|����� �������������  <br/> |�������� IPM ���������, ������� ���� ����������.  <br/> |
|IPM �������� �����  <br/> |�������� ����� ��� ������ � ����������� IPM.  <br/> |
|��������� �����  <br/> |�������� �������� ��������� ��� ������������� ��������� ������.  <br/> |
|�������� ����� ����������� ������  <br/> |�������� ����� ��� ���������� ����������� ������.  <br/> |
|����� ������������� �������� �����  <br/> |�������� ����� ��� ���������� ������������� ��� ��������� ���������.  <br/> |
|�������� ����� ������ �������������  <br/> |�������� ����� ��� ���������� ������������� ��� ������������� ������������.  <br/> |
   
The first four folders relate to the IPM subtree, a tree of folders that MAPI creates when a message store is initialized. Default message stores for interactive messaging clients always include the IPM folder subtree and the other special folders in their folder hierarchy. Non-default message stores are required only to support the search-results root folder, the IPM subtree root folder, the Deleted Items folder, and the receive folder. To ensure that the IPM subtree folders exist and are valid, clients can call the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function. **HrValidateIPMSubtree** checks the folders and recreates them if there is a problem. 
  
�������� ����� ��� ����������� ������, ����� ������������� � ������� ���������������, �� ���������� ������ ��������� IPM; ��� ����� ��������� � �������� ����� ��� �������� ���������. ���������� ������ �������� �����, ������� ������������ ���������� ������� � ���������, ��������������� ��������� ������ ��������� ������. �������� �� ��, ��� ������� ����� ��������� ���������� ������ ����� � ����� �����, ����������� �������� ��������� � ����� �������� ����� ���� ��������� ���� ����������� ������ �����, ��������� �� ����� ������. 
  
�������� ����� ������ ������������� � ������ ������������� �������� ���������, ������� ��������� ������������� ��� �������������� �������� ����������� ������ ��������� � �����. � �������� ����� ������ ������������� �������� �������������, � ������� ������� ����� ������������ ����� ����� � ��������� ���������; ����� ������ ������������� �������� �������������, ������� ���� ���������� ���������� ������������ ��� ���������� ����� ��� �����.
  
�������, ������� �������� � IPM ��������� ������� ������� ��� ����� � ��������� � �������� ����� ��������� IPM, � �� � �������� ����� ��������� ���������. ��� ���� ������� �� IPM � ��������, ���������� � ���������, ������������ � ����� ������������ ��� ����� ������ � ����������� � ������� ������ ������ �� ��������� �� �������� IPM. 
  
MAPI assigns special entry identifier properties for these special folders. For a list of the special folder entry identifiers, see [�������� ����� ��������� ���������](opening-a-message-store-folder.md).
  
### <a name="outlook-special-folders"></a>����������� ����� Outlook

����������� ����� Outlook ���������������� �� �� ������ ��������������, ������� �������� � ����� "��������" � �������� ����� ��� �������� ���������.
  
|**Folder**|**�������� ��� �������**|
|:-----|:-----|
|���������  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** [(PidTagIpmAppointmentEntryId)](pidtagipmappointmententryid-canonical-property.md)  <br/> |
|Контакты  <br/> |**PR_IPM_CONTACT_ENTRYID** [(PidTagIpmContactEntryId)](pidtagipmcontactentryid-canonical-property.md)  <br/> |
|Журнал  <br/> |**PR_IPM_JOURNAL_ENTRYID** [(PidTagIpmJournalEntryId)](pidtagipmjournalentryid-canonical-property.md)  <br/> |
|Примечания  <br/> |**PR_IPM_NOTE_ENTRYID** [(PidTagIpmNoteEntryId)](pidtagipmnoteentryid-canonical-property.md)  <br/> |
|Задачи  <br/> |**PR_IPM_TASK_ENTRYID** [(PidTagIpmTaskEntryId)](pidtagipmtaskentryid-canonical-property.md)  <br/> |
|Черновики  <br/> |**PR_IPM_DRAFTS_ENTRYID** [(PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>См. также



[����� MAPI](mapi-folders.md)

