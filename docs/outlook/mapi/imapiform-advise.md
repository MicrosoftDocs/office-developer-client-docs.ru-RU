---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b5347205e10b44d62a7e11cbe2f4179970f1bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808875"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**Относится к**: Outlook 
  
Регистрирует просмотра формы для уведомлений о событиях, которые влияют на форме.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Параметры

 _pAdvise_
  
> [in] Объект приемника для последующих уведомлений рекомендаций указатель в представление. 
    
 _pulConnection_
  
> [out] Указатель на ненулевое значение, представляющее регистрации успешного уведомлений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Регистрация прошла успешно.
    
E_OUTOFMEMORY 
  
> Регистрация не удалось выполнить из-за нехватки памяти.
    
## <a name="remarks"></a>Замечания

Средства просмотра формы вызов метода **IMAPIForm::Advise** формы для регистрации уведомлений при внесении изменений в форме. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Сохранить копию представления уведомить указателя приемника, переданной в параметре _pAdvise_ , которые можно использовать для вызова метода соответствующие [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) при возникновении события. Вызов представление уведомить метода [IUnknown::AddRef's](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) приемника для сохранения указателя до его отмены регистрации уведомлений. Содержимое для параметра _pulConnection_ значение ненулевое число. 
  
Многие формы реализовать вспомогательный объект для обработки регистрации и последующие уведомления о событиях. 
  
Дополнительные сведения о процессе уведомления в общем случае видеть [Уведомления о событии в MAPI](event-notification-in-mapi.md). 
  
Дополнительные сведения о уведомлений и формах можно [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>См. также



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Уведомление о событиях в MAPI](event-notification-in-mapi.md)
  
[Отправка и получение уведомлений о формах](sending-and-receiving-form-notifications.md)
