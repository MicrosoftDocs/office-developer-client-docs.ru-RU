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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирует просмотра форм для уведомлений о событиях, влияющих на форму.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Parameters

 _pAdvise_
  
> [in] Указатель на представление советует объекту раковины получать последующие уведомления. 
    
 _pulConnection_
  
> [вышел] Указатель на значение nonzero, которое представляет успешную регистрацию уведомлений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация прошла успешно.
    
E_OUTOFMEMORY 
  
> Регистрация была неудачной из-за недостаточной памяти.
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по методу **IMAPIForm:::Advise** формы, чтобы зарегистрироваться для уведомления при внесении изменений в форму. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Храните копию представления, сообщайте указатель раковины, переданный в  _параметре pAdvise,_ чтобы вы могли использовать его для вызова соответствующего метода [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) при событии. Вызов представления советую [методу IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) сохранить указатель до отмены регистрации уведомлений. Установите содержимое параметра  _pulConnection_ на номер nonzero. 
  
Во многих формах реализован объект помощника для обработки регистрации и последующего уведомления о событиях. 
  
Дополнительные сведения о процессе уведомления в целом см. в сообщении [о событиях в MAPI.](event-notification-in-mapi.md) 
  
Дополнительные сведения об уведомлениях и формах см. в рублях [Отправка и получение уведомлений о форме.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>См. также



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Уведомление о событиях в MAPI](event-notification-in-mapi.md)
  
[Отправка и получение уведомлений о форме](sending-and-receiving-form-notifications.md)

