---
title: �������� ��������� ������ ���������� ��������� ���������
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: acbfd3ae-bfdc-4103-bed2-6bcf7b9c448c
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 8bfa5709dede4a9501d261e0f495acbc0894b470
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812250"
---
# <a name="sending-messages-message-store-provider-tasks"></a>�������� ���������: ������ ���������� ��������� ���������

**Относится к**: Outlook 
  
A message store provider gets involved with the message sending process when a client calls the message's [IMessage::SubmitMessage](imessage-submitmessage.md) method. If multiple messages are to be sent, the message store must send them in the same order that the client used for its **SubmitMessage** calls. 
  
��������� ��������� ��������� ���������� �� �������� ��������� ������� MAPI. ���� ��������� �������� ��������� �� �������� ����� ���������, ��������� ������� ��������������� ���������, ��� ����� ��������� ��������� � ���������� �� ������� ���������� ���� �����������, ��������� ������� MAPI ������ ��������� �������. 
  
��������� ��������� ��������� ������, ������� ���������� ���������� ��������� ��������� ��� �������� ���������. 
  
**В IMessage::SubmitMessage поставщик хранилища сообщения**.
  
1. Если сообщение имеет флаг MSGFLAG_RESEND в своем свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) и возвращает все ошибки в клиент вызывает [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) . **PrepareSubmit** проверяет свойство **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) каждого получателя в список получателей сообщения.
    
   - Если значение флага MAPI_SUBMITTED, указывающего на то, что получатель не получил исходное сообщение **PrepareSubmit** сбрасывает и устанавливает для свойства **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) значение TRUE. 
    
   - ���� ���� MAPI_SUBMITTED �� ����������, ������������ �� ��, ��� ���������� ��� ������� �������� ��������� **PrepareSubmit** �������� �������� **PR_RECIPIENT_TYPE** MAPI_P1 � ������������� ��� �������� **PR_RESPONSIBILITY** �������� TRUE � ���������� �� ������, ��������� �������� **PrepareSubmit** �������. 
    
2. ������ ���� MSGFLAG_SUBMIT � �������� **PR_MESSAGE_FLAGS** ���������. 
    
3. ������ �� ���, ��� ������� ��� **PR_RESPONSIBILITY** � ������� ����������� � ������ �������� FALSE, ����� �������, ��� ��� ���������� ��� �������������� ��������������� ��� �������� ���������. 
    
4. Задает дату и время возникновения в свойстве **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Calls [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) to: 
    
   - ���������� ��� ������ �������� � ����������� � �������� ��� ���������� ������������ ����� � ��������� �������.
   - �������� ������������� ����.
   - Проверьте наличие любые необходимые предварительной обработки и если требуется предварительной обработки, задайте флаг NEEDS_PREPROCESSING и свойство **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), свойство зарезервировано для MAPI. 
   - ���������� ����� NEEDS_SPOOLER ��������� ��������� ����� ������� � ���������� � �� ����� ���������� ���� �����������. 
    
6. ���� ���������� ���� ��������� NEEDS_PREPROCESSING ��������� ��������� ������:
    
   - Размещение сообщения в очереди исходящих сообщений с SUBMITFLAG_PREPROCESS бит в свойстве **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)).
   - ���������� ��������� ������� MAPI, ������� ��� ������� �������.
   - ��������� ���������� ������� � ����� ��������� ��-�������� ������������ � ��������� ������� MAPI. 
   - ��������� ������� MAPI ��������� ��������� ������:
     - Блокирует сообщения путем вызова IMsgStore::SetLockState. 
     - Выполняет необходимые предварительной обработки, вызвав все функции предварительной обработки в порядке регистрации. Поставщики транспорта вызов IMAPISupport::RegisterPreprocessor для регистрации функции предварительной обработки. 
     - Вызывает IMessage::SubmitMessage открыть сообщение как магазин сообщение о завершении предварительной обработки.

<br/>

Если не было без предварительной обработки, а когда диспетчер очереди MAPI вызывает **SubmitMessage** , если был предварительной в процессе клиента выполняются следующие два действия. 

**Поставщик хранилища сообщения**.

1. Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - ������������ �����������, ������� ����� ������������.
   - ������������� ��� �������� **PR_RESPONSIBILITY** �������� TRUE ��� �����������, ������� �� ������������. 
   - ���� ��� ���������� ��������, ��� ���� ����� ��������� ��������� � ����������, ��������� ��������� ������:
     - Если предварительно сообщение или сообщение хранения нужна поставщика диспетчер очереди MAPI для завершения обработки сообщений, рекомендуется, чтобы системы обмена сообщениями, что обработчики могут быть вызваны вызывает IMAPISupport::CompleteMsg. Поток сообщений продолжает с очередью MAPI, как описано в следующей процедуре.  
     - Если без предварительной обработки сообщения или поставщика хранилища сообщений не нужно, чтобы диспетчер очереди MAPI для завершения обработки сообщений выполняет следующие задачи:
       - Копии сообщения в папку, определяемую средством идентификатор записи в свойстве PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId), если необходимо задать.
       - Удаляет сообщение, если свойство PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit) значение TRUE.
       - Разблокирует сообщение, если она заблокирована.
       - Возвращает клиенту. Поток сообщений завершена. 
   
2. ���� ��������� ��������� �� ����� ���������� ��� ����������, �� ���� ����������� ��������, ��� ��������� ��������� ��� ���� NEEDS_SPOOLER ��������� ��������� ������:
    
   - ��������� ���������� � ������� ��������� ��� ��������� ���� SUBMITFLAG_PREPROCESS � �������� **PR_SUBMIT_FLAGS**. 
   - ���������� ��������� ������� MAPI, ��������� ������� ��� �������, ������ ����������� � �������. 
   - ���������� ������� � ����� ��������� ��-�������� ������������ � ������� ������, ����������� ����������� ������� MAPI.
    
���� ��������� �� ����� �������������� ��������� ������� MAPI, ��������� �������� ��������� ������������� �������� �������� **PR_SUBMIT_FLAGS** ��������� SUBMITFLAG_LOCKED. ���� SUBMITFLAG_LOCKED ���������, ��� ��������� ������� MAPI ������������ ��������� ��� ������������� ��� �������������. ������ ��� **PR_SUBMIT_FLAGS,** SUBMITFLAG_PREPROCESS, ����� �������� ��� ��������� ������� ��������������� ��������� ������ ��� ���������� ������������� ���������, ������������������, ���������� ����������. 
  

