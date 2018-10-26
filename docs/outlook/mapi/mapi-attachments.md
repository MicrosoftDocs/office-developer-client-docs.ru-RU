---
title: �������� MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: fd8075d2fddb7ada6803c869cbbd282c464e75bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585880"
---
# <a name="mapi-attachments"></a>�������� MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
��������� ���������� ��������� ��������� �������������� �������� ��� ����� � ����������� ��������� ���������� � ���� ������, ������� OLE, ��������� ��� �������� ������. ��� �������������� ��������, ���������� �������� ���������. ��� ��� �������� ���������, ������������ � �������� ������ ����� ���� ���������, ��� ��������������� ��������� ���������. ������ ����, ������������� ������ ��� �������, �������� ����� ���������������� �����, ��������� ��� ����� ��������. ��� ����� ���������� ���������� �������� � ���������, �� �� ����������� � ��������� ���������. ��� ������ ��������� ����� ��������� ��������� �������� � ���������� ������� ��������. Номера вложения действительны только, пока сообщение открыто и сохраняются в свойстве **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).
  
��� ������� � ������� ���������� ��� ���� �������� ���������, ������� �������� ��� �������� � �������. � ������� �������� �������� ��������, ������� ������� ����� ������������ ��� ������� � �������� ��������, ����� ��� ���� ����� �������� � ���� ������. ������� ����� ��������� ������� �������� �:
  
- Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
- Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Message store providers are expected to support both of these approaches. Подход **OpenProperty** требуется указать, что вызывающего IID_IMAPITable как идентификатор интерфейса и **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) как тега свойства. **PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table. Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
 ����� ������������ **PR_MESSAGE_ATTACHMENTS**: 
  
- � ������� **IMAPIProp::OpenProperty** ��� ������� � �������� ��� ���������� �������. 
    
- With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- � �������� ����������� ��������� �������, ����� �������, ��� ����������� �������� ������� ��������� � ��������.
    
For more information, see [������� ��������](attachment-tables.md).
  

