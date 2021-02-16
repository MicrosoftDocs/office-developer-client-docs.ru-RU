---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317313"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Регистрирует объект у поставщика store сообщений для уведомлений об изменениях в хранилище сообщений. Затем хранилище сообщений будет отправлять уведомления об изменениях зарегистрированного объекта.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Размер идентификатора записи в вайтах, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи объекта, о котором должны быть созданы уведомления. Этот объект может быть папкой, сообщением или любым другим объектом в хранилище сообщений. Кроме того, если MAPI задает для параметра  _cbEntryID_ 0 и передает **null** для  _lpEntryID,_ то в окну рекомендации будут отправляться уведомления об изменениях во всем хранилище сообщений.
    
 _ulEventMask_
  
> [in] Маска событий типов событий уведомлений, происходящих для объекта, для которого MAPI будет создавать уведомления. Маска фильтрует определенные случаи. Каждый тип события имеет связанную с ним структуру, которая содержит дополнительные сведения о событии. В следующей таблице перечислены возможные типы событий, а также соответствующие структуры.
    
|**Тип события notification**|**Соответствующая структура**|
|:-----|:-----|
|fnevCriticalError  <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|fnevNewMail  <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|fnevObjectCreated  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectDeleted  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectModified  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectCopied  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectMoved  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevSearchComplete  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevStatusObjectModified  <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in] Указатель на объект-консультант, который будет вызван при событии объекта сеанса, о том, какое уведомление запрашивается. Этот рекомендуемый объект-тоник уже должен существовать.
    
 _lpulConnection_
  
> [out] Указатель на переменную, которая после успешного возврата содержит номер подключения для регистрации уведомления. Номер подключения должен быть неzero.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_SUPPORT 
  
> Операция не поддерживается MAPI или одним или более поставщиками услуг.
    
## <a name="remarks"></a>Примечания

Поставщики store сообщений реализуют метод **IMSLogon::Advise** для регистрации объекта для методов вызова уведомлений. При изменении заданного объекта поставщик проверяет, какой бит маски события был задан в параметре  _ulEventMask,_ и, следовательно, тип изменения. Если бит задан, поставщик вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемника рекомендации, заданного параметром  _lpAdviseSink,_ чтобы сообщить о событии. Данные, переданные в структуре уведомлений процедуре **OnNotify,** описывают событие. 
  
Вызов **OnNotify может** произойти во время вызова, который изменяет объект, или в любое время. В системах, поддерживаюх несколько потоков выполнения, вызов **OnNotify** может происходить в любом потоке. Для безопасной обработки вызова **OnNotify,** который может произойти во время неоппортуна, клиентские приложения должны использовать функцию [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Для предоставления уведомлений поставщику  store сообщений, который реализует advise, необходимо сохранить копию указателя на объект-замещение _lpAdviseSink;_ Для этого поставщик вызывает метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для приемника консультаций, чтобы сохранить указатель на объект, пока регистрация уведомления не будет отменена с помощью вызова метода [IMSLogon::Unadvise.](imslogon-unadvise.md) Реализация **advise** должна назначить номер подключения регистрации уведомлений и вызвать **AddRef** по этому номеру подключения, прежде чем возвращать его в _параметре lpulConnection._ Перед отменой регистрации поставщики услуг могут освободить объект-тонконсультант, но не должны отпускать номер подключения, пока не будет вызвана служба **Unadvise.** 
  
После успешного  вызова "Консультация" и перед вызовом **Unadvise** поставщики должны быть готовы к тому, чтобы объект-сигнальный сигнал был отпущен. Таким образом, поставщик должен освободить объект-сигнальный сигнал после возврата advise, если он не имеет определенного долгосрочного использования для него.  
  
Дополнительные сведения о процессе уведомления см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md) 
  
## <a name="see-also"></a>См. также



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[�����������](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

