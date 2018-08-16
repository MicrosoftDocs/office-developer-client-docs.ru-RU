---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6a315cef8263f7e241a815a0f054dc3174d88fa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809366"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**Относится к**: Outlook 
  
Регистрация для получения уведомлений о указанного события, которые влияют на хранилище сообщений.
  
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
  
> [in] Указатель на идентификатор записи папки или сообщения о уведомления, которое будет создан, или **значение null**. Если _lpEntryID_ имеет значение NULL, **уведомлений** регистрирует уведомлений на хранилище всего сообщения. 
    
 _ulEventMask_
  
> [in] Маска значения, которые указывают на тип события уведомлений, вызывающего заинтересована в и должно быть включено в регистрации. Нет соответствующих структура [уведомления](notification.md) , связанные с каждым типом событий, в котором содержатся сведения о событии. Ниже приведены допустимые значения для параметра _ulEventMask_ : 
    
 _fnevCriticalError_
  
> Регистрирует уведомлений о серьезной ошибки, например недостаточно памяти.
    
 _fnevExtended_
  
> Поставщик хранилища регистрирует для уведомлений о событиях, характерные для определенного сообщения.
    
 _fnevNewMail_
  
> Регистрирует уведомлений о появлении нового сообщения. 
    
 _fnevObjectCreated_
  
> Регистрирует уведомлений о создания новой папки или сообщения.
    
 _fnevObjectCopied_
  
> Регистрирует уведомлений о папке или сообщения от копирования.
    
 _fnevObjectDeleted_
  
> Регистрирует уведомлений о папке или удаления сообщений.
    
 _fnevObjectModified_
  
> Регистрирует уведомлений о папке или изменяемого сообщения.
    
 _fnevObjectMoved_
  
> Регистрирует уведомлений о папке или перемещения сообщений.
    
 _fnevSearchComplete_
  
> Регистрирует для уведомлений о завершении операции поиска.
    
 _lpAdviseSink_
  
> [in] Указатель на объект приемника уведомлений для последующих уведомлений. Этот объект приемника уведомлений должно уже была распределена.
    
 _lpulConnection_
  
> [out] Указатель на ненулевое число, представляющее соединение между вызывающего абонента уведомить объект приемника и сеанса. 
    
 _lpAdviseSink_
  
> [in] Указатель на объект приемника уведомлений для последующих уведомлений. Этот объект приемника уведомлений должно уже была распределена. 
    
 _lpulConnection_
  
> [out] Указатель на подключение ненулевое число, представляющее соединение между вызывающего абонента уведомить объект приемника и хранилища сообщений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Регистрация прошла успешно.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик хранения сообщения не поддерживает регистрации для уведомлений через хранилища сообщений.
    
## <a name="remarks"></a>Замечания

Метод **IMsgStore::Advise** устанавливает соединение между вызывающего абонента уведомить объектом приемника и хранилище сообщений или объекта в хранилище сообщений. Это подключение используется для отправки уведомлений на приемник уведомлений, когда один или несколько событий, как указано в параметре _ulEventMask_ , возникающих в объект источника уведомлений. При параметр _lpEntryID_ указывает идентификатор записей, источник уведомлений — это объект идентификатором этой записи. Когда _lpEntryID_ имеет значение NULL, источник уведомлений — это хранилище сообщений. 
  
Чтобы отправить уведомление, MAPI или поставщика хранилища сообщений вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник зарегистрированных уведомлений. Один из параметров в **OnNotify**, уведомления о структуре, содержит сведения, описывающие определенных событий.
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Может поддерживать уведомлений с помощью или без помощи MAPI. MAPI имеет три метода объекта поддержки за помощь реализации уведомлений поставщиков услуг: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)и [IMAPISupport::Notify](imapisupport-notify.md). Если вы решите использовать методы поддержки MAPI, вызовите **подписки на** при вызове метода **уведомлений** и освобождать указатель _lpAdviseSink_ . 
  
Если для поддержки уведомлений самостоятельно, вызовите метод [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) приемник уведомлений, представленное параметром _lpAdviseSink_ сохранить копию этого указателя. Ведение эту копию, пока не будет вызван метод [IMsgStore::Unadvise](imsgstore-unadvise.md) для отмены регистрации. 
  
Независимо от того, как вы поддерживаете уведомлений нумерации ненулевое подключения для регистрации уведомлений и вернуть его в параметре _lpulConnection_ . Не release этот номер подключения, пока **Unadvise** вызван и завершения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

На компьютерах, поддерживающих многопоточной среде вызов **OnNotify** могут также создаваться в любом потоке в любое время. Если вы должны быть уверенным, уведомления о возникновении только в конкретный момент времени в определенном потоке, вызовите функцию [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) для создания объекта приемник уведомлений, передаваемых в **уведомлений**. 
  
После вызова метода **уведомлений** завершено успешно и прежде **Unadvise** вызван для отмены регистрации, подготовить для объекта приемник уведомлений нужно освободить. Объект приемника уведомлений освобождать после **уведомлений** возвращает при отсутствии определенных длительного использования для него. 
  
Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md). 
  
Дополнительные сведения об обработке уведомлений можно [Обработки уведомлений](handling-notifications.md). 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnNotificationsOn  <br/> |Mfcmapi (en) использует метод **IMsgStore::Advise** для регистрации уведомлений на хранилище всего сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[�����������](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
