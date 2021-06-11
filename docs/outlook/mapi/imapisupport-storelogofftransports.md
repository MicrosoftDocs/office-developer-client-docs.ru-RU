---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421384"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запрашивает упорядоченный выпуск магазина сообщений.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in, out] Битмаска флагов, которые контролируют процесс входа в хранилище сообщений. На входе все флаги для этого параметра являются взаимоисключающими; на один вызов можно установить только один из следующих флагов:
    
LOGOFF_ABORT 
  
> Все действия поставщика транспорта для этого магазина должны быть остановлены перед входом в систему. Управление возвращается клиенту после того, как действие остановлено, а пульпер MAPI выключил магазин. Если какие-либо транспортные действия происходят, журнал не происходит, и не происходит никаких изменений в пулере MAPI или поведении поставщика транспорта. Если в настоящее время нет действий, пульпер MAPI освобождает магазин. 
    
LOGOFF_NO_WAIT 
  
> Пульпер MAPI должен освободить хранилище и вернуть управление клиенту сразу после того, как будет отправлена вся готовая к отправлению почта. Если в хранилище сообщений имеется почтовый ящик по умолчанию, любое в процессе сообщения получается, а затем дополнительный прием отключен. 
    
LOGOFF_ORDERLY 
  
> Пульпер MAPI должен освободить магазин и вернуть управление клиенту сразу после завершения обработки всех ожидающих сообщений. Новые сообщения не должны обрабатываться. 
    
LOGOFF_PURGE 
  
> Работает так же, как LOGOFF_NO_WAIT флаг. Флаг LOGOFF_PURGE возвращает управление вызываемой после завершения. 
    
LOGOFF_QUIET 
  
> Журнал не должен происходить, если какие-либо действия поставщика транспорта происходят. Тип действия, который происходит, возвращается в виде флага на выходе.
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> Журнал может завершиться. Все ресурсы, связанные с хранилищем, были освобождены, а объект признан недействительным. Шпалер MAPI выполнил или выполнит все запросы. В этой точке должен быть вызван только метод **IUnknown::Release** магазина сообщений. 
    
LOGOFF_INBOUND 
  
> В настоящее время сообщение приходит в магазин от одного или более поставщиков транспорта. 
    
LOGOFF_OUTBOUND 
  
> В настоящее время сообщение отправляется из магазина одним или более поставщиками транспорта. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> В настоящее время сообщения в исходящие очереди для магазина.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Процедура входа прошла успешно.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::StoreLogoffTransports** реализован для объектов поддержки поставщиков сообщений. Поставщики магазинов сообщений звонят **в StoreLogoffTransports,** чтобы предоставить клиентские приложениям определенный контроль над тем, как MAPI обрабатывает деятельность поставщика транспорта по мере закрытия магазина сообщений. 
  
Если другой процесс должен открыть магазин для того же профиля, MAPI игнорирует вызов **в StoreLogoffTransports** и возвращает флаг LOGOFF_COMPLETE в _параметре lpulFlags._ 
  
Поведение поставщика магазина после возврата из **StoreLogoffTransports** должно основываться на значении  _lpulFlags,_ которое указывает состояние системы и передает инструкции клиента по поведению журналов. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **StoreLogoffTransports** обычно называется методом [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) поставщика магазина. Однако его можно также назвать **методом IUnknown::Release** магазина сообщений. Реализуйте **метод выпуска** вашего магазина сообщений, чтобы проверить, был ли звонок в **StoreLogoffTransports.** Если вызов не произошел, позвоните **в StoreLogoffTransports** с LOGOFF_ABORT флагом. 
  
Параметр  _lpulFlags задан_ флагу, который указывает, как клиент требует закрыть хранилище сообщений. Определите соответствующий параметр  _для ulFlags_ на основе параметра соответствующего параметра в вызове **в StoreLogoff**. То есть, если клиент вызвал метод **StoreLogoff** с набором  _ulFlags_ LOGOFF_ORDERLY, необходимо вызвать **StoreLogoffTransports** с  _набором ulFlags_ для LOGOFF_ORDERLY. 
  
Дополнительные сведения о процессе входа в хранилище сообщений см. в [журнале Shutting Down a Message Store Provider.](shutting-down-a-message-store-provider.md)
  
## <a name="see-also"></a>См. также



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

