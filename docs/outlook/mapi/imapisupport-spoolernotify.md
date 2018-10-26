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
ms.openlocfilehash: a2837e5470729ae3cdd0b83e17d0342620c986e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592117"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Уведомление об изменении состояния или запрос на обслуживание диспетчер очереди MAPI. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, которое указывает тип уведомления. Поставщики транспорта можно задать все флажки кроме NOTIFY_NEWMAIL_RECEIVED; только NOTIFY_NEWMAIL_RECEIVED и NOTIFY_READTOSEND являются допустимыми для поставщиков хранилища сообщений. Для параметра _ulFlags_ допустимы следующие флажки: 
    
NOTIFY_CONFIG_CHANGE 
  
> Регистрация запроса для изменения конфигурации поставщика транспорта. 
    
NOTIFY_CRITICAL_ERROR 
  
> Неустранимая ошибка поставщика транспорта. Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR параметр _lpvData_ используется для вызовов, поставщика транспорта, эти флаги являются взаимоисключающими. 
    
NOTIFY_CRITSEC 
  
> Запрашивает критический раздел для поставщика транспорта. Параметр _lpvData_ не определен и должен иметь значение NULL. 
    
NOTIFY_NEWMAIL 
  
> Диспетчер очереди MAPI следует загрузить любые полученные новые сообщения на следующего доступного времени. Параметр _lpvData_ не определен и необходимо указать значение NULL. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Новое сообщение было получено, в хранилище сообщений. Параметр _lpvData_ указывает на структуру [NEWMAIL_NOTIFICATION](newmail_notification.md) , описывающую сообщения. Этот флаг используется для поставщиков хранилища сообщений, которые тесно связаны с поставщиками транспорта и игнорируется, если поставщик хранения вошел в систему с установленным флагом MAPI_NO_MAIL. 
    
NOTIFY_NONCRIT 
  
> Освобождает критический раздел, полученное с предыдущего вызова **SpoolerNotify** с _ulFlags_ , задайте значение NOTIFY_CRITSEC. Параметр _lpvData_ не определен и необходимо указать значение NULL. 
    
NOTIFY_READYTOSEND 
  
> Хранилище поставщика транспорта или сообщения готова для отправки сообщений. Параметр _lpvData_ не определен и необходимо указать значение NULL. 
    
NOTIFY_SENTDEFERRED 
  
> Теперь будет отправлено сообщение ранее отложенные и поставщика транспорта уведомляться, когда сообщение будет готов для доставки с помощью вызова метода [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . Идентификатор записи отложенные сообщения содержится в структуру [SBinary](sbinary.md) , на который указывает _lpvData_. Так как NOTIFY_SENTDEFERRED и NOTIFY_CRITICAL_ERROR использовать параметр _lpvData_ , эти флаги являются взаимоисключающими. 
    
 _lpvData_
  
> [in] Указатель на связанных данных, которые применяются к уведомление. Параметр _lpvData_ указывает на допустимый данные только в том случае, если заданы следующие флаги (_lpvData_ имеет значение NULL при _ulFlags_ задано значение других типов уведомлений): 
    
|**параметр _ulFlags_**|**значение _lpvData_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Сведения об ошибке.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Структура **NEWMAIL_NOTIFICATION** , содержащая сведения о вновь доставлено сообщение.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Структура **SBinary** , содержащая идентификатор записи отложенные сообщения.  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::SpoolerNotify** применяется для сообщения хранения и передачи объекты поддержки поставщика. Эти поставщики вызов **SpoolerNotify** для уведомления об изменении состояния или запрос на обслуживание диспетчер очереди MAPI. **SpoolerNotify** называется главным образом поставщиками транспорта и может быть вызван в любое время во время сеанса. 
  
## <a name="notes-to-transport-providers"></a>Примечания для поставщиками транспорта

При изменении конфигурации поставщика транспорта вызова **SpoolerNotify** и установите _ulFlags_ NOTIFY_CONFIG_CHANGED. **SpoolerNotify** отвечает путем вызова метода [IXPLogon::AddressTypes](ixplogon-addresstypes.md) для запроса внести изменения в типы поддерживаемых адресов. 
  
При необходимости критического раздела для обеспечения бесперебойный обработки звонков **SpoolerNotify** с _ulFlags_ , задайте значение NOTIFY_CRITSEC. Этот флаг установлен информирует диспетчер очереди MAPI, что она не вызывайте методы [IXPLogon::Idle](ixplogon-idle.md) и [IXPLogon::Poll](ixplogon-poll.md) . При наличии критического раздела откройте возврата MAPI_E_BUSY при вызове метода [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . По окончании критический раздел, сделайте другой вызов **SpoolerNotify** с _ulFlags_ , задайте значение NOTIFY_NONCRIT. 
  
К примеру Если ваш поставщик удаленного транспорта в процессе отправку сообщения, может потребоваться разрешает пользователю указать номер телефона для установления подключения к удаленному. Прежде чем цикле процедуру диалогового окна следует объявить критический раздел. Когда пользователь закрывает диалоговое окно, завершение процедуру диалогового окна, необходимо разблокировать критический раздел.
  
Если _ulFlags_ NOTIFY_CRITICAL_ERROR, диспетчер очереди MAPI не производит дальнейшие вызовы поставщика за исключением до выпуска. При вызове **SpoolerNotify** с NOTIFY_CRITICAL_ERROR задать с помощью методов [IXPLogon::StartMessage](ixplogon-startmessage.md) или [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) возврата со значением соответствующие ошибки из **StartMessage** или ** SubmitMessage ** звонков сразу же после вызова **SpoolerNotify** . 
  
Если ваш поставщик транспорта восстановлен из условие, ранее привел к сбою, вызовите **SpoolerNotify** с _ulFlags_ , задайте значение NOTIFY_READYTOSEND. Этот флаг указывает, что поставщик снова готовы обрабатывать сообщения. 
  
## <a name="notes-to-message-store-providers"></a>Примечания для поставщиков хранилища сообщений

Вызовите **SpoolerNotify**, передав флаг NOTIFY_READYTOSEND _ulFlags_, прежде чем принять первый звонок на [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) в **IMessage::SubmitMessage**. Этот вызов **SpoolerNotify** должно выполняться только один раз за сеанс. 
  
Если поставщик хранилища сообщений тесно связаны с транспорта поставщика и Вы вызовите **SpoolerNotify** _ulFlags_ имеет значение NOTIFY_NEWMAIL_RECEIVED, диспетчер очереди MAPI откроется новое сообщение и начинает обработку новой функции обработки сообщений. После завершения обработки очереди MAPI вызывает метод [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) , чтобы сообщить о новое сообщение. 
  
Дополнительные сведения о вызове **SpoolerNotify**видеть какие-либо из следующих разделов:
  
- [Реализация метода FlushQueues](implementing-the-flushqueues-method.md)
    
- [Взаимодействие с очередью MAPI](interacting-with-the-mapi-spooler.md)
    
- [Модель приема сообщений](message-reception-model.md)
    
## <a name="see-also"></a>См. также



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

