---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409029"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает текущее сообщение.
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Parameters

 _ppmsg_
  
> [вышел] Указатель на указатель на возвращенный интерфейс для сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
S_FALSE 
  
> В настоящее время для формы вызова не существует сообщения.
    
## <a name="remarks"></a>Примечания

Формы называют **метод IMAPIMessageSite::GetMessage** для получения интерфейса сообщения для текущего сообщения. Текущее сообщение — это то же сообщение, которое ранее было передано в методе [IPersistMessage::InitNew,](ipersistmessage-initnew.md) [IPersistMessage::Load](ipersistmessage-load.md)или [IPersistMessage::SaveCompleted.](ipersistmessage-savecompleted.md) 
  
 **GetMessage** возвращает S_FALSE, если сообщение в настоящее время не существует. Это состояние может возникать после звонков в [метод IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) или до следующего вызова **в IPersistMessage::Load** или **IPersistMessage::SaveCompleted.** 
  
Список интерфейсов, связанных с серверами форм, см. в [перечне интерфейсов форм MAPI.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI использует **метод IMAPIMessageSite::GetMessage** для возврата кэшного указателя сообщения, если он доступен.  <br/> |
   
## <a name="see-also"></a>См. также



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)

