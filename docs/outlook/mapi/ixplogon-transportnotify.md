---
title: IXPLogonTransportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportNotify
api_type:
- COM
ms.assetid: c712fc17-f436-41cf-9aa3-186c9a86d56e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2482dc39d3f1d1568b45dd3de88358e08d190be4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428860"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**Относится к**: Outlook 2013 | Outlook 2016 
  
Сигнализирует о возникновении события, о котором поставщик транспорта запросил уведомление.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Параметры

 _lpulFlags_
  
> [in, out] Битоваяmas флагов, сигнализовая о событиях уведомлений. Пулер MAPI может установить следующие флаги при вводе и должен быть возвращен без изменений при выходе:
    
NOTIFY_ABORT_DEFERRED 
  
> Извещение поставщика транспорта о том, что сообщение, за которое он принял ответственность, откладывается. Только поставщики транспорта, поддерживают отсрочку, должны поддерживать этот флаг. Параметр  _lppvData указывает_ на идентификатор записи отмененного сообщения. Сообщения, которые не обработаны пулом MAPI, по-прежнему можно отложить, вызывая метод [IMsgStore::AbortSubmit.](imsgstore-abortsubmit.md) 
    
NOTIFY_BEGIN_INBOUND 
  
> The MAPI spooler can now accept inbound messages for this transport provider session. Пулер MAPI регулярно вызывает метод [IXPLogon::P oll,](ixplogon-poll.md) если поставщик транспорта установил флаг LOGON_SP_POLL с вызовом [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) при логи. После NOTIFY_BEGIN_INBOUND флага пул MAPI будет соблюдать флаг NOTIFY_NEWMAIL, переданный в вызове метода [IMAPISupport::SpoolerNotify.](imapisupport-spoolernotify.md) Строка таблицы состояния для сеанса поставщика транспорта должна быть обновлена перед возвратом путем вызова метода [IMAPISupport::ModifyStatusRow.](imapisupport-modifystatusrow.md) Флаги NOTIFY_BEGIN_INBOUND и NOTIFY_END_INBOUND взаимоисключающие. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Сообщает поставщику транспорта о том, что необходимо как можно быстрее проходить входящие сообщения. Чтобы соответствовать этому уведомлению, поставщик транспорта должен установить флаг STATUS_INBOUND_FLUSH в свойстве **PR_STATUS_CODE** ([PidTagStatusCode)](pidtagstatuscode-canonical-property.md)строки таблицы состояния как можно скорее с помощью **ModifyStatusRow**. Цикл обмена входящие сообщения завершается, когда поставщик определяет, что он скачал все, что может, или когда он получил вызов метода **TransportNotify** с установленным NOTIFY_END_INBOUND_FLUSH флагом. До окончания цикла входящих сообщений поставщик не должен вызывать метод [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) или иным образом отклонить циклы в операционной системе, чтобы ускорить доставку входящих сообщений. Это допустимо, так как пулер MAPI обычно использует NOTIFY_BEGIN_INBOUND_FLUSH только в ответ на запрос пользователя через клиентские приложения для доставки всех сообщений. В конце операции очистки входящий почты поставщик должен использовать **SpoolerNotify** для  очистки флага STATUS_INBOUND_FLUSH в свойстве PR_STATUS_CODE строки состояния. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Исходящие операции теперь могут происходить для этого сеанса поставщика транспорта. Если для этого поставщика необходимо отправить какие-либо сообщения, следует вызвать метод [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md) Строка таблицы состояния для этого сеанса должна быть обновлена перед возвратом. Флаги NOTIFY_BEGIN_OUTBOUND и NOTIFY_END_OUTBOUND взаимоисключающие. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Работает аналогично флагу NOTIFY_BEGIN_INBOUND_FLUSH, но ссылается на исходящие сообщения. Соответствующий флаг состояния STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> Пулер MAPI должен отменить передачу сообщения, для которого параметр _lppvData_ указывает на 32-битное значение из вызова метода **IXPLogon::SubmitMessage.** Флаг NOTIFY_CANCEL_MESSAGE можно установить без возврата поставщика транспорта из метода **SubmitMessage,** **IXPLogon::StartMessage** или **IXPLogon::EndMessage,** связанного с сообщением. Поставщик транспорта должен как можно скорее вернуться из точки входа, которая обработчик отмененного сообщения. Для входящих сообщений, обрабатываемых в данный момент, поставщик транспорта должен сохранить входящие сообщения там, где оно хранится в настоящее время, и доставить его снова в следующий удобное время. Данные объекта сообщения, уже сохраненные для входящих сообщений, удаляются. Если поставщик транспорта не обновил это 32-битное значение во время **StartMessage** или **SubmitMessage,** значение будет 0 для исходящие сообщения и 1 для входящие сообщения. 
    
