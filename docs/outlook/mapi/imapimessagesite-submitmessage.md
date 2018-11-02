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
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 587b8bbb7ac25a7977d8962535f1909464ffc248
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571103"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Объекты формы вызовите метод **IMAPIMessageSite::SubmitMessage** для запроса, что сообщение добавляемых в очередь для доставки. На сайте сообщения должны вызвать метод [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) перед отправкой сообщения. Сообщение не требуется быть сохранен ранее, так как **SubmitMessage** необходимо вызвать сообщение сохраняется, если сообщение было изменено. После возврата **SubmitMessage**формы необходимо проверить для текущего сообщения и затем закрыть самого, если не существует. 
  
Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |Mfcmapi (en) использует метод **IMAPIMessageSite::SubmitMessage** для сохранения сообщения. Во-первых он вызывает метод **IPersistMessage::HandsOffMessage** и вызывает **SubmitMessage**.  <br/> |
   
## <a name="see-also"></a>См. также



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы формы MAPI](mapi-form-interfaces.md)

