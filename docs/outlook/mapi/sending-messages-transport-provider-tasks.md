---
title: �������� ��������� ������ ���������� ����������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd722f48-b166-4670-8dba-897ac50caf37
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 4625d9d09b067d064dac7ca67b7c79ebb818bcce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812251"
---
# <a name="sending-messages-transport-provider-tasks"></a>�������� ���������: ������ ���������� ����������

  
  
**Относится к**: Outlook 
  
 **��� �������� ���������, ������������ ����������**
  
- Свойства сообщения **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) значение TRUE после поставщика транспорта отправившего сообщение или пытался отправить сообщение. If an attempt to send a message fails, transport providers should call [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) to generate a nondelivery report. Если сообщение было успешно отправлено и **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) задано значение TRUE, создайте структуру [ADRLIST](adrlist.md) , содержащую успешные получателей Установка свойства **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) для каждого из них, а также вызвать **StatusRecips** для создания отчетов о доставке. For more information about creating delivery and non-delivery reports, see the following topics: [��������� ������ MAPI](mapi-report-messages.md), [�������� ��������� ��������� ������](required-report-message-properties.md), [�������� ��������� ������������� ������](optional-report-message-properties.md), and [�������� ������� � �������� ���������](sending-message-delivery-reports.md).
    
- ������ ������ **PR_SENDER** ��������� ������� ������������� ������������, ������� ����� � �������. Эта группа включает в себя: **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)), **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)), **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)), **PR_SENDER_ADDRTYPE** ([ PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) и **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).
    
- �������� ��������� **PR_SENT_REPRESENTING**, ���� ��� ��������, ������������� ������������, ������� ����� � ������� ��� identity ���������� �������. �������� **PR_SENT_REPRESENTING** ������������ ��� ���������� �������� ��������� � ������ ������������ �� ����� ������� ������������. ���������� ����������, ������� �� ������������ ��� �������� ������� ������������ �� �� ��������� ���������. 
    
- Необходимо задайте свойство сообщения **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) для указания при вызове [IMessage::SubmitMessage](imessage-submitmessage.md)клиента.
    
- Задайте свойство **PR_PROVIDER_SUBMIT_TIME** ([PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)) сообщение, указывающее дату и время поставщика хранилища сообщений отметил сообщение как был отправлен. 
    
����� ��������� ������������ �� ��������� �����������, ��������� ������ ������ �����������, ������ ������������ ����� ����� ����� ������������� ������ �����������. 
  
���������� ���������� ��� ����������� ����� ��������� ��������� � ���������� ����� ����� ��������������� �� ����������� ��������� � �������� ������ ����������. ��������� ������ �������� � ��������� **PR_ORIGINATOR** � �������� ������ �������� � ������� �������� PR_REPLY. ������ ����� ������ ��� ��������; ��� �� ����� ���������� ���������� ����� ������������ � ������������ ��������� �������. 
  

