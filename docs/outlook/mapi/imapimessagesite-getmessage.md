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
ms.openlocfilehash: 3612c12a503174484d4a469ffa167922a015ed5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576612"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает текущее сообщение.
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Параметры

 _ppmsg_
  
> [out] Указатель на указатель на возвращенный интерфейс для сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
S_FALSE 
  
> Для вызова формы в настоящий момент не сообщения.
    
## <a name="remarks"></a>Замечания

Форм вызовите метод **IMAPIMessageSite::GetMessage** для получения интерфейса сообщения для текущего сообщения. Текущее сообщение имеет то же сообщение как ранее был передан в метод [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)или [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) . 
  
 **GetMessage** возвращает S_FALSE, если сообщение не в настоящий момент. Это состояние может произойти после вызовов в метод [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) или до следующего вызова **IPersistMessage::Load** или **IPersistMessage::SaveCompleted** будет создано. 
  
Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |Mfcmapi (en) использует метод **IMAPIMessageSite::GetMessage** возвращает указатель в настоящее время кэширования сообщение, если она доступна.  <br/> |
   
## <a name="see-also"></a>См. также



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы формы MAPI](mapi-form-interfaces.md)

