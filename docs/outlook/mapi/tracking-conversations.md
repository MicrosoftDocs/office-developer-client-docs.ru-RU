---
title: Отслеживание бесед
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: 'Дата последнего изменения: 23 июля 2011 г.'
localization_priority: Priority
ms.openlocfilehash: 3a59a7a15b4647832634adc4757544876b8841b1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706224"
---
# <a name="tracking-conversations"></a>Отслеживание бесед

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отслеживание беседы — это сбор ответов на сообщение. Клиенты должны настроить два свойства, помогающие облегчающие отслеживание бесед:
  
- **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC** — нормализованная тема сообщения, тема без строк префикса Установите для этого свойства значение свойства **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) сообщения. 
    
- **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))
    
    **PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI. 
    
 **ScCreateConversationIndex** ������� �������� ������� ������ ��� ���� ��������� ���������. **ScCreateConversationIndex** ��������� ������ ��� ���� ���������, ������� �������� 22 ����� � �����, � ����� �� ���� ��� ��������� �������� ��������� ������� 5 ����. 
  
��������� ����� ������� �� 22 �����, ��������� �� ���� ������:
  
- ���� ��������������� ������. ��� �������� ����� 1.
    
- ���� ���� ��� ������� ��������� ����� ������������� � ������ [FILETIME](filetime.md) ���������. 
    
- ����������� ���� ���������� ���������� ������������� ��� [������������� GUID](guid.md)� ������.
    
������ ���� �������� ������� �� 5 ������, ��������� ��������� �������:
  
- ���� ���, ���������� ���, ������� ������������ �������� ����� �������� ������� � �������, ���������� � ����� �������� �����������. ���� ��� ����� ����� �������� 0, ���� ������� ������, ���.02 ������� � ������, ��� ��� ���� � 1, ���� �������� �� ��������� ����� ������� � ������, ��� 56 ���.
    
- 30 ���� ���, ���������� �������� ����� �������� ������� � ����� � ����� ��������� � �������� **FILETIME**. ��� ����� ����� �������� ��������� � ������� ������ �� ���� ���������, � ����������� �� ������� ����. ���� ���� ��� ����� ����, **ScCreateConversationIndex** ������� ������� 15 ��� � ������ 18 �������� ������. ���� ���� ���, ������� ������� ������� 10 ��� � ������ 23 �����. 
    
- ������ ����, ���������� ��������� �����, ����������� ��� ������ ������� Win32 [GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx).
    
- ������ ����, ���������� ����������� ������, ������� ���� �� ����� ��������� �����.
    
���� ������� ������� �������� ������ ��������� �������, ���������� ��������� ������������:
  
1. �������� �������� � ������� ������ ������������ ����������. � ������� ������� � ������� UTC, � �� �������� �������.
    
2. ������ ������ ������ ��������� �� �� �� �����.
    
3. ���������� ������ �� ���� � ��� �� ���� ���������.
    
4. ��������� ������ ������ � ������ �����, ������������ ��� ����������� ������������� ������ �������. 
    
5. Для реализации сортировки по категориям, чтобы сообщения группировались по темам, сначала выполните сортировку по **PR_CONVERSATION_TOPIC**, а затем по **PR_CONVERSATION_INDEX**. Чтобы представить результаты сортировки, присвойте свойству **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) значение 0 для сообщений с длиной индекса беседы 22 байта. Затем для каждого увеличения длины на 5 байтов увеличивайте значение свойства **PR_DEPTH** на единицу. 
    
������ PR_ORIGINAL ������� ����� ����� �������������� ��� ������������ ���������. ������� ��� �������� ��� ���������� �������� ��� ���������������� ��������� ��������� ���������. Все свойства PR_ORIGINAL являются необязательными. Если явным образом не присвоено значение, например **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), поставщик хранилища сообщений может использовать значение по умолчанию или значение свойства **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). Аналогичным образом, если не установлено значение **PR_ORIGINAL_AUTHOR_NAME** или **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), этим свойствам могут быть по умолчанию присвоены значения свойств **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) и **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) соответственно. 
  

