---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f6902b45cde3e5349d69b6f35c3f8980deb031b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809178"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**Относится к**: Outlook 
  
Подготавливает сообщение для отправки диспетчер очереди MAPI.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpMessage_
  
> [in] Указатель на сообщение для подготовки.
    
 _lpulFlags_
  
> [in, out] На входе _lpulFlags_ параметр зарезервирован и должно быть равно нулю. В выходных данных _lpulFlags_ должен иметь значение NULL. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Сообщение было успешно подготовлен.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::PrepareSubmit** реализуется для объектов поддержки поставщика хранилища сообщений. Поставщики хранилища сообщений вызов **PrepareSubmit** в их реализации метода [IMessage::SubmitMessage](imessage-submitmessage.md) для подготовки сообщение для отправки в очередь MAPI. 
  
 **PrepareSubmit** используется для обработки сообщений, для которых флаг MSGFLAG_RESEND в своем свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). MSGFLAG_RESEND имеет значение для сообщений, которые включают запрос повторно при сбое начального передачи. **PrepareSubmit** определяет, какой из получателей в список получателей успешно получено сообщение и которого не. 
  
Для доступа к списку получателей, **PrepareSubmit** вызывает метод [IMessage::GetRecipientTable](imessage-getrecipienttable.md) сообщение. Чтобы получить данные получателей, **PrepareSubmit** вызывает метод [IMAPITable::QueryRows](imapitable-queryrows.md) таблицы получателей. Для каждой строки в таблице **PrepareSubmit** проверяет свойство **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) и выполняет одно из следующих действий:
  
- Если установлен флаг MAPI_SUBMITTED, **PrepareSubmit** сбрасывает и устанавливает для свойства **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) значение FALSE.
    
- Если флаг MAPI_SUBMITTED не установлен, **PrepareSubmit** изменяет **PR_RECIPIENT_TYPE** MAPI_P1 и **PR_RESPONSIBILITY** на значение TRUE. 
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Перед вызовом **PrepareSubmit**обязательно, задать флаг NOTIFY_READYTOSEND с помощью параметра _ulFlags_ и вызывается метод [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) . Вызов **SpoolerNotify** необходимо выполнить один раз в сеансе до вызова **PrepareSubmit**. **SpoolerNotify** синхронизирует диспетчер очереди MAPI, а также гарантирует, что все поставщики необходимые транспорта зашли в систему и зарегистрированные их типов адресов. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

