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
# <a name="sending-messages-mapi-spooler-tasks"></a>Отправка сообщений: задачи пула MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
��������� ������� MAPI ��������� � �������� �������� ��������� ��� ��������� ��������� �� �������� ����� ��������� � ������� ���������� ���������� ����� ��������� ��������� � ���������� �� ������� ���������� ���������� � ��� ��������� ������� ��������������� ���������.
  
 **��������� ������� MAPI ����� ����� ����������� ��������������� ���������, ���������� ��������� ��������� ��������:**
  
1. If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method. 
    
2. Отправляет сообщение всем получателям, у PR_RESPONSIBILITY  [(PidTagResponsibility)](pidtagresponsibility-canonical-property.md)имеется свойство FALSE. 
    
3. Вызывает соответствующую функцию ([RemovePreprocessInfo)](removepreprocessinfo.md)для очистки любых дополнительных сведений, добавленных в сообщение, для использования во время предварительной очистки, если свойство **PR_PREPROCESS** ([PidTagPreprocess)](pidtagpreprocess-canonical-property.md)было установлено. This function is specified when the transport provider registers its preprocessor function. 
    
4. Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:
    
  - ������������ ���������.
    
  - Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists. Затем сообщение копируется в папку, идентифицируемую идентификатором записи в свойстве **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId),](pidtagsentmailentryid-canonical-property.md)если оно не замещается отправленной обработкой сообщений поставщиком обработчиком сообщений. Наконец, оно удаляет сообщение, если свойству **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)задано true. 
    

