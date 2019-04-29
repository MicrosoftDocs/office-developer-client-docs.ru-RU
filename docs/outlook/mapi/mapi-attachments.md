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
ms.openlocfilehash: 90fbec8b61499f383228823d69b041a21199a22e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417835"
---
# <a name="mapi-attachments"></a>�������� MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
��������� ���������� ��������� ��������� �������������� �������� ��� ����� � ����������� ��������� ���������� � ���� ������, ������� OLE, ��������� ��� �������� ������. ��� �������������� ��������, ���������� �������� ���������. ��� ��� �������� ���������, ������������ � �������� ������ ����� ���� ���������, ��� ��������������� ��������� ���������. ������ ����, ������������� ������ ��� �������, �������� ����� ���������������� �����, ��������� ��� ����� ��������. ��� ����� ���������� ���������� �������� � ���������, �� �� ����������� � ��������� ���������. ��� ������ ��������� ����� ��������� ��������� �������� � ���������� ������� ��������. Номера вложений допустимы только в том случае, если оно открыто и хранится в свойстве **пр_аттач_нум** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).
  
��� ������� � ������� ���������� ��� ���� �������� ���������, ������� �������� ��� �������� � �������. � ������� �������� �������� ��������, ������� ������� ����� ������������ ��� ������� � �������� ��������, ����� ��� ���� ����� �������� � ���� ������. ������� ����� ��������� ������� �������� �:
  
- Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
- Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Message store providers are expected to support both of these approaches. Для подхода **опенпроперти** требуется, чтобы вызывающий оператор указал иид_имапитабле в качестве идентификатора интерфейса и **пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) в качестве тега свойства. **PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table. Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
 ����� ������������ **PR_MESSAGE_ATTACHMENTS**: 
  
- � ������� **IMAPIProp::OpenProperty** ��� ������� � �������� ��� ���������� �������. 
    
- With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- � �������� ����������� ��������� �������, ����� �������, ��� ����������� �������� ������� ��������� � ��������.
    
For more information, see [������� ��������](attachment-tables.md).
  

