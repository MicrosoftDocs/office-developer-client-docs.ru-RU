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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338691"
---
# <a name="sending-messages-transport-provider-tasks"></a>Отправка сообщений: задачи поставщика транспорта

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **��� �������� ���������, ������������ ����������**
  
- Установите для свойства **пр_респонсибилити** ([PIDTAGRESPONSIBILITY](pidtagresponsibility-canonical-property.md)) сообщения значение true, после того как поставщик транспорта отправил сообщение или попытался отправить сообщение. If an attempt to send a message fails, transport providers should call [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) to generate a nondelivery report. Если сообщение успешно отправлено, а свойство **пр_оригинатор_деливери_репорт_рекуестед** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) имеет значение true, создайте структуру [ADRLIST](adrlist.md) с успешными получателями, Установка свойства **пр_деливер_тиме** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) для каждого из них и вызов **статусреЦипс** для создания отчета о доставке. For more information about creating delivery and non-delivery reports, see the following topics: [��������� ������ MAPI](mapi-report-messages.md), [�������� ��������� ��������� ������](required-report-message-properties.md), [�������� ��������� ������������� ������](optional-report-message-properties.md), and [�������� ������� � �������� ���������](sending-message-delivery-reports.md).
    
- ������ ������ **PR_SENDER** ��������� ������� ������������� ������������, ������� ����� � �������. Эта группа включает: **пр_сендер_ентрид** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)), **Пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md)), **пр_сендер_сеарч_кэй** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)), **пр_сендер_аддртипе** ([ PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) и **пр_сендер_емаил_аддресс** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).
    
- �������� ��������� **PR_SENT_REPRESENTING**, ���� ��� ��������, ������������� ������������, ������� ����� � ������� ��� identity ���������� �������. �������� **PR_SENT_REPRESENTING** ������������ ��� ���������� �������� ��������� � ������ ������������ �� ����� ������� ������������. ���������� ����������, ������� �� ������������ ��� �������� ������� ������������ �� �� ��������� ���������. 
    
- Задайте свойство **пр_клиент_субмит_тиме** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) сообщения, чтобы указать, когда клиент вызывает [iMessage:: субмитмессаже](imessage-submitmessage.md).
    
- Задайте свойство сообщения **пр_провидер_субмит_тиме** ([PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)), чтобы указать дату и время, когда поставщик хранилища сообщений пометил сообщение как отправленное. 
    
����� ��������� ������������ �� ��������� �����������, ��������� ������ ������ �����������, ������ ������������ ����� ����� ����� ������������� ������ �����������. 
  
���������� ���������� ��� ����������� ����� ��������� ��������� � ���������� ����� ����� ��������������� �� ����������� ��������� � �������� ������ ����������. ��������� ������ �������� � ��������� **PR_ORIGINATOR** � �������� ������ �������� � ������� �������� PR_REPLY. ������ ����� ������ ��� ��������; ��� �� ����� ���������� ���������� ����� ������������ � ������������ ��������� �������. 
  

