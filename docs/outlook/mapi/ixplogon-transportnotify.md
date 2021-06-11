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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Сигнализирует о возникновении события, о котором поставщик транспорта запрашивал уведомление.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in, out] Битмашка флагов, которые сигнализют о событиях уведомлений. Следующие флаги могут быть установлены шпалером MAPI на входе и должны быть возвращены без изменений на выходе:
    
NOTIFY_ABORT_DEFERRED 
  
> Извещение поставщика транспорта о том, что сообщение, за которое он принял ответственность, откладывается. Только поставщики транспорта, поддерживают отсрочку, должны поддерживать этот флаг. Параметр  _lppvData указывает_ на идентификатор записи отмененного сообщения. Сообщения, которые не обработаны пульпером MAPI, по-прежнему можно отложить, позвонив по [методу IMsgStore::AbortSubmit.](imsgstore-abortsubmit.md) 
    
NOTIFY_BEGIN_INBOUND 
  
> Spooler MAPI теперь может принимать входящие сообщения для этого сеанса поставщика транспорта. Шпалер MAPI регулярно вызывает метод [IXPLogon::P ll,](ixplogon-poll.md) если поставщик транспорта задает флаг LOGON_SP_POLL с вызовом [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) в logon. После NOTIFY_BEGIN_INBOUND флага шпалер MAPI почитает флаг NOTIFY_NEWMAIL, переданный в вызове [методу IMAPISupport::SpoolerNotify.](imapisupport-spoolernotify.md) Строка таблицы состояния для сеанса поставщика транспорта должна быть обновлена перед возвращением, позвонив по методу [IMAPISupport::ModifyStatusRow.](imapisupport-modifystatusrow.md) Флаги NOTIFY_BEGIN_INBOUND и NOTIFY_END_INBOUND являются взаимоисключающими. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Сигнализирует поставщику транспорта как можно быстрее проходить цикл через входящие сообщения. Чтобы выполнить это уведомление, поставщик транспорта должен установить флаг STATUS_INBOUND_FLUSH в свойстве **PR_STATUS_CODE** [(PidTagStatusCode)](pidtagstatuscode-canonical-property.md)строки таблицы состояния как можно скорее с помощью **ModifyStatusRow**. Цикл входящие сообщения завершается, когда поставщик определяет, что скачал все, что он может, или когда он получил вызов метода **TransportNotify** с набором флага NOTIFY_END_INBOUND_FLUSH. До окончания цикла входящих сообщений поставщик не должен вызывать [метод IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) или иным образом отклонить циклы в операционную систему, чтобы ускорить доставку входящих сообщений. Это допустимо, так как шпалер MAPI обычно использует NOTIFY_BEGIN_INBOUND_FLUSH только в ответ на запрос пользователя через клиентскую заявку, чтобы доставить все сообщения сейчас. В конце операции входящий флеш поставщик должен использовать **SpoolerNotify** для очистки флага STATUS_INBOUND_FLUSH в свойстве PR_STATUS_CODE строки состояния.  
    
NOTIFY_BEGIN_OUTBOUND 
  
> Исходящие операции теперь могут происходить для этого сеанса поставщика транспорта. Если для этого поставщика будут отправлены какие-либо сообщения, следует позвонить в [метод IXPLogon::SubmitMessage.](ixplogon-submitmessage.md) Строка таблицы состояния для этого сеанса должна быть обновлена перед возвращением. Флаги NOTIFY_BEGIN_OUTBOUND и NOTIFY_END_OUTBOUND являются взаимоисключающими. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Работает аналогично флагу NOTIFY_BEGIN_INBOUND_FLUSH, но ссылается на исходящие сообщения. Соответствующий флаг состояния STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> Шпалер MAPI должен отменить передачу сообщения, для которого параметр _lppvData_ указывает на 32-битное значение из вызова метода **IXPLogon::SubmitMessage.** Флаг NOTIFY_CANCEL_MESSAGE можно установить без вызова транспортного поставщика, возвращаемого из **службы SubmitMessage,** **IXPLogon::StartMessage** или **метода IXPLogon::EndMessage,** связанного с сообщением. Поставщик транспорта должен как можно скорее вернуться из точки входа, которая занимается отмененным сообщением. Для входящих сообщений, обрабатываемых в настоящее время, поставщик транспорта должен сохранить входящие сообщения, где бы оно в настоящее время не хранилось, и доставить его снова в удобное время. Данные объекта сообщения, уже хранимые для входящих сообщений, удаляются. Если поставщик транспорта не обновил это 32-битное значение во время **StartMessage** или **SubmitMessage,** значение 0 для исходящие сообщения и 1 для входящие сообщения. 
    
