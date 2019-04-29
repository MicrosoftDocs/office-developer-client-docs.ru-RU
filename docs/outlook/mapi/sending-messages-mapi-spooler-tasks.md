---
title: �������� ��������� ������ ������� MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 8a6730cca5c75a888afb5ff0a44f1e2a0a6465e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420201"
---
# <a name="sending-messages-mapi-spooler-tasks"></a>Отправка сообщений: задачи системы буферизации MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
��������� ������� MAPI ��������� � �������� �������� ��������� ��� ��������� ��������� �� �������� ����� ��������� � ������� ���������� ���������� ����� ��������� ��������� � ���������� �� ������� ���������� ���������� � ��� ��������� ������� ��������������� ���������.
  
 **��������� ������� MAPI ����� ����� ����������� ��������������� ���������, ���������� ��������� ��������� ��������:**
  
1. If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method. 
    
2. Поставщик транспорта отправляет сообщение всем получателям, у которых для свойства **пр_респонсибилити** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) задано значение false. 
    
3. Вызывает соответствующую функцию ([ремовепрепроцессинфо](removepreprocessinfo.md)), чтобы очистить дополнительные сведения, добавленные к сообщению для использования во время предварительной обработки, если было задано свойство **пр_препроцесс** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)). This function is specified when the transport provider registers its preprocessor function. 
    
4. Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:
    
  - ������������ ���������.
    
  - Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists. После этого сообщение копируется в папку, указанную идентификатором записи, в свойстве **пр_сентмаил_ентрид** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), если она не была заменена с помощью отправленной обработки сообщений поставщика обработчиков обмена сообщениями. Наконец, он удаляет сообщение, если для свойства **пр_делете_афтер_субмит** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) задано значение true. 
    

