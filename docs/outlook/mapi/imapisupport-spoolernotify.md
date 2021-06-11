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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сообщает шпалеру MAPI об изменении состояния или запросе на обслуживание. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмашка флагов, которая указывает тип уведомления. Поставщики транспорта могут устанавливать все флаги, за исключением NOTIFY_NEWMAIL_RECEIVED; только NOTIFY_NEWMAIL_RECEIVED и NOTIFY_READTOSEND допустимы для поставщиков хранения сообщений. Для параметра  _ulFlags_ допустимы следующие флаги: 
    
NOTIFY_CONFIG_CHANGE 
  
> Регистрирует запрос на изменение конфигурации поставщика транспорта. 
    
NOTIFY_CRITICAL_ERROR 
  
> В поставщике транспорта произошла невозвратная ошибка. Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR для вызовов поставщика транспорта используется параметр  _lpvData,_ эти флаги являются взаимоисключающими. 
    
NOTIFY_CRITSEC 
  
> Запрашивает критически важный раздел для поставщика транспорта. Параметр  _lpvData_ неопределяем и должен быть NULL. 
    
NOTIFY_NEWMAIL 
  
> Шпалер MAPI должен скачать все вновь полученные сообщения в следующее доступное время. Параметр  _lpvData_ не установлен и должен быть задан в NULL. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> В хранилище сообщений получено новое сообщение. Параметр  _lpvData_ указывает на структуру [NEWMAIL_NOTIFICATION,](newmail_notification.md) описываемую сообщение. Этот флаг используется для поставщиков магазинов сообщений, тесно соединых с поставщиками транспорта, и игнорируется, если поставщик магазина вошел в систему с MAPI_NO_MAIL флагом. 
    
NOTIFY_NONCRIT 
  
> Выпускает критический раздел, полученный при предыдущем вызове **в SpoolerNotify** с  _набором ulFlags_ для NOTIFY_CRITSEC. Параметр  _lpvData_ не установлен и должен быть задан в NULL. 
    
NOTIFY_READYTOSEND 
  
> Поставщик транспорта или магазина сообщений готов отправлять сообщения. Параметр  _lpvData_ не установлен и должен быть задан в NULL. 
    
NOTIFY_SENTDEFERRED 
  
> Ранее отложенное сообщение должно быть отправлено, и поставщик транспорта должен быть уведомлен, когда сообщение будет готово к отправке с помощью вызова метода [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md) Идентификатор входа отложенного сообщения содержится в [структуре SBinary,](sbinary.md) на которые указывает _lpvData._ Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR используют параметр  _lpvData,_ эти флаги являются взаимоисключающими. 
    
 _lpvData_
  
> [in] Указатель на связанные данные, применимые к уведомлению. Параметр  _lpvData_ указывает на допустимые данные только при задании следующих флагов _(lpvData_ является NULL, когда  _ulFlags_ задан для других типов уведомлений): 
    
|**_Параметр ulFlags_**|**_значение lpvData_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Сведения об ошибке.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Структура **NEWMAIL_NOTIFICATION,** которая содержит сведения о вновь доставленном сообщении.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Структура **SBinary,** которая содержит идентификатор входа отложенного сообщения.  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление было успешным.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::SpoolerNotify** реализован для объектов хранения сообщений и поставщиков транспорта. Эти поставщики **звонят в SpoolerNotify,** чтобы уведомить шпалер MAPI об изменении состояния или запросе на обслуживание. **SpoolerNotify** называется главным образом поставщиками транспорта и может быть вызвана в любое время во время сеанса. 
  
## <a name="notes-to-transport-providers"></a>Заметки поставщикам транспорта

Если вы изменили конфигурацию поставщика транспорта, позвоните **в SpoolerNotify** и установите  _ulFlags_ для NOTIFY_CONFIG_CHANGED. **SpoolerNotify** отвечает, вызывая [метод IXPLogon::AddressTypes](ixplogon-addresstypes.md) для запроса на изменение поддерживаемых типов адресов. 
  
Если вам нужен критический раздел для обеспечения непрерывной обработки, позвоните **в SpoolerNotify** с  _набором ulFlags_ для NOTIFY_CRITSEC. Настройка этого флага информирует шпалер MAPI о том, что он не должен вызывать методы [IXPLogon::Idle](ixplogon-idle.md) и [IXPLogon::P oll.](ixplogon-poll.md) Хотя у вас открыт критический раздел, MAPI_E_BUSY, когда называется метод [IMAPIStatus::ValidateState.](imapistatus-validatestate.md) После завершения критического раздела сделайте еще один вызов **в SpoolerNotify** с  _набором ulFlags_ для NOTIFY_NONCRIT. 
  
Например, если поставщик удаленного транспорта находится в процессе отправки сообщений, может потребоваться разрешить пользователю ввести номер телефона для установления удаленного подключения. Перед циклом в диалоговом окне необходимо объявить критический раздел. Когда пользователь закрывает диалоговое окно, завершая процедуру диалогового окна, необходимо освободить критический раздел.
  
При задаче  _ulFlags_ NOTIFY_CRITICAL_ERROR, пуллер MAPI не вызывает поставщика, кроме как освободить его. Если вы вызываете **SpoolerNotify** с набором NOTIFY_CRITICAL_ERROR из [IXPLogon::StartMessage](ixplogon-startmessage.md) или [IXPLogon::SubmitMessage,](ixplogon-submitmessage.md) вернись с соответствующим значением ошибки из **startMessage** или ** SubmitMessage ** call immediately after the **SpoolerNotify** call. 
  
Если поставщик транспорта оправился от условия, которое ранее привело к сбойу, позвоните **в SpoolerNotify** с  _набором ulFlags_ для NOTIFY_READYTOSEND. Этот флаг указывает, что поставщик снова готов обрабатывать сообщения. 
  
## <a name="notes-to-message-store-providers"></a>Заметки поставщикам магазина сообщений

Вызывай **SpoolerNotify** NOTIFY_READYTOSEND, перед тем как сделать первый звонок в [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) в **IMessage::SubmitMessage.** Этот вызов **в SpoolerNotify** должен быть выполнен только один раз за сеанс. 
  
Если поставщик магазина сообщений тесно соединимся с поставщиком транспорта, и вы звоните **в SpoolerNotify** с набором  _ulFlags_ NOTIFY_NEWMAIL_RECEIVED, пульпер MAPI открывает новое сообщение и начинает обработку новой функции крюка сообщения. После завершения обработки шпалер MAPI вызывает [метод IMsgStore::NotifyNewMail,](imsgstore-notifynewmail.md) чтобы сообщить вам о новом сообщении. 
  
Дополнительные сведения о вызове **SpoolerNotify** см. в следующих темах:
  
- [Реализация метода FlushQueues](implementing-the-flushqueues-method.md)
    
- [Взаимодействие со Spooler MAPI](interacting-with-the-mapi-spooler.md)
    
- [Модель приема сообщений](message-reception-model.md)
    
## <a name="see-also"></a>См. также



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

