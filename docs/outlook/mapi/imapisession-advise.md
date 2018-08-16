---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45033ab924dcf443e9d231b3a7b4348119758935
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809069"
---
# <a name="imapisessionadvise"></a>IMAPISession::Advise

  
  
**Относится к**: Outlook 
  
Регистрация для получения уведомлений о указанного события, которые влияют на сеанс.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи адресной книги или объекта хранилища сообщение о том, какие следует создавать уведомления или значение NULL, это означает, что клиент регистрируется для получения уведомлений о событиях, которые влияют на только на сеанс. 
    
 _ulEventMask_
  
> [in] Маска значения, которые указывают на тип события уведомлений, которые клиент заинтересована в и должно быть включено в регистрации. Если _lpEntryID_ имеет значение NULL, MAPI автоматически регистрирует клиента для событий критическая ошибка, влияющие на только на сеанс. Если _lpEntryID_ указывает на идентификатор записи, для параметра _ulEventMask_ допустимы следующие значения: 
    
fnevCriticalError 
  
> Регистрирует уведомлений о серьезной ошибки, например недостаточно памяти.
    
fnevExtended 
  
> Регистрирует для уведомлений о событиях, характерные для определенного адресной книги или сообщения поставщик хранилища и о сеансе завершение работы.
    
fnevNewMail 
  
> Регистрирует уведомлений о появлении нового сообщения. 
    
fnevObjectCreated 
  
> Регистрирует уведомлений о создании нового объекта.
    
fnevObjectCopied
  
> Регистрирует для уведомлений об объекте копируются.
    
fnevObjectDeleted
  
> Регистрирует для уведомлений об объекте удаляются.
    
fnevObjectModified
  
> Регистрирует для уведомлений об объекте изменяется.
    
fnevObjectMoved
  
> Регистрирует для уведомлений об объекте происходит перемещение.
    
fnevSearchComplete
  
> Регистрирует для уведомлений о завершении операции поиска.
    
 _lpAdviseSink_
  
> [in] Указатель на объект приемника уведомлений для последующих уведомлений. Этот объект приемника уведомлений должно уже была распределена.
    
 _lpulConnection_
  
> [out] Указатель на ненулевое число, представляющее соединение между вызывающего абонента уведомить объект приемника и сеанса.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Регистрация прошла успешно.
    
MAPI_E_INVALID_ENTRYID 
  
> Идентификатор записи, на который указывает _lpEntryID_ не представляет идентификатор допустимый записи. 
    
MAPI_E_NO_SUPPORT 
  
> Поставщик услуг, ответственный за запись идентификатор, на который указывает _lpEntryID_ не поддерживает тип события, указанного в параметре _ulEventMask_ или не поддерживает уведомления. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Идентификатор записи, на который указывает _lpEntryID_ не может справиться с любой из поставщиков услуг в профиле. 
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::Advise** устанавливает объект приемника, сеанса и (необязательно) поставщика услуг 's рекомендаций соединение между вызывающего абонента. Это подключение используется для отправки уведомлений на приемник уведомлений, когда один или несколько указанных в параметре _ulEventMask_ событиями на объект, на который указывает _lpEntryID_. Если _lpEntryID_ имеет значение NULL, целевой объект сеанса и отправлять уведомления только для критические ошибки и расширенные события. 
  
При _lpEntryID_ указывает идентификатор записей, MAPI вызывает метод **уведомлений** объекта входа в систему, к которой относится к поставщику услуг ответственность. Например если _lpEntryID_ указывает идентификатор записи в список рассылки, MAPI вызывает метод [IABLogon::Advise](iablogon-advise.md) поставщик соответствующие адресной книги. 
  
Чтобы отправить уведомление, поставщиком услуг или MAPI вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник зарегистрированных уведомлений. Один из параметров в **OnNotify**, уведомления о структуре, содержит сведения, описывающие определенных событий.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

На компьютерах, поддерживающих многопоточной среде вызов **OnNotify** могут также создаваться в любом потоке в любое время. Если вам требуется Software assurance возникновения уведомления только в конкретный момент времени в определенном потоке, вызовите функцию [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) для создания объекта приемник уведомлений, передайте методу **уведомлений** . 
  
Чтобы определить, когда вышел клиента, зарегистрируйте уведомления в ваш поставщик услуг, вызвав **уведомлений** с _lpEntryID_ значение NULL, а _cbEntryID_ значение 0. В случае выхода из системы, вы получите уведомление о fnevExtended. 
  
После вызова **уведомлений** прошло успешно, и перед [IMAPISession::Unadvise](imapisession-unadvise.md) вызван для отмены регистрации, release объекта приемник уведомлений при отсутствии определенных длительного использования для него. 
  
Общие сведения о процессе уведомления в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md). 
  
Дополнительные сведения об обработке уведомлений можно [Обработки уведомлений](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |Mfcmapi (en) использует метод **IMAPISession::Advise** для регистрации уведомлений от сеанса.  <br/> |
   
## <a name="see-also"></a>См. также



[IABLogon::Advise](iablogon-advise.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Unadvise](imapisession-unadvise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Уведомление о событиях в MAPI](event-notification-in-mapi.md)
