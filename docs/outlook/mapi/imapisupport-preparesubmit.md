---
title: имаписуппортпрепаресубмит
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
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425738"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Подготавливает сообщение для отправки в очередь печати MAPI.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _лпмессаже_
  
> возврата Указатель на сообщение, которое необходимо подготовить.
    
 _лпулфлагс_
  
> [вход, выход] В параметре input параметр _лпулфлагс_ зарезервирован и должен равняться нулю. В выходных данных _лпулфлагс_ должен иметь значение null. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение успешно подготовлено.
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт::P репаресубмит** реализован для объектов поддержки поставщика хранилища сообщений. Поставщики хранилищ сообщений вызывают **препаресубмит** в своей реализации метода [iMessage:: субмитмессаже](imessage-submitmessage.md) , чтобы подготовить сообщение для отправки в Диспетчер очереди MAPI. 
  
 **Препаресубмит** используется для обработки сообщений с установленным флагом MSGFLAG_RESEND в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). MSGFLAG_RESEND задается для сообщений, которые включают в себя запрос на повторную отправку при неудачной попытке первоначальной передачи. **Препаресубмит** определяет, какие получатели в списке получателей успешно получили сообщение, а какие нет. 
  
Чтобы получить доступ к списку получателей, **препаресубмит** вызывает метод [iMessage:: жетреЦипиенттабле](imessage-getrecipienttable.md) для сообщения. Чтобы получить данные получателя, **препаресубмит** вызывает метод [IMAPITable:: QueryRows](imapitable-queryrows.md) для таблицы получателей. Для каждой строки в таблице **препаресубмит** проверяет свойство **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) и выполняет одно из следующих действий:
  
- Если установлен флаг MAPI_SUBMITTED, **препаресубмит** очищает флаг и задает для свойства **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) значение false.
    
- Если флаг MAPI_SUBMITTED не установлен, **препаресубмит** изменяет **PR_RECIPIENT_TYPE** в MAPI_P1 и устанавливает **PR_RESPONSIBILITY** в значение true. 
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Перед вызовом **препаресубмит**убедитесь, что вы вызвали метод [Имаписуппорт:: спулернотифи](imapisupport-spoolernotify.md) и установите флаг NOTIFY_READYTOSEND в параметре _ulFlags_ . Вызов **спулернотифи** должен быть сделан один раз для каждого сеанса перед вызовом **препаресубмит**. **Спулернотифи** синхронизирует Диспетчер очереди MAPI и гарантирует, что все необходимые поставщики транспорта вошли в систему и их типы адресов зарегистрированы. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

