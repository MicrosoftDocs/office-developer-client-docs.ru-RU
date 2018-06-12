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
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 5429f98a0335ae99b719d0f15b66a95ba87430e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809643"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**Применимо к**: Outlook 
  
Указывает на возникновение события, о том, какие поставщика транспорта запрошено уведомление.
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in, out] Битовая маска флаги, сообщающий события уведомления. Следующие флаги можно задать диспетчером очереди MAPI на входные данные и должны быть возвращены без изменений на выходных данных:
    
NOTIFY_ABORT_DEFERRED 
  
> Уведомляет поставщика транспорта о том, что сообщения, для которого он принят ответственность за откладывается. Только поставщики транспорта, которые поддерживают об отсрочках должен поддерживать этот флаг. Параметр _lppvData_ указывает идентификатор записи отмененные сообщения. Сообщения, которые не обработан диспетчер очереди MAPI по-прежнему может быть отложено путем вызова метода [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) . 
    
NOTIFY_BEGIN_INBOUND 
  
> Диспетчер очереди MAPI теперь может принимать входящие сообщения для данного сеанса поставщика транспорта. Диспетчер очереди MAPI регулярно вызывает метод [IXPLogon::Poll](ixplogon-poll.md) , поставщика транспорта установить флаг LOGON_SP_POLL с вызова [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) при входе в систему. После установки флага NOTIFY_BEGIN_INBOUND диспетчер очереди MAPI учитывает NOTIFY_NEWMAIL флаг, переданный в вызове метода [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) . Строка таблицы состояния сеанса поставщика транспорта следует обновить до возвращения путем вызова метода [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . Флаги NOTIFY_BEGIN_INBOUND и NOTIFY_END_INBOUND являются взаимоисключающими. 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> Сигналы поставщика транспорта для перехода по входящих сообщений, как можно скорее. Для выполнения этого уведомления, поставщика транспорта следует устанавливать флаг STATUS_INBOUND_FLUSH в свойстве **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) его строку в таблице состояния сразу после его можно с помощью **ModifyStatusRow**. Если поставщик определяет его загрузки все, что она может или при получении вызова метода **TransportNotify** с установленным флагом NOTIFY_END_INBOUND_FLUSH входящих сообщений цикл будет завершена. До конца входящих сообщений цикл поставщик не вызвать метод [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) или в противном случае освободить циклов для операционной системы для доставки скорость входящих сообщений. Это допустимо, поскольку диспетчер очереди MAPI обычно используется NOTIFY_BEGIN_INBOUND_FLUSH только в ответ на запрос пользователя, с помощью клиентского приложения теперь доставка всех сообщений. В конце входящих сброса операции поставщика следует использовать **SpoolerNotify** Снимите флаг STATUS_INBOUND_FLUSH в свойстве **PR_STATUS_CODE** его строке состояния. 
    
NOTIFY_BEGIN_OUTBOUND 
  
