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
ms.openlocfilehash: eef65990637d9c164ffe75f682e01ed134510e32
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570277"
---
# <a name="sending-messages-mapi-spooler-tasks"></a>�������� ���������: ������ ������� MAPI

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
��������� ������� MAPI ��������� � �������� �������� ��������� ��� ��������� ��������� �� �������� ����� ��������� � ������� ���������� ���������� ����� ��������� ��������� � ���������� �� ������� ���������� ���������� � ��� ��������� ������� ��������������� ���������.
  
 **��������� ������� MAPI ����� ����� ����������� ��������������� ���������, ���������� ��������� ��������� ��������:**
  
1. If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method. 
    
2. Имеет поставщика транспорта отправки сообщения для всех получателей, которые их **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) свойство должно быть указано значение FALSE. 
    
3. Очистка любые дополнительные сведения, который был добавлен к сообщению для использования во время предварительной обработки, если свойство **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) вызывает соответствующую функцию ([RemovePreprocessInfo](removepreprocessinfo.md)). This function is specified when the transport provider registers its preprocessor function. 
    
4. Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:
    
  - ������������ ���������.
    
  - Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists. Затем копирует сообщение в папку, указанную с идентификатором запись в свойство **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), если не замещена обмена сообщениями поставщика обработчик отправленные обработки сообщений. И, наконец удаляет сообщение, если свойство **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) значение TRUE. 
    

