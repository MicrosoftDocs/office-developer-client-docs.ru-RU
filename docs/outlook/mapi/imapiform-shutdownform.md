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
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329479"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Закрывает форму.
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>Параметры

 _ulSaveOptions_
  
> [in] Значение, которое управляет тем, как данные в форме сохраняются или сохраняются до закрытия формы. Можно установить один из следующих флагов:
    
SAVEOPTS_NOSAVE 
  
> Данные формы не должны быть сохранены.
    
SAVEOPTS_PROMPTSAVE 
  
> Пользователю должно быть предложено сохранить все измененные данные в форме.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Данные формы следует сохранять, если они изменились с момента последнего сохранения. Если пользовательский интерфейс не отображается, форма может при необходимости переключиться на использование функций для SAVEOPTS_NOSAVE интерфейса.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма была закрыта.
    
E_UNEXPECTED 
  
> Форма уже была закрыта при предыдущем вызове **ShutdownForm.**
    
## <a name="remarks"></a>Примечания

С помощью метода **IMAPIForm::ShutdownForm** можно вызвать метод IMAPIForm, чтобы закрыть форму. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Выполните следующие задачи в реализации **ShutdownForm:**
  
1. Убедитесь, что просмотр еще не вызвал **ShutdownForm,** и E_UNEXPECTED, если он есть. Хотя это маловероятно, вам следует проверить.
    
2. Вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) формы, чтобы хранилище формы и любых внутренних структур данных оставалось доступным до завершения обработки. 
    
3. Определите, есть ли какие-либо несовеченные изменения в данных формы. Сохраните несохранения данных в соответствии с тем, как параметр  _ulSaveOptions_ задан путем вызова метода [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) вашего просмотра. 
    
4. Уничтожите окно пользовательского интерфейса формы.
    
5. Освободите объекты сайта сообщений и сообщений формы, вызывая их методы [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) 
    
6. Уведомите всех зарегистрированных посетителей об ожидающих завершениях работы, вызывая их методы [IMAPIViewAdviseSink::OnShutdown.](imapiviewadvisesink-onshutdown.md) 
    
7. Вызовите метод [IMAPIViewContext::SetAdviseSink,](imapiviewcontext-setadvisesink.md) чтобы отменить регистрацию формы для уведомления, установив для указателя приемника рекомендации **null.**
    
8. Вызовите [функцию MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить память для свойств формы. 
    
9. Вызовите метод **IUnknown::Release** формы, который соответствует вызову **AddRef,** выполненного на шаге 2. 
    
10. Возврат S_OK.
    
> [!NOTE]
> После завершения этих действий единственными допустимыми методами объекта формы, которые могут быть вызваны, являются методы из интерфейса [IUnknown.](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Когда **ShutdownForm** возвращает ошибку, отпустите форму, вызывая метод **IUnknown::Release.** Вы можете игнорировать все ошибки, возвращенные **ShutdownForm.**
  
## <a name="see-also"></a>См. также



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

