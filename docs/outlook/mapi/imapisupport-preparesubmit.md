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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Готовит сообщение для отправки в шпалер MAPI.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in] Указатель на сообщение для подготовки.
    
 _lpulFlags_
  
> [in, out] При входе  _параметр lpulFlags зарезервирован_ и должен быть нулем. На выходе  _lpulFlags должен_ быть NULL. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение было успешно подготовлено.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::P repareSubmit** реализован для объектов поддержки поставщиков сообщений. Поставщики магазинов сообщений звонят **prepareSubmit** при реализации метода [IMessage::SubmitMessage](imessage-submitmessage.md) для подготовки сообщения для отправки в пульпер MAPI. 
  
 **PrepareSubmit** используется для обработки сообщений с MSGFLAG_RESEND в  свойстве [PR_MESSAGE_FLAGS (PidTagMessageFlags).](pidtagmessageflags-canonical-property.md) MSGFLAG_RESEND для сообщений, которые включают запрос, который должен быть оби в случае сбой начальной передачи. **PrepareSubmit** определяет, кто из получателей в списке получателей успешно получил сообщение, а какой нет. 
  
Чтобы получить доступ к списку получателей, **PrepareSubmit** вызывает [метод IMessage::GetRecipientTable.](imessage-getrecipienttable.md) Чтобы получить данные получателя, **PrepareSubmit** вызывает метод [IMAPITable::QueryRows таблицы](imapitable-queryrows.md) получателей. Для каждой строки в таблице **PrepareSubmit** **проверяет свойство PR_RECIPIENT_TYPE** [(PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)и принимает одно из следующих действий:
  
- Если флаг MAPI_SUBMITTED, **PrepareSubmit** очищает флаг и задает **свойство** [PR_RESPONSIBILITY (PidTagResponsibility)](pidtagresponsibility-canonical-property.md)false.
    
- Если флаг MAPI_SUBMITTED не установлен, **PrepareSubmit**  PR_RECIPIENT_TYPE MAPI_P1 и **PR_RESPONSIBILITY** true. 
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Перед вызовом **PrepareSubmit** убедитесь, что вы вызвали метод [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) и установите флаг NOTIFY_READYTOSEND в параметре _ulFlags._ Вызов **SpoolerNotify** должен быть выполнен один раз в сеанс перед вызовом **на PrepareSubmit.** **SpoolerNotify** синхронизирует шпалер MAPI и обеспечивает вход всех необходимых поставщиков транспорта и регистрацию их типов адресов. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

