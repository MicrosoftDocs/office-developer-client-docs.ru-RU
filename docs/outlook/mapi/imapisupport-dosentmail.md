---
title: Имаписуппортдосентмаил
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
ms.openlocfilehash: 8289b8dd2e0ab3c760e77a37b821d2fe74e4abe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315971"
---
# <a name="imapisupportdosentmail"></a>IMAPISupport::DoSentMail

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
������������ ������������ ���������.
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _Лпмессаже_
  
> [in] ��������� �� ��������� ���������, ��� �������� ����� ������ ��������� � �����, ��������������� ��� �������� ������������ ���������.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Замечания

The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.
  
 **DoSentMail** ��������� ��������� ������: 
  
- Проверяет сообщение для свойства **пр_делете_афтер_субмит** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)), чтобы определить, следует ли удалять сообщение после отправки.
    
- ���������� ������������ ����� �������������.
    
- ���������� ��������� ��� ������ ����������� ������� ��� �����, ������������ ���������� ���������.
    
- ���������� ��������� � ����� "������������", ����� "���������", ��� � ������ �����.
    
- ����������� ���������.
    
## <a name="see-also"></a>См. также



[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[������������ �������� PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

