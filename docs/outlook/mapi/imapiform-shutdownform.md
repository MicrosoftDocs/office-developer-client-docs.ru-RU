---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 49ed8669a5496524917c15ac86e4a13060931057
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578572"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Закрывает форму.
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>Параметры

 _ulSaveOptions_
  
> [in] Значение, определяющее, как или ли данные в форме сохраняется до закрытия формы. Можно установить один из следующих флагов.
    
SAVEOPTS_NOSAVE 
  
> Не следует сохранить данные формы.
    
SAVEOPTS_PROMPTSAVE 
  
> Пользователь должен запрос на сохранение любых измененных данных в форме.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Необходимо сохранить данные формы, если он был изменен с момента последнего сохранения. Если пользовательский интерфейс не отображается, формы при необходимости можно переключиться на использование функциональные возможности для параметра SAVEOPTS_NOSAVE.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Форма была закрыта.
    
ЗНАЧЕНИЕ E_UNEXPECTED 
  
> Форма уже была закрыта во время предыдущего вызова **ShutdownForm**.
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IMAPIForm::ShutdownForm** для закрытия формы. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

В реализации **ShutdownForm**выполните следующие задачи:
  
1. Проверьте, что средство просмотра еще не звонил **ShutdownForm**и возвратить значение E_UNEXPECTED, если она есть. Хотя это маловероятно, следует проверить.
    
2. Вызов метода [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) формы, чтобы хранилища, используемого в форме и все внутренние структуры данных доступны только после завершения обработки. 
    
3. Определите, есть ли несохраненные изменения к данным формы. Сохраните несохраненные данные в соответствии с как задать параметр _ulSaveOptions_ путем вызова метода [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) пользователя. 
    
4. Уничтожает окно интерфейса пользователя формы.
    
5. Освобождение сообщения и объекты сайта сообщение формы, вызвав их [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) методы. 
    
6. Сообщить все зарегистрированные пользователи, просматривающие ожидание завершения работы, вызвав их [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) методы. 
    
7. Вызовите метод [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) для отмены регистрации формы для уведомлений, задав указателя приемника уведомлений значение **null**.
    
8. Вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить память для свойств формы. 
    
9. Вызовите метод **функции IUnknown::Release** формы, соответствующие **AddRef** вызов, выполненный на шаге 2. 
    
10. Возвращает значение S_OK.
    
> [!NOTE]
> После выполнения этих действий допустимо только методы объекта формы, который может вызывать — это списки из интерфейс [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При возврате **ShutdownForm** , независимо от того, является ли он возвращает ошибку, release формы путем вызова метода **функции IUnknown::Release** . Можно игнорировать любые ошибки, возвращаемые **ShutdownForm**.
  
## <a name="see-also"></a>См. также



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

