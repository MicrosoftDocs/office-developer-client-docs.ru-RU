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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423694"
---
# <a name="mapi-recipients"></a>���������� MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Every message to be transmitted has one or more recipients, or a set of properties that describe where the message is to be delivered. Because recipients are used only in the context of a message, they are considered subobjects of a message instead of separate MAPI objects. Clients and providers work with recipients using the **IMessage** interface. For more information, see [IMessage: IMAPIProp](imessageimapiprop.md).
  
��� ������� �������� � ����������� ��������� ����� ��� ����������� � �������. ������ ��������� ����� ����������� �������, ���������� ������� ���������� � ������ �� ��� �����������. �������, ���������� � ������� ������� �� ��������� ���������. ����� ��������� ��������� � �������� ��������, ���������� ����� ����� ������ ��� ������� � �������:
  
- Отображение имени или **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
- Тип получателя или **PR_RECIPIENT_TYPE** [(PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)
    
- Идентификатор строки или **PR_ROWID** [(PidTagRowid)](pidtagrowid-canonical-property.md)
    
После того как сообщение прошло процесс разрешения имен, у каждого получателя также будет идентификатор записи или столбец **PR_ENTRYID** [(PidTagEntryId).](pidtagentryid-canonical-property.md) � ��� �������� ��������� ������ � ������� ����������� ����� ��������� ��� �������������� �������:
  
- Тип адреса или **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)
    
- Ответственность за транспорт или **PR_RESPONSIBILITY** [(PidTagResponsibility)](pidtagresponsibility-canonical-property.md)
    
Clients can retrieve a message's recipient table by calling its **IMessage::GetRecipientTable** method or its **IMAPIProp::OpenProperty** method. For more information, see [IMessage::GetRecipientTable](imessage-getrecipienttable.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Message store providers are expected to support both of these approaches. The **OpenProperty** approach requires that the client specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_RECIPIENTS** as the property tag. **PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)— это свойство объекта таблицы, представляю которое представляет таблицу получателей сообщения. Message store providers are required to set **PR_MESSAGE_RECIPIENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
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
  

