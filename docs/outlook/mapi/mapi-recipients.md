---
title: ���������� MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 88a4360d-6ab8-466e-8ebd-af80227ee00a
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: ebdaf47b4f20763574ffac73bddeb3eb4eeb95df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328219"
---
# <a name="mapi-recipients"></a>���������� MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Every message to be transmitted has one or more recipients, or a set of properties that describe where the message is to be delivered. Because recipients are used only in the context of a message, they are considered subobjects of a message instead of separate MAPI objects. Clients and providers work with recipients using the **IMessage** interface. For more information, see [IMessage: IMAPIProp](imessageimapiprop.md).
  
��� ������� �������� � ����������� ��������� ����� ��� ����������� � �������. ������ ��������� ����� ����������� �������, ���������� ������� ���������� � ������ �� ��� �����������. �������, ���������� � ������� ������� �� ��������� ���������. ����� ��������� ��������� � �������� ��������, ���������� ����� ����� ������ ��� ������� � �������:
  
- Отображаемое имя или **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- Тип получателя или **пр_реЦипиент_типе** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- Идентификатор строки или **пр_ровид** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
После того как сообщение будет переработано в процессе разрешения имен, у каждого получателя также будет идентификатор записи или столбец **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)). � ��� �������� ��������� ������ � ������� ����������� ����� ��������� ��� �������������� �������:
  
- Тип адреса или **пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- Ответственность за транспортировку или **пр_респонсибилити** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Clients can retrieve a message's recipient table by calling its **IMessage::GetRecipientTable** method or its **IMAPIProp::OpenProperty** method. For more information, see [IMessage::GetRecipientTable](imessage-getrecipienttable.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Message store providers are expected to support both of these approaches. The **OpenProperty** approach requires that the client specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_RECIPIENTS** as the property tag. **Пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) — это свойство объекта Table, представляющее таблицу получателей сообщения. Message store providers are required to set **PR_MESSAGE_RECIPIENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
For more information about how to work with a recipient table, see [����������� ������](recipient-tables.md).
  
� ���������� � ������������ ��� ������� � ������� �����������, ����� ������������ **PR_MESSAGE_RECIPIENTS**: 
  
- With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include recipients when copying. For more information see, [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- � �������� ����������� ��������� �������, ����� �������, ��� ���������� �������� ������� ��������� � �����������.
    
������� ����� �������� ����������� �� ���������, ���������� ������� �� �������� ����� MAPI ��� ����� �������� ����� �������. ��� ����� ������, ���������� one-offs, ����� ������������ �������� ��� ������������ ����������� � ���������� ����� ��������. � �� ����� ��� �����������, ������� ������� �� �������� ����� � �������������� �������, ��������� � �� � �������� �����, ����������� ���������� ����� �������������� �������, ����������������� � MAPI. ��� �������� ���������� � �������������� �������� ��������� ������� �������� � ������� ��������� ����� �������. 
  
���������� ���������� ������ **IMAPISupport::CreateOneOff** ��� �������� �������������� ��������� ������� ��� ������ �� ���������� ���������: 
  
- ����� ��������� � �����.
    
- ����� �� ����� ���������� � ���������� �������� ���� �������� �������.
    
For more information, see [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
������� �������� **IAddrBook::CreateOneOff** ��� �������� �������������� ��������� ������� ��� ������ �� ��������� ���������, �����: 
  
- ����� ������������� ��� ��������� �����.
    
- ����� ������������� ��� ����� � ���������.
    
For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).
  
For more information about one-off entry identifiers and addresses, see [�������������� ��������� �������](one-off-entry-identifiers.md) and [����������� ������](one-off-addresses.md).
  
�������� ���������� � ��� ��������� ������� �������� ����� � �������� ����������� � �����������. ��� ���������� ��������� ��������� ������� �����, ����������� � ������������ �������� �����. ����� ������ ������������ � �������� ���������� ��� ��������� ���������, �������� ������� ����� ���������� � **ADRLIST** ���������, � ������� ���������� �������� ��� ���� ����������� ���������. 
  
��� ��������, �������� ���������� ��� �����������, **PR_RECIPIENT_TYPE** � **PR_RESPONSIBILITY**. **PR_RECIPIENT_TYPE** ���������, �������� �� ���������� ���������, ������� �����, ������� ����� ��� ��������� ����������. ������ ��� ���� ����������� ����������� ��� ���������, ������������ � ������ ���. 
  
���� ���������� �� �������� ��������� � ������� ��������� ��� ��� ���, ���������� ����������, � ��� ��� ������ �������� MAPI_P1 ��� ��������, ��� ���������� ���������. ���� ������ ��������� �� ����������� ��������� �� ������, �� �������� **PR_RECIPIENT_TYPE** ���������� � ����������� ���� MAPI_SUBMITTED ��� ��������� �������� ���������. �������� ��������� ������������ ����������� ��� �����������, �������� �� **PR_RECIPIENT_TYPE** �������� MAPI_TO. ��� ��������� ���� �������� ���������������. 
  
 **PR_RESPONSIBILITY** � ��� ��������, ����������� ��� ���������� ���������� �� �� ������ ������������ �������� ����������. ����� �������� ��������� ��������� ���� ����������� ���������� **PR_RESPONSIBILITY** �������� FALSE. ��� ���������� ���������� �� ������ ����������� ��������������� �� �������� � ������ ��� ���������� �����������, �� **PR_RESPONSIBILITY** ������ �������� TRUE. 
  

