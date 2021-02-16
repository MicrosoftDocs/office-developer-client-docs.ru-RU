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
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414160"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сообщает поставщику транспорта, что пул MAPI завершил обработку исходящие сообщения.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulMsgRef_
  
> [in] Значение ссылки для конкретного сообщения, полученное во время предыдущего вызова метода [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md) 
    
 _lpulFlags_
  
> [out] Битовая маской флагов, которая показывает пуле MAPI, что следует делать с сообщением. Если флаги не установлены, сообщение отправлено. Можно установить следующие флаги:
    
END_DONT_RESEND 
  
> На данный момент у поставщика транспорта есть все необходимые сведения об этом сообщении. Если поставщику транспорта требуются дополнительные сведения или когда он отправил сообщение, он оповещение пула MAPI путем вызова метода [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) с флагом NOTIFY_SENTDEFERRED и путем передачи идентификатора записи сообщения. 
    
END_RESEND_LATER 
  
> В настоящее время поставщик транспорта не отправляет сообщение по причинам, не относянымся к ошибкам. Для отправки сообщения поставщик транспорта должен быть вызван позже еще раз.
    
END_RESEND_NOW 
  
> Поставщик транспорта должен перезапустить сообщение, переданное ему в вызове метода [IMessage::SubmitMessage.](imessage-submitmessage.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Пулер MAPI вызывает метод **IXPLogon::EndMessage** после завершения обработки, вовлеченной в предоставление расширенных сведений о доставке или ненамере. 
  
После возврата этого вызова значение параметра  _ulMsgRef_ больше не является допустимым для этого сообщения. Поставщик транспорта может повторно использовать то же значение в будущем сообщении. 
  
Все объекты, которые поставщик транспорта открывает во время передачи сообщения, должны быть освобождены до возврата вызова **EndMessage,** за исключением объекта сообщения, который пулер MAPI передает поставщику транспорта. Объект сообщения, переданный пулом MAPI, недействителен после вызова **EndMessage.** 
  
## <a name="see-also"></a>См. также



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

