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
ms.openlocfilehash: 431e3d2f66616db2c586b76387a8521832ed985f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426550"
---
# <a name="sending-messages-transport-provider-tasks"></a>Отправка сообщений: задачи поставщика транспорта

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **��� �������� ���������, ������������ ����������**
  
- Установите свойство **PR_RESPONSIBILITY** [(PidTagResponsibility)](pidtagresponsibility-canonical-property.md)true после того, как поставщик транспорта отправил сообщение или попытался отправить сообщение. If an attempt to send a message fails, transport providers should call [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) to generate a nondelivery report. Если сообщение отправлено успешно **и свойство PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** [(PidTagOriginatorDeliveryReportReportRequested)](pidtagoriginatordeliveryreportrequested-canonical-property.md)настроено на TRUE, создайте структуру [ADRLIST,](adrlist.md) содержащую успешных получателей, **задайте** свойство PR_DELIVER_TIME [(PidTagDeliverTime)](pidtagdelivertime-canonical-property.md)для каждого, и позвоните **StatusRecips** для создания отчета о доставке. For more information about creating delivery and non-delivery reports, see the following topics: [��������� ������ MAPI](mapi-report-messages.md), [�������� ��������� ��������� ������](required-report-message-properties.md), [�������� ��������� ������������� ������](optional-report-message-properties.md), and [�������� ������� � �������� ���������](sending-message-delivery-reports.md).
    
- ������ ������ **PR_SENDER** ��������� ������� ������������� ������������, ������� ����� � �������. В эту группу входят: **PR_SENDER_ENTRYID** [(PidTagSenderEntryId),](pidtagsenderentryid-canonical-property.md) **PR_SENDER_NAME** [(PidTagSenderName),](pidtagsendername-canonical-property.md) **PR_SENDER_SEARCH_KEY** [(PidTagSenderSearchKey),](pidtagsendersearchkey-canonical-property.md) **PR_SENDER_ADDRTYPE** [(PidTagSenderAddressType)](pidtagsenderaddresstype-canonical-property.md)и **PR_SENDER_EMAIL_ADDRESS** [(PidTagSenderEmailAddress).](pidtagsenderemailaddress-canonical-property.md)
    
- �������� ��������� **PR_SENT_REPRESENTING**, ���� ��� ��������, ������������� ������������, ������� ����� � ������� ��� identity ���������� �������. �������� **PR_SENT_REPRESENTING** ������������ ��� ���������� �������� ��������� � ������ ������������ �� ����� ������� ������������. ���������� ����������, ������� �� ������������ ��� �������� ������� ������������ �� �� ��������� ���������. 
    
- Установите свойство PR_CLIENT_SUBMIT_TIME  [(PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)для указать, когда клиент называется [IMessage::SubmitMessage](imessage-submitmessage.md).
    
- Установите свойство **PR_PROVIDER_SUBMIT_TIME** [(PidTagProviderSubmitTime),](pidtagprovidersubmittime-canonical-property.md)чтобы указать дату и время, когда поставщик хранения сообщений указал сообщение как отправленное. 
    
����� ��������� ������������ �� ��������� �����������, ��������� ������ ������ �����������, ������ ������������ ����� ����� ����� ������������� ������ �����������. 
  
���������� ���������� ��� ����������� ����� ��������� ��������� � ���������� ����� ����� ��������������� �� ����������� ��������� � �������� ������ ����������. ��������� ������ �������� � ��������� **PR_ORIGINATOR** � �������� ������ �������� � ������� �������� PR_REPLY. ������ ����� ������ ��� ��������; ��� �� ����� ���������� ���������� ����� ������������ � ������������ ��������� �������. 
  

