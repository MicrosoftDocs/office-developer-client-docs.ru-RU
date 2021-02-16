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
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425738"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Подготовка сообщения для отправки в пул MAPI.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpMessage_
  
> [in] Указатель на сообщение, которое необходимо подготовить.
    
 _lpulFlags_
  
> [in, out] При вводе параметр  _lpulFlags зарезервирован_ и должен быть нулем. В выходных  _данных lpulFlags должен_ иметь NULL. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение успешно подготовлено.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::P repareSubmit** реализован для объектов поддержки поставщика службы хранения сообщений. Поставщики реализации метода [IMessage::SubmitMessage](imessage-submitmessage.md) вызывали **PrepareSubmit** для подготовки сообщения к отправке в пулер MAPI. 
  
 **PrepareSubmit** используется для обработки сообщений с флагом MSGFLAG_RESEND в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags).](pidtagmessageflags-canonical-property.md) MSGFLAG_RESEND для сообщений, которые содержат запрос на повторное обращение при сбойе начальной передачи. **PrepareSubmit** определяет, какой из получателей в списке получателей успешно получил сообщение, а какой нет. 
  
Чтобы получить доступ к списку получателей, **PrepareSubmit** вызывает метод [IMessage::GetRecipientTable](imessage-getrecipienttable.md) сообщения. Чтобы получить данные получателя, **PrepareSubmit** вызывает метод [IMAPITable::QueryRows](imapitable-queryrows.md) таблицы получателей. Для каждой строки таблицы **PrepareSubmit** проверяет **свойство PR_RECIPIENT_TYPE** ([PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)и делает одно из следующих действий:
  
- Если флаг MAPI_SUBMITTED установлен, **PrepareSubmit** очищает флаг и устанавливает для свойства **PR_RESPONSIBILITY** ([PidTagResponsibility)](pidtagresponsibility-canonical-property.md)false.
    
- Если флаг MAPI_SUBMITTED не установлен, **prepareSubmit** **PR_RECIPIENT_TYPE** MAPI_P1 и устанавливает PR_RESPONSIBILITY **true.** 
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Перед вызовом **PrepareSubmit** убедитесь, что вы вызвали метод [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) и установили флаг NOTIFY_READYTOSEND в параметре _ulFlags._ Вызов **SpoolerNotify** должен быть выполнен один раз на сеанс перед вызовом **PrepareSubmit.** **SpoolerNotify** синхронизирует пул MAPI и обеспечивает регистрацию всех необходимых поставщиков транспорта и их типов адресов. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

