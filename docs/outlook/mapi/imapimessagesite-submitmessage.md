---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 694ee8b12b9918502e60c0c6ea92992cc1062945
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808983"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**Применимо к**: Outlook 
  
Запросы в текущем сообщении очереди для доставки.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как отправить сообщение. Можно задать следующий флаг:
    
FORCE_SUBMIT 
  
> MAPI следует отправить сообщение даже в том случае, если не могут отправляться немедленно.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Объекты формы вызовите метод **IMAPIMessageSite::SubmitMessage** для запроса, что сообщение добавляемых в очередь для доставки. На сайте сообщения должны вызвать метод [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) перед отправкой сообщения. Сообщение не требуется быть сохранен ранее, так как **SubmitMessage** необходимо вызвать сообщение сохраняется, если сообщение было изменено. После возврата **SubmitMessage**формы необходимо проверить для текущего сообщения и затем закрыть самого, если не существует. 
  
Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |Mfcmapi (en) использует метод **IMAPIMessageSite::SubmitMessage** для сохранения сообщения. Во-первых он вызывает метод **IPersistMessage::HandsOffMessage** и вызывает **SubmitMessage**.  <br/> |
   
## <a name="see-also"></a>См. также



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы формы MAPI](mapi-form-interfaces.md)

