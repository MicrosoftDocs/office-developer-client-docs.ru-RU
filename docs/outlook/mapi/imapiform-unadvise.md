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
ms.openlocfilehash: 826863e30ae39d3c8d523bd2dff84731bcf16971
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808905"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**Относится к**: Outlook 
  
Отменяет регистрацию для уведомлений с помощью средства просмотра формы, ранее установленные путем вызова [IMAPIForm::Advise](imapiform-advise.md).
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulConnection_
  
> [in] Число подключений, определяющее регистрации уведомлений, чтобы отменить.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Регистрация отменена.
    
E_INVALIDARG 
  
> Номер соединения, переданной в параметре _ulConnection_ не представляет допустимое регистрации. 
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IMAPIForm::Unadvise** для отмены регистрации для уведомлений, сначала установить путем вызова метода **IMAPIForm::Advise** . 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Отменить указатель, содержат представление формы просмотра уведомить приемник путем вызова метода [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) . Как правило, называется **выпуска** во время вызова **Unadvise** . Тем не менее если другой поток находится в процессе вызова одного из методов [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) для представления уведомить приемник, задержки звонка **выпуска** до возвращения методом **IMAPIViewAdviseSink** . 
  
## <a name="see-also"></a>См. также



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

