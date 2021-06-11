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
ms.openlocfilehash: de29707c7a257ea0e7ad658622d2a3054487f8b5
ms.sourcegitcommit: adcf409d56b6cb25be6117f09794defa41ad6c0f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2019
ms.locfileid: "37495308"
---
# <a name="sending-messages-message-store-provider-tasks"></a>Отправка сообщений: задачи поставщика магазина сообщений

**Область применения**: Outlook 2013 | Outlook 2016 
  
A message store provider gets involved with the message sending process when a client calls the message's [IMessage::SubmitMessage](imessage-submitmessage.md) method. If multiple messages are to be sent, the message store must send them in the same order that the client used for its **SubmitMessage** calls. 
  
��������� ��������� ��������� ���������� �� �������� ��������� ������� MAPI. ���� ��������� �������� ��������� �� �������� ����� ���������, ��������� ������� ��������������� ���������, ��� ����� ��������� ��������� � ���������� �� ������� ���������� ���� �����������, ��������� ������� MAPI ������ ��������� �������. 
  
��������� ��������� ��������� ������, ������� ���������� ���������� ��������� ��������� ��� �������� ���������. 
  
**В IMessage::SubmitMessage поставщик магазина сообщений:**
  
1. Вызывает [IMAPISupport::P repareSubmit,](imapisupport-preparesubmit.md) если в сообщении установлен флаг MSGFLAG_RESEND в свойстве **PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)и возвращается клиенту все ошибки. **PrepareSubmit** **проверяет свойство PR_RECIPIENT_TYPE** [(PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)каждого получателя в списке получателей сообщения.
    
   - Если флаг MAPI_SUBMITTED, указывающий, что получатель не получил исходное сообщение, **PrepareSubmit** очищает флаг и задает свойство [PR_RESPONSIBILITY (PidTagResponsibility)](pidtagresponsibility-canonical-property.md)true.  
    
   - Если флаг MAPI_SUBMITTED не установлен, указав, что получатель действительно получил исходное сообщение, **PrepareSubmit** изменяет  свойство **PR_RECIPIENT_TYPE** на MAPI_P1 и задает свойство PR_RESPONSIBILITY true и возвращает клиенту любую ошибку, созданную **prepareSubmit.** 
    
2. ������ ���� MSGFLAG_SUBMIT � �������� **PR_MESSAGE_FLAGS** ���������. 
    
3. ������ �� ���, ��� ������� ��� **PR_RESPONSIBILITY** � ������� ����������� � ������ �������� FALSE, ����� �������, ��� ��� ���������� ��� �������������� ��������������� ��� �������� ���������. 
    
4. Задает дату и время возникновения в **свойстве** [PR_CLIENT_SUBMIT_TIME (PidTagClientSubmitTime).](pidtagclientsubmittime-canonical-property.md)
    
5. Calls [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) to: 
    
   - ���������� ��� ������ �������� � ����������� � �������� ��� ���������� ������������ ����� � ��������� �������.
   - �������� ������������� ����.
   - Проверьте, требуется ли предварительная процессировка, и если требуется предварительная проверка, установите флаг NEEDS_PREPROCESSING и **свойство PR_PREPROCESS** [(PidTagPreprocess),](pidtagpreprocess-canonical-property.md)свойство, зарезервированное для MAPI. 
   - ���������� ����� NEEDS_SPOOLER ��������� ��������� ����� ������� � ���������� � �� ����� ���������� ���� �����������. 
    
6. ���� ���������� ���� ��������� NEEDS_PREPROCESSING ��������� ��������� ������:
    
   - Помещает сообщение в исходячую очередь с SUBMITFLAG_PREPROCESS в свойстве[PR_SUBMIT_FLAGS (PidTagSubmitFlags).](pidtagsubmitflags-canonical-property.md) 
   - ���������� ��������� ������� MAPI, ������� ��� ������� �������.
   - ��������� ���������� ������� � ����� ��������� ��-�������� ������������ � ��������� ������� MAPI. 
   - ��������� ������� MAPI ��������� ��������� ������:
     - Блокирует сообщение, позвонив в IMsgStore::SetLockState. 
     - Выполняет необходимую предварительную подготовку, вызывая все функции предварительной подготовки в порядке регистрации. Поставщики транспорта звонят по вызову IMAPISupport::RegisterPreprocessor для регистрации функций препроцессации. 
     - Вызывает IMessage::SubmitMessage в открытом сообщении, чтобы указать в хранилище сообщений, что препроцессия завершена.

<br/>

Следующие два шага происходят в клиентском процессе, если не было предварительной обработки, и когда пульпер MAPI вызывает **SubmitMessage,** если была предварительная обработка. 

**Поставщик хранения сообщений:**

1. Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - ������������ �����������, ������� ����� ������������.
   - ������������� ��� �������� **PR_RESPONSIBILITY** �������� TRUE ��� �����������, ������� �� ������������. 
   - ���� ��� ���������� ��������, ��� ���� ����� ��������� ��������� � ����������, ��������� ��������� ������:
     - Вызывает IMAPISupport::CompleteMsg, если сообщение было предварительно оформлено или поставщик магазина сообщений хочет, чтобы пуллер MAPI завершил обработку сообщений, которая рекомендуется для вызова крючков обмена сообщениями. Поток сообщений продолжается с пульпером MAPI, как описано в следующей процедуре.  
     - Выполняет следующие задачи, если сообщение не было предпроцессом или поставщик магазина сообщений не хочет, чтобы пулер MAPI завершил обработку сообщений:
       - Копирует сообщение в папку, указанную идентификатором записи в свойстве PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId), если установлено.
       - Удаляет сообщение, если PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit) установлено true.
       - Разблокирует сообщение, если оно заблокировано.
       - Возвращается клиенту. Поток сообщений завершен. 
   
2. ���� ��������� ��������� �� ����� ���������� ��� ����������, �� ���� ����������� ��������, ��� ��������� ��������� ��� ���� NEEDS_SPOOLER ��������� ��������� ������:
    
   - ��������� ���������� � ������� ��������� ��� ��������� ���� SUBMITFLAG_PREPROCESS � �������� **PR_SUBMIT_FLAGS**. 
   - ���������� ��������� ������� MAPI, ��������� ������� ��� �������, ������ ����������� � �������. 
   - ���������� ������� � ����� ��������� ��-�������� ������������ � ������� ������, ����������� ����������� ������� MAPI.
    
���� ��������� �� ����� �������������� ��������� ������� MAPI, ��������� �������� ��������� ������������� �������� �������� **PR_SUBMIT_FLAGS** ��������� SUBMITFLAG_LOCKED. ���� SUBMITFLAG_LOCKED ���������, ��� ��������� ������� MAPI ������������ ��������� ��� ������������� ��� �������������. ������ ��� **PR_SUBMIT_FLAGS,** SUBMITFLAG_PREPROCESS, ����� �������� ��� ��������� ������� ��������������� ��������� ������ ��� ���������� ������������� ���������, ������������������, ���������� ����������. 
  

