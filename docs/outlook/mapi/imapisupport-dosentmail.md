---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 2bded946a1fc7d7ab181d3953defa24e247c003c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809133"
---
# <a name="imapisupportdosentmail"></a>IMAPISupport::DoSentMail

  
  
**Относится к**: Outlook 
  
������������ ������������ ���������.
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpMessage_
  
> [in] ��������� �� ��������� ���������, ��� �������� ����� ������ ��������� � �����, ��������������� ��� �������� ������������ ���������.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.
  
 **DoSentMail** ��������� ��������� ������: 
  
- Проверяет сообщения для свойства **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)), чтобы определить, нужно ли удалять после отправки сообщения.
    
- ���������� ������������ ����� �������������.
    
- ���������� ��������� ��� ������ ����������� ������� ��� �����, ������������ ���������� ���������.
    
- ���������� ��������� � ����� "������������", ����� "���������", ��� � ������ �����.
    
- ����������� ���������.
    
## <a name="see-also"></a>��. �����



[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[������������ �������� PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

