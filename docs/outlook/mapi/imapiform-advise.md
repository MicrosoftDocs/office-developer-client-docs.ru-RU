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
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329486"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Регистрирует просмотр формы для уведомлений о событиях, влияющих на форму.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Параметры

 _pAdvise_
  
> [in] Указатель на объект приемника представления рекомендует получать последующие уведомления. 
    
 _pulConnection_
  
> [out] Указатель на неимякое значение, которое представляет успешную регистрацию уведомлений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация прошла успешно.
    
E_OUTOFMEMORY 
  
> Регистрация не была успешной из-за нехватки памяти.
    
## <a name="remarks"></a>Примечания

Посетители форм звонят **методу IMAPIForm::Advise** формы, чтобы зарегистрировать уведомление при внесении изменений в форму. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Храните копию указателя приемника рекомендации представления, переданную в  _параметре pAdvise,_ чтобы использовать его для вызова соответствующего метода [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) при событии. Вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) приемника представлений, чтобы сохранить указатель до отмены регистрации уведомления. Установите для содержимого параметра  _pulConnection_ ненулевую нулевую. 
  
Многие формы реализуют объект-помощник для обработки регистрации и последующего уведомления о событиях. 
  
Дополнительные сведения о процессе уведомлений в целом см. в [уведомлении о событии в MAPI.](event-notification-in-mapi.md) 
  
Дополнительные сведения об уведомлениях и формах см. в сведениях об отправке и [получении уведомлений о формах.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>См. также



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Уведомление о событии в MAPI](event-notification-in-mapi.md)
  
[Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md)

