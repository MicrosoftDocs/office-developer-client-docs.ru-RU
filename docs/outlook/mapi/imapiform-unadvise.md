---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329472"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отменяет регистрацию уведомлений с предварительно установленным средством просмотра форм по вызову [IMAPIForm:::Advise](imapiform-advise.md).
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in] Номер подключения, который определяет отмену регистрации уведомлений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация была отменена.
    
E_INVALIDARG 
  
> Номер подключения, переданный в  _параметре ulConnection,_ не является допустимой регистрацией. 
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по методу **IMAPIForm::Unadvise,** чтобы отменить регистрацию для уведомления, которое они впервые установили, позвонив по методу **IMAPIForm::Advise.** 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Откажитесь от указателя, удерживаемого в представлении просмотра формы, посоветуйте удалить его [метод IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) Как правило, **выпуск** вызываем во время вызова **Unadvise.** Однако, если другой поток находится в процессе вызова одного из методов [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) для представления, сообщите об этом, отозвать вызов выпуска до возвращения метода **IMAPIViewAdviseSink.**  
  
## <a name="see-also"></a>См. также



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

