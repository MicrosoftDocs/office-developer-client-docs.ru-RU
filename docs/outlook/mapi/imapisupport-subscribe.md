---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6658f1c4bcfaf7557d9b53c5e70d87e124475580
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809202"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**Относится к**: Outlook 
  
Регистрирует приемника уведомления для получения уведомлений через MAPI.
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Параметры

 _lpKey_
  
> [in] Указатель на ключ уведомлений, представляющий объект источника уведомлений. Параметр _lpKey_ не может быть NULL. 
    
 _ulEventMask_
  
> [in] Маска значения, которые указывают на тип события уведомлений, вызывающего заинтересована в и должно быть включено в регистрации. Допустимыми являются следующие значения:
    
 _fnevCriticalError_
  
> Регистрирует уведомлений о серьезной ошибки, например недостаточно памяти.
    
 _fnevExtended_
  
> Поставщик хранилища регистрирует для уведомлений о событиях, характерные для определенного адресной книги или сообщения.
    
 _fnevNewMail_
  
> Регистрирует уведомлений о появлении нового сообщения. 
    
 _fnevObjectCreated_
  
> Регистрирует уведомлений о создании нового объекта.
    
 _fnevObjectCopied_
  
> Регистрирует для уведомлений об объекте копируются.
    
 _fnevObjectDeleted_
  
> Регистрирует для уведомлений об объекте удаляются.
    
 _fnevObjectModified_
  
> Регистрирует для уведомлений об объекте изменяется.
    
 _fnevObjectMoved_
  
> Регистрирует для уведомлений об объекте происходит перемещение.
    
 _fnevSearchComplete_
  
> Регистрирует для уведомлений о завершении операции поиска.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее, как выполняется уведомлений. Можно задать следующий флаг:
    
NOTIFY_SYNC 
  
> Когда вызывающего вызывает метод [IMAPISupport::Notify](imapisupport-notify.md) для создания уведомлений для этой приемник уведомлений, **Уведомлять** должна вызывать все необходимые приемников уведомлений перед возвращением. Если этот флаг не установлен, уведомление является асинхронным и обратных вызовов в очереди для процессов, которые подписаны и при этих процессов регулировка процессора. 
    
 _lpAdviseSink_
  
> [in] Указатель на объект приемник уведомлений. 
    
 _lpulConnection_
  
> [out] Указатель на подключение ненулевое число, представляющее регистрации.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Уведомление о регистрации прошла успешно.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::Subscribe** применяется для всех объектов поддержки поставщика службы. **Подписки на** вызова поставщиков услуг от одного из своих **уведомлений** методы, позволяющие MAPI для управления уведомления. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы использовать методы поддержки MAPI для уведомлений, создание ключа источника уведомлений, будет создан объект о уведомления, которое. Значение ключа должно быть уникальным и должны быть легко ключа при каждом изменении объекта. 
  
MAPI использует уведомления ключ для поиска функций обратного вызова, зарегистрированных в функцию [HrAllocAdviseSink](hrallocadvisesink.md) для соответствующий источник уведомлений. Передайте этот ключ **IMAPISupport::Notify** каждый раз, когда должны получать уведомления о соответствующий источник уведомлений. 
  
Флаг NOTIFY_SYNC влияет на операции последующие вызовы **уведомлений**. При установке NOTIFY_SYNC **Уведомлять** не возвращается до завершения отправки все необходимые уведомления. Если NOTIFY_SYNC не задано, **Уведомлять** работает асинхронно, возможно, с возвращаемым перед все уведомления было отправлено. 
  
## <a name="see-also"></a>См. также



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�����������](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

