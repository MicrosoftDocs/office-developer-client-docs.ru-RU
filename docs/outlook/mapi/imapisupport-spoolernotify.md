---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423771"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сообщает пулу MAPI об изменении состояния или запросе на обслуживание. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая указывает тип уведомления. Поставщики транспорта могут устанавливать все флаги, кроме NOTIFY_NEWMAIL_RECEIVED; только NOTIFY_NEWMAIL_RECEIVED и NOTIFY_READTOSEND допустимы для поставщиков store сообщений. Для параметра  _ulFlags_ допустимы следующие флаги: 
    
NOTIFY_CONFIG_CHANGE 
  
> Регистрирует запрос на изменение конфигурации поставщика транспорта. 
    
NOTIFY_CRITICAL_ERROR 
  
> Произошла неу обнаруженная ошибка для поставщика транспорта. Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR использовать параметр  _lpvData_ для вызовов поставщика транспорта, эти флаги являются взаимоисключающими. 
    
NOTIFY_CRITSEC 
  
> Запрашивает критический раздел для поставщика транспорта. Параметр  _lpvData_ не задан и должен иметь NULL. 
    
NOTIFY_NEWMAIL 
  
> The MAPI spooler should download any newly received messages at the next available time. Параметр  _lpvData_ не задан и должен иметь NULL. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> В хранилище сообщений получено новое сообщение. Параметр  _lpvData указывает_ на [NEWMAIL_NOTIFICATION,](newmail_notification.md) которая описывает сообщение. Этот флаг используется для поставщиков хранения сообщений, которые тесно совмещение с поставщиками транспорта, и игнорируется, если поставщик магазина вошел в систему с установленным MAPI_NO_MAIL флагом. 
    
NOTIFY_NONCRIT 
  
> Освобождает критический раздел, полученный при предыдущем вызове **SpoolerNotify,** для  _ulFlags_ установлено значение NOTIFY_CRITSEC. Параметр  _lpvData_ не задан и должен иметь NULL. 
    
NOTIFY_READYTOSEND 
  
> Поставщик транспорта или хранения сообщений готов к отправке сообщений. Параметр  _lpvData_ не задан и должен иметь NULL. 
    
NOTIFY_SENTDEFERRED 
  
> Теперь необходимо отправить ранее отложенное сообщение, и поставщик транспорта должен быть уведомлен о готовности сообщения к доставке с помощью вызова метода [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md) Идентификатор записи отложенного сообщения содержится в структуре [SBinary,](sbinary.md) на который указывает _lpvData._ Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR использовать параметр  _lpvData,_ эти флаги являются взаимоисключающими. 
    
 _lpvData_
  
> [in] Указатель на связанные данные, применимые к уведомлению. Параметр  _lpvData_ указывает на допустимые данные, только если заданы следующие флаги (_lpvData_ имеет NULL, если  _для ulFlags_ заданы другие типы уведомлений): 
    
|**_Параметр ulFlags_**|**_Значение lpvData_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Сведения об ошибке.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Структура **NEWMAIL_NOTIFICATION,** которая содержит сведения о только что доставленном сообщении.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Структура **SBinary,** которая содержит идентификатор записи отложенного сообщения.  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::SpoolerNotify реализован** для объектов поддержки службы хранения сообщений и поставщика транспорта. Эти поставщики **вызывали SpoolerNotify,** чтобы уведомить пультер MAPI об изменении состояния или запросе на обслуживание. **SpoolerNotify** в основном вызван поставщиками транспорта и может быть вызван в любое время во время сеанса. 
  
## <a name="notes-to-transport-providers"></a>Примечания для поставщиков транспорта

Если вы изменили конфигурацию поставщика транспорта, вызовите **SpoolerNotify** и установите  _для ulFlags_ NOTIFY_CONFIG_CHANGED. **В ответ SpoolerNotify** вызывает метод [IXPLogon::AddressTypes](ixplogon-addresstypes.md) для запроса на изменение поддерживаемых типов адресов. 
  
Если требуется критический раздел для непрерывной обработки, вызовите **SpoolerNotify** с  _ulFlags,_ установленным NOTIFY_CRITSEC. Установка этого флага сообщает пулу MAPI о том, что он не должен вызывать методы [IXPLogon::Idle](ixplogon-idle.md) и [IXPLogon::P oll.](ixplogon-poll.md) При открытом критическом разделе MAPI_E_BUSY каждый раз, когда будет вызван метод [IMAPIStatus::ValidateState.](imapistatus-validatestate.md) Завершив критический раздел, еще раз вызовите **SpoolerNotify,** где для  _ulFlags_ установлено значение NOTIFY_NONCRIT. 
  
Например, если ваш удаленный поставщик транспорта загружает сообщения, может потребоваться разрешить пользователю вводить телефонный номер, чтобы установить удаленное подключение. Перед циклом процедуры в диалоговом окне объявите критический раздел. Когда пользователь закрывает диалоговое окно, завершая процедуру диалоговых окна, необходимо освободить критический раздел.
  
Если вы установите  _для ulFlags_ NOTIFY_CRITICAL_ERROR, пулер MAPI не будет больше звонить поставщику, кроме как освободить его. If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or ** SubmitMessage ** call immediately after the **SpoolerNotify** call. 
  
Если ваш поставщик транспорта восстановился после условия, которое ранее вызывло сбой, вызовите **SpoolerNotify,** для  _ulFlags_ установлено NOTIFY_READYTOSEND. Этот флаг указывает, что поставщик снова готов к обработке сообщений. 
  
## <a name="notes-to-message-store-providers"></a>Примечания для поставщиков store сообщений

Вызовите **SpoolerNotify,** передав флаг NOTIFY_READYTOSEND в _ulFlags_ перед первым вызовом [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) в **IMessage::SubmitMessage.** Этот вызов **SpoolerNotify** должен быть выполнен только один раз для каждого сеанса. 
  
Если поставщик службы хранения сообщений тесно совмещение с поставщиком транспорта и вызовите **SpoolerNotify** с  _ulFlags,_ задав для него NOTIFY_NEWMAIL_RECEIVED, пулер MAPI откроет новое сообщение и начнет обработку новой функции обработки сообщения. После завершения обработки пулер MAPI вызывает метод [IMsgStore::NotifyNewMail,](imsgstore-notifynewmail.md) чтобы сообщить вам о новом сообщении. 
  
Дополнительные сведения о вызове **SpoolerNotify** см. в следующих темах:
  
- [Реализация метода FlushQueues](implementing-the-flushqueues-method.md)
    
- [Взаимодействие с пулером MAPI](interacting-with-the-mapi-spooler.md)
    
- [Модель приема сообщений](message-reception-model.md)
    
## <a name="see-also"></a>См. также



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