> Исходящие операции теперь могут возникнуть для данного сеанса поставщика транспорта. Если все сообщения, отправляемые для данного поставщика, исходя из вызов метода [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . Строка таблицы состояние для данного сеанса следует обновить до возвращения. Флаги NOTIFY_BEGIN_OUTBOUND и NOTIFY_END_OUTBOUND являются взаимоисключающими. 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> Флаг NOTIFY_BEGIN_INBOUND_FLUSH работает так же, но ссылается на исходящие сообщения. Флаг соответствующего состояния — STATUS_OUTBOUND_FLUSH.
    
NOTIFY_CANCEL_MESSAGE 
  
> Диспетчер очереди MAPI необходимо отменить передачу сообщения, для которого указывает параметр _lppvData_ на 32-разрядное значение из метода **IXPLogon::SubmitMessage** вызова. Флаг NOTIFY_CANCEL_MESSAGE может быть задан без поставщика транспорта, возвращенные **SubmitMessage**, **IXPLogon::StartMessage**или вызова метода **IXPLogon::EndMessage** , который связан с сообщением. Поставщика транспорта должен возвращать из точки входа, обрабатывающего отмененное сообщение как можно скорее. Для входящего сообщения, которое было выполнено поставщика транспорта следует сохранить входящего сообщения везде, где он хранится в настоящее время и обеспечивают еще раз при следующем удобное время. Данные объекта сообщение, хранящийся для входящего сообщения удаляются. Если во время **StartMessage** или **SubmitMessage** поставщика транспорта не добавляются это значение 32-разрядная версия, значение 0 для исходящих сообщений и 1 для входящих сообщений. 
    
NOTIFY_END_INBOUND 
  
> Входящие операции необходимо прекратить для данного сеанса поставщика транспорта. Диспетчер очереди MAPI прекращает использование метода **опроса** и игнорирует NOTIFY_NEWMAIL для данного сеанса. Необходимо выполнить в обрабатывать сообщения. Строка таблицы состояния сеанса транспорта обновления путем вызова [ModifyStatusRow](imapisupport-modifystatusrow.md) до возвращения. Флаги NOTIFY_END_INBOUND и NOTIFY_BEGIN_INBOUND являются взаимоисключающими. 
    
NOTIFY_END_INBOUND_FLUSH 
  
> Уведомляет поставщика транспорта из входящих сброса режим. Поставщика транспорта не должны прекратить загрузку, но загрузка должно выполняться в фоновом режиме. Строка таблицы состояния сеанса транспорта обновления путем вызова **ModifyStatusRow** при поставщика транспорта обеспечить соответствие это уведомление. 
    
NOTIFY_END_OUTBOUND 
  
> Исходящие операции необходимо прекратить для данного сеанса поставщика транспорта. Диспетчер очереди MAPI прекращает для вызова **SubmitMessage** и игнорирует флаг NOTIFY_READYTOSEND **SpoolerNotify** . При наличии исходящее сообщение отправлено в настоящее время, она не должна быть остановлена; Чтобы остановить доставки сообщения, используйте флаг NOTIFY_CANCEL_MESSAGE. Строка таблицы состояние для данного сеанса обновления путем вызова **ModifyStatusRow** до возвращения. Флаги NOTIFY_END_INBOUND и NOTIFY_BEGIN_OUTBOUND являются взаимоисключающими. 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> Работает аналогично для NOTIFY_END_INBOUND_FLUSH, но относится к исходящих сообщений. Флаг соответствующего состояния — STATUS_OUTBOUND_FLUSH.
    
 _lppvData_
  
> [out] Указатель на указатель на данные события. Дополнительные сведения о указывает, какие _lppvData_ параметр _lpulFlags_ см. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
## <a name="remarks"></a>Замечания

Диспетчер очереди MAPI вызывает метод **IXPLogon::TransportNotify** сигнала поставщика транспорта о событиях, для которых был запрошен уведомлений. Эти события включают запрос очереди MAPI для отмены передачи сообщений, начала или окончания операции входящих или исходящих транспорта и начала и окончания операции очистки очереди входящих или исходящих сообщений. 
  
Когда пользователь пытается отменить сообщение, в котором имеются ранее отложенные поставщика транспорта, диспетчер очереди MAPI вызывает **TransportNotify**, передав в NOTIFY_ABORT_DEFERRED и NOTIFY_CANCEL_MESSAGE флаги в _ulFlags_. Если диспетчер очереди MAPI выхода из системы и по-прежнему имеет сообщений в очереди, передается только NOTIFY_ABORT_DEFERRED в _ulFlags_ при вызове **TransportNotify**.
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик необходимо синхронизировать доступ к данным на этот вызов, так как диспетчер очереди MAPI можно было вызвать этот метод из другого потока выполнения или из процедуры для другое окно. Произойдет вероятнее всего, когда диспетчер очереди MAPI сигналы отмены сообщение, что поставщик транспорта начала отправки.
  
## <a name="see-also"></a>См. также

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) 
- [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) 
- [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) 
- [IXPLogon::EndMessage](ixplogon-endmessage.md) 
- [IXPLogon::Poll](ixplogon-poll.md)
- [IXPLogon::StartMessage](ixplogon-startmessage.md)
- [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [IXPLogon: IUnknown](ixplogoniunknown.md)

