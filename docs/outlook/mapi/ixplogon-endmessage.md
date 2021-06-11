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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Информирует поставщика транспорта о том, что шпалер MAPI завершил обработку исходящие сообщения.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulMsgRef_
  
> [in] Эталонное значение, определенное для сообщений, которое было получено в более ранней ссылке на [метод IXPLogon::SubmitMessage.](ixplogon-submitmessage.md) 
    
 _lpulFlags_
  
> [вышел] Битмашка флагов, которая указывает шпалеру MAPI, что он должен делать с сообщением. Если флаги не установлены, сообщение отправлено. Можно установить следующие флаги:
    
END_DONT_RESEND 
  
> Поставщик транспорта имеет всю необходимую информацию об этом сообщении на данный момент. Если поставщик транспорта требует дополнительных сведений или отправляет сообщение, он оповещение пулера MAPI вызывает метод [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) с флагом NOTIFY_SENTDEFERRED и путем передачи идентификатора записи сообщения. 
    
END_RESEND_LATER 
  
> Поставщик транспорта не отправляет сообщение в настоящее время по причинам, которые не являются условиями ошибки. Поставщик транспорта должен быть вызван позже, чтобы отправить сообщение.
    
END_RESEND_NOW 
  
> Поставщик транспорта должен перезапустить переданное ему сообщение в [вызове метода IMessage::SubmitMessage.](imessage-submitmessage.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Шпалер MAPI вызывает **метод IXPLogon::EndMessage** после завершения обработки, которая была задействована в предоставлении расширенных сведений о доставке или неделиверии. 
  
После возвращения этого вызова значение  _параметра ulMsgRef_ больше не допустимо для этого сообщения. Поставщик транспорта может повторно использовать такое же значение в будущем сообщении. 
  
Все объекты, открываемые поставщиком транспорта во время передачи сообщения, должны быть освобождены до возврата вызова **EndMessage,** за исключением объекта сообщения, который spooler MAPI передает поставщику транспорта. Объект сообщения, переданный пулером MAPI, недействителен после вызова **EndMessage.** 
  
## <a name="see-also"></a>См. также



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

