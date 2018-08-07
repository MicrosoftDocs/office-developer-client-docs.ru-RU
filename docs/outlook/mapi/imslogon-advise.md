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
ms.openlocfilehash: 87be00bce55fabda6271b472a9e5c446aaf8054a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809410"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**Относится к**: Outlook 
  
Регистрирует объект поставщика хранилища сообщений для уведомлений об изменениях в хранилище сообщений. Хранилище сообщений будет отправлять уведомления об изменениях зарегистрированных объект.
  
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
  
> [in] Размер в байтах, идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи о том, какие следует создавать уведомления объекта. Этот объект можно папки, сообщение или любого другого объекта в хранилище сообщений. Кроме того Если MAPI задается параметр _cbEntryID_ 0 и передает **значение null** для _lpEntryID_, приемник уведомлений предоставляет уведомления об изменениях в хранилище всего сообщения.
    
 _ulEventMask_
  
> [in] Маски события типов событий уведомлений для объекта, о том, какие MAPI будет создавать уведомления. Маска фильтр определенных случаев. Каждый тип события имеет структуру, связанные с ним, который содержит дополнительные сведения о событии. В следующей таблице перечислены типы возможных событий вместе с их соответствующие структуры.
    
|**Тип события уведомления**|**Соответствующий структуры**|
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
  
> [in] Указатель на объект приемника уведомлений будет вызываться при возникновении события для объекта сеанса, о том, какие запросил уведомление. Этот объект приемника уведомлений должны уже существовать.
    
 _lpulConnection_
  
> [out] Указатель на переменную, которая после успешного возврата содержит номер подключения для регистрации уведомлений. Номер подключения должен быть отличное от нуля.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_SUPPORT 
  
> Операция не поддерживается с MAPI или с одного или нескольких поставщиков услуг.
    
## <a name="remarks"></a>Замечания

Поставщики хранилища сообщений реализуйте метод **IMSLogon::Advise** для регистрации объекта для обратных вызовов уведомлений. При каждом изменении на указанный объект, поставщик проверяет маска какие события было задано с помощью параметра _ulEventMask_ и, следовательно, какой тип изменения произошло. Если немного, поставщик вызывает метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для объекта приемник уведомлений, указанное с помощью параметра _lpAdviseSink_ сообщение о событии. Данные, передаваемые в структуре уведомлений в подпрограмму **OnNotify** описание события. 
  
Вызов **OnNotify** может возникнуть во время звонка, которое изменяет объект или в любой момент позже. На компьютерах, поддерживающих многопоточной среде вызов **OnNotify** может выполняться на любой поток. Безопасно обработка вызова **OnNotify** , который может произойти в неподходящее время, клиентское приложение должно использовать функцию [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Для предоставления уведомлений, объект приемника; рекомендаций поставщика хранилища сообщений, который реализует **уведомлений** необходимо сохранить копию указатель _lpAdviseSink_ для этого поставщика вызывает метод [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) для приемник уведомлений на обслуживание указателя на объект до отмены регистрации уведомлений с помощью вызова метода [IMSLogon::Unadvise](imslogon-unadvise.md) . Реализации **уведомлений** следует присвоить номер подключения для регистрации уведомлений и вызов **AddRef** на этот номер подключения до возвращения в параметре _lpulConnection_ . Поставщиков услуг можно освободить объект приемника уведомлений перед отменяется регистрация, но они не должны освобождать номер подключения до вызова **Unadvise** . 
  
После вызова **уведомлений** прошло успешно, и перед **Unadvise** вызван поставщиков должен быть подготовлен для объекта приемник уведомлений нужно освободить. Таким образом поставщика освобождать возвращается объект приемника уведомлений после возвращает **уведомлений** , если оно не имеет определенного длительного использования для него. 
  
Дополнительные сведения о процессе уведомления содержатся в разделе [Уведомление о событии в MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>См. также



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[�����������](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

