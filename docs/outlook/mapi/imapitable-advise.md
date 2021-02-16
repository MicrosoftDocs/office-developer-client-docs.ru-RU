---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418815"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Регистрирует объект приемника рекомендации для получения уведомлений об указанных событиях, влияющих на таблицу.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulEventMask_
  
> [in] Значение, указывающее тип события, которое будет создавать уведомление. Допустимо только следующее значение:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [in] Указатель на объект приемника рекомендации для получения последующих уведомлений. Этот рекомендуемый объект-тоник должен быть уже выделен.
    
 _lpulConnection_
  
> [out] Указатель на неживое значение, которое представляет успешную регистрацию уведомлений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация уведомлений успешно завершена.
    
MAPI_E_NO_SUPPORT 
  
> Реализация таблицы либо не поддерживает изменения строк и столбцов, либо не поддерживает уведомления.
    
## <a name="remarks"></a>Примечания

Используйте метод **IMAPITable::Advise,** чтобы зарегистрировать объект таблицы, реализованный в поставщике, для получения вызовов уведомлений. При изменении объекта таблицы поставщик проверяет, какой бит маски события был задан в параметре  _ulEventMask,_ и, таким образом, тип изменения. Если бит задан, поставщик вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемника рекомендации, заданного параметром  _lpAdviseSink,_ чтобы сообщить о событии. Данные, переданные в структуре уведомлений процедуре **OnNotify,** описывают событие. 
  
Вызов **OnNotify может** произойти во время вызова, который изменяет объект, или в любое следующее время. В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** может происходить в любом потоке. Чтобы сделать вызов **OnNotify,** который может произойти во время неоппортуны, более безопасным для обработки, поставщик должен использовать функцию [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Для предоставления уведомлений поставщик, реализующий advise, должен сохранить копию указателя на _объект-сигнал lpAdviseSink;_  для этого он вызывает метод **IUnknown::AddRef** для приемника рекомендации, чтобы поддерживать указатель на объект, пока регистрация уведомлений не будет отменена вызовом метода [IMAPITable::Unadvise.](imapitable-unadvise.md) Реализация **advise** должна назначить номер подключения регистрации уведомлений и вызвать **AddRef** на этом номере подключения, прежде чем возвращать его в _параметре lpulConnection._ Поставщики услуг могут освободить объект-сигнальный сигнал до отмены регистрации, но не должны освободить номер подключения, пока не будет вызвана служба ** Unadvise **. 
  
After a call to **Advise** has succeeded and before ** Unadvise ** has been called, clients must be prepared for the advise sink object to be released. Таким образом, клиент должен освободить  свой объект-тоник консультации после того, как advise возвращается, если он не имеет определенного долгосрочного использования для него. 
  
Из-за асинхронного поведения уведомлений реализации, меняя параметры столбцов таблицы, могут получать уведомления с информацией, упорядоченной в предыдущем порядке столбца. Например, строка таблицы может быть возвращена для сообщения, которое только что было удалено из контейнера. Такое уведомление отправляется, когда было внося изменение параметра столбца и отправлены сведения о нем, но представление таблицы уведомлений еще не было обновлено с этой информацией.
  
Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md) Конкретные сведения об уведомлении таблицы [см. в таблице уведомлений.](about-table-notifications.md) Сведения об использовании методов **IMAPISupport** для поддержки уведомлений см. в подразделе ["Поддержка уведомления о событии".](supporting-event-notification.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI использует метод **IMAPITable::Advise** для регистрации уведомлений, чтобы представление таблицы оставалась актуальным.  <br/> |
   
## <a name="see-also"></a>См. также



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