NOTIFY_END_INBOUND 
  
> Для этого сеанса поставщика транспорта входящие операции должны быть прекращены. Пулер MAPI перестает использовать метод **Poll** и игнорирует NOTIFY_NEWMAIL для этого сеанса. Необходимо завершить обработку сообщений. Строка таблицы состояния для сеанса транспорта должна быть обновлена путем вызова [ModifyStatusRow](imapisupport-modifystatusrow.md) перед возвратом. Флаги NOTIFY_END_INBOUND и NOTIFY_BEGIN_INBOUND взаимоисключающие. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Сообщает поставщику транспорта о выходе из режима очистки входящий почты. Поставщик транспорта не должен останавливать загрузку, но загрузку следует делать в фоновом режиме. Строка таблицы состояния для сеанса транспорта должна обновляться путем вызова **ModifyStatusRow,** когда поставщик транспорта может выполнить это уведомление. 
    
NOTIFY_END_OUTBOUND 
  
> Для этого сеанса поставщика транспорта исходящие операции должны быть прекращены. Пулер MAPI перестает вызывать **SubmitMessage** и игнорирует флаг **SpoolerNotify** NOTIFY_READYTOSEND. Если в настоящее время отправляется исходящие сообщения, его не следует остановить; чтобы остановить доставку сообщения, используйте флаг NOTIFY_CANCEL_MESSAGE сообщения. Строка таблицы состояния для этого сеанса должна быть обновлена путем вызова **ModifyStatusRow** перед возвратом. Флаги NOTIFY_END_INBOUND и NOTIFY_BEGIN_OUTBOUND взаимоисключающие. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Работает аналогично NOTIFY_END_INBOUND_FLUSH, но относится к исходящие сообщения. Соответствующий флаг состояния STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> [out] Указатель на указатель на данные конкретного события. Дополнительные сведения о том, что _указывает lppvData,_ см. в описании параметра _lpulFlags._ 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Пулер MAPI вызывает метод **IXPLogon::TransportNotify,** чтобы уведомить поставщика транспорта о событиях, для которых запрашивается уведомление. К этим событиям относится запрос пула MAPI на отмену передачи сообщений, начало или завершение операций транспорта входящие и исходящие сообщения, а также начало или завершение операции по очистке очереди входящие или исходящие сообщения. 
  
Когда пользователь пытается отменить сообщение, которое поставщик транспорта ранее отложил, пулер MAPI вызывает **TransportNotify,** передавая флаги NOTIFY_ABORT_DEFERRED и NOTIFY_CANCEL_MESSAGE в _ulFlags._ Если пулер MAPI выключается и все еще содержит сообщения в очереди, он передает только NOTIFY_ABORT_DEFERRED в _ulFlags_ при вызове **TransportNotify.**
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик должен синхронизировать доступ к своим данным в этом вызове, так как пулер MAPI может вызвать этот метод из другого потока выполнения или из процедуры для другого окна. Скорее всего, это произойдет, когда пульщик MAPI сообщает об отмене сообщения, которое начал отправлять поставщик транспорта.
  
## <a name="see-also"></a>См. также

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) 
- [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) 
- [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) 
- [IXPLogon::EndMessage](ixplogon-endmessage.md) 
- [IXPLogon::Poll](ixplogon-poll.md)
- [IXPLogon::StartMessage](ixplogon-startmessage.md)
- [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [IXPLogon : IUnknown](ixplogoniunknown.md)

