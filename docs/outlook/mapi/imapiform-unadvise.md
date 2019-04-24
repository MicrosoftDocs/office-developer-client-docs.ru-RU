---
title: Имапиформунадвисе
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
  
ОтМеняет регистрацию для уведомлений с помощью средства просмотра форм, ранее установленного вызовом [имапиформ:: Advise](imapiform-advise.md).
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Параметры

 _Улконнектион_
  
> возврата Номер подключения, указывающий на отмену регистрации уведомления.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация отменена.
    
E_INVALIDARG 
  
> Номер подключения, переданный в параметре _улконнектион_ , не представляет допустимую регистрацию. 
    
## <a name="remarks"></a>Комментарии

В средствах просмотра форм вызывается метод **имапиформ:: unadvise** для отмены регистрации уведомлений, которые были установлены при вызове метода **Имапиформ:: Advise** . 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Отмените указатель, который вы удерживаете, в приемник уведомлений просмотра формы, вызвав его метод [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . Как правило, **выпуск** вызывается во время вызова метода unadvise. **** Тем не менее, если другой поток находится в процессе вызова одного из методов [имапивиевадвисесинк](imapiviewadvisesinkiunknown.md) для приемника уведомлений о просмотре, задерживает вызов **освобождения** до возвращения метода **имапивиевадвисесинк** . 
  
## <a name="see-also"></a>См. также



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

