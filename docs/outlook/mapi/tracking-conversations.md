---
title: ������������ �����
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 58157d597d3bb1042d6bc16ff954495a507c8333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812506"
---
# <a name="tracking-conversations"></a>������������ �����

  
  
**Относится к**: Outlook 
  
������������ ��������� �������� ���� ������� �� ���������. ������� ������� ���������� ��� ��������, ������� �������� ��� ������������ ������:
  
- **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))
    
    **PR_CONVERSATION_TOPIC** � ��� ��������������� ���� ���������, ���� ��� �������� �����. Этому свойству присвоено значение свойства **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) сообщение. 
    
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
    
- ������ ����, ���������� ��������� �����, ����������� ��� ������ ������� Win32 [GetTickCount](http://msdn.microsoft.com/en-us/library/ms724408%28VS.85%29.aspx).
    
- ������ ����, ���������� ����������� ������, ������� ���� �� ����� ��������� �����.
    
���� ������� ������� �������� ������ ��������� �������, ���������� ��������� ������������:
  
1. �������� �������� � ������� ������ ������������ ����������. � ������� ������� � ������� UTC, � �� �������� �������.
    
2. ������ ������ ������ ��������� �� �� �� �����.
    
3. ���������� ������ �� ���� � ��� �� ���� ���������.
    
4. ��������� ������ ������ � ������ �����, ������������ ��� ����������� ������������� ������ �������. 
    
5. ��� ���������� ���������� �� ����������, ����� ��������� ��������������� �� ������, ���������� �� **PR_CONVERSATION_TOPIC** ������ � ����� �� **PR_CONVERSATION_INDEX**. Чтобы представить результаты сортировки, присвойте свойству **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) 0 для сообщений с индексом беседы, который является 22 байта в длину. ����� ��� ������ 5-�������� ����������� ������ � �����, ����������� �������� �������� **PR_DEPTH** �� 1. 
    
������ PR_ORIGINAL ������� ����� ����� �������������� ��� ������������ ���������. ������� ��� �������� ��� ���������� �������� ��� ���������������� ��������� ��������� ���������. ��� �������� PR_ORIGINAL �������� ���������������. Если вы не задано явно, например, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), поставщика хранилища сообщений можно использовать значение по умолчанию, или значение **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) свойство. Аналогичным образом Если не установлен **PR_ORIGINAL_AUTHOR_NAME** или **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), эти свойства можно по умолчанию значения **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) и **PR_ CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) свойства соответственно. 
  

