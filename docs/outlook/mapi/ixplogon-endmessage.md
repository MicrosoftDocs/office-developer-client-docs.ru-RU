---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f727d68e0e193e8f2e148d881968993f836f8ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582471"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Информирует поставщика транспорта, что диспетчер очереди MAPI завершения обработки на исходящее сообщение.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulMsgRef_
  
> [in] Значение ссылки конкретного сообщения, полученные в более ранних вызова метода [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . 
    
 _lpulFlags_
  
> [out] Битовая маска флаги, которое указывает диспетчер очереди MAPI, что следует сделать с сообщением. Если флаги не установлены, отправлено сообщение. Можно задать следующие флажки:
    
END_DONT_RESEND 
  
> Поставщика транспорта содержит все сведения, необходимые об этом сообщении в данный момент. Когда поставщика транспорта нужны дополнительные сведения или сообщение отправлено, Уведомляет диспетчер очереди MAPI путем вызова метода [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) с флагом NOTIFY_SENTDEFERRED и, передавая код запись сообщения. 
    
END_RESEND_LATER 
  
> Поставщика транспорта не отправляет сообщение в настоящее время по причинам, которые не являются условия ошибок. Поставщика транспорта должен быть вызван снова более поздней версии для отправки сообщения.
    
END_RESEND_NOW 
  
> Поставщика транспорта необходимо перезагрузить сообщение, переданное для вызова метода [IMessage::SubmitMessage](imessage-submitmessage.md) . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
## <a name="remarks"></a>Замечания

Диспетчер очереди MAPI вызывает метод **IXPLogon::EndMessage** после завершения обработки в области расширенного доставки или сведения о недоставке. 
  
После возвращения этого вызова значение с помощью параметра _ulMsgRef_ больше не действителен для данного сообщения. Поставщика транспорта можно повторно использовать такое же значение на последующих сообщений. 
  
Все объекты, поставщика транспорта открывает во время передачи сообщения необходимо освободить перед возврат вызова **EndMessage** , за исключением объект сообщения, диспетчер очереди MAPI передает поставщика транспорта. После вызова **EndMessage** недопустимый объект сообщения, переданного по очереди MAPI. 
  
## <a name="see-also"></a>См. также



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