NOTIFY_END_INBOUND 
  
> Для этого сеанса поставщика транспорта необходимо прекратить входящие операции. Spooler MAPI перестает использовать метод **Poll** и игнорирует NOTIFY_NEWMAIL для этого сеанса. Обработка сообщений должна быть завершена. Строка таблицы состояния для сеанса транспорта должна быть обновлена путем вызова [ModifyStatusRow](imapisupport-modifystatusrow.md) перед возвращением. Флаги NOTIFY_END_INBOUND и NOTIFY_BEGIN_INBOUND являются взаимоисключающими. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Сообщает поставщику транспорта о выходе из режима флеша во входящие. Поставщик транспорта не должен прекращать загрузку, но загрузка должна быть сделана в фоновом режиме. Строка таблицы состояния для сеанса транспорта должна быть обновлена путем вызова **ModifyStatusRow,** когда поставщик транспорта может выполнить это уведомление. 
    
NOTIFY_END_OUTBOUND 
  
> Исходящие операции должны прекратиться для этого сеанса поставщика транспорта. Шпалер MAPI перестает вызывать **SubmitMessage** и игнорирует **флаг SpoolerNotify** NOTIFY_READYTOSEND. Если в настоящее время отправляется исходящие сообщения, его не следует прекращать; чтобы остановить доставку сообщения, используйте флаг NOTIFY_CANCEL_MESSAGE. Строка таблицы состояния для этого сеанса должна быть обновлена путем вызова **ModifyStatusRow** перед возвращением. Флаги NOTIFY_END_INBOUND и NOTIFY_BEGIN_OUTBOUND являются взаимоисключающими. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Работает аналогично NOTIFY_END_INBOUND_FLUSH, но относится к исходящие сообщения. Соответствующий флаг состояния STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> [вышел] Указатель на указатель на данные, определенные событиям. Дополнительные сведения о том, что _указывает lppvData,_ см. в описании параметра _lpulFlags._ 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Spooler MAPI вызывает **метод IXPLogon::TransportNotify,** чтобы сигнализировать поставщику транспорта о событиях, для которых запрашивалось уведомление. Эти события включают запрос пулера MAPI для отмены передачи сообщений, начала или окончания входящие или исходящие транспортные операции, а также начало или завершение операции по очистке очереди входящие или исходящие сообщения. 
  
Когда пользователь пытается отменить сообщение, которое поставщик транспорта ранее отложил, spooler MAPI вызывает **TransportNotify**, передав как флаги NOTIFY_ABORT_DEFERRED, так и NOTIFY_CANCEL_MESSAGE в  _ulFlags_. Если шпалер MAPI отключается и по-прежнему содержит сообщения в очереди, он NOTIFY_ABORT_DEFERRED в _ulFlags_ при вызове **TransportNotify.**
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик должен синхронизировать доступ к своим данным по этому вызову, так как шпалер MAPI может вызывать этот метод из другого потока выполнения или из процедуры для другого окна. Это, скорее всего, произойдет, когда шпалер MAPI подавит сигнал об отмене сообщения, которое поставщик транспорта начал отправлять.
  
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

