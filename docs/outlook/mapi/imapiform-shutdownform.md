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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Закрывает форму.
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>Parameters

 _ulSaveOptions_
  
> [in] Значение, которое контролирует, как и сохраняются ли данные в форме до закрытия формы. Можно установить один из следующих флагов:
    
SAVEOPTS_NOSAVE 
  
> Данные формы не следует сохранить.
    
SAVEOPTS_PROMPTSAVE 
  
> Пользователю необходимо получить запрос на сохранение всех измененных данных в форме.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Данные формы должны быть сохранены, если они изменились с момента последнего сохранения. Если пользовательский интерфейс не отображается, форма может дополнительно перейти к использованию функций для SAVEOPTS_NOSAVE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма была закрыта.
    
E_UNEXPECTED 
  
> Форма уже была закрыта предварительным вызовом **в ShutdownForm.**
    
## <a name="remarks"></a>Примечания

Зрители формы звонят **по методу IMAPIForm::ShutdownForm,** чтобы закрыть форму. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Выполните следующие задачи в реализации **ShutdownForm:**
  
1. Убедитесь, что зритель еще не вызвал **ShutdownForm,** и E_UNEXPECTED если он есть. Хотя это маловероятно, необходимо проверить.
    
2. Позвоните по методу [IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) чтобы хранилище формы и любых внутренних структур данных оставалось доступным до завершения обработки. 
    
3. Определите, есть ли какие-либо неопределяемые изменения в данных формы. Сохранение неопровергаемой информации в соответствии с тем, как задан параметр _ulSaveOptions,_ вызывав метод [IMAPIMessageSite::SaveMessage.](imapimessagesite-savemessage.md) 
    
4. Уничтожите окно пользовательского интерфейса формы.
    
5. Освободите объекты веб-сайтов сообщений и сообщений формы, назвав их [методы IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) 
    
6. Уведомить всех зарегистрированных зрителей о ожидаемом закрытии, позвонив по [их методам IMAPIViewAdviseSink::OnShutdown.](imapiviewadvisesink-onshutdown.md) 
    
7. Позвоните по методу [IMAPIViewContext::SetAdviseSink,](imapiviewcontext-setadvisesink.md) чтобы отменить регистрацию формы для уведомления, установив указатель на раковину рекомендации на **нуль**.
    
8. Вызов [функции MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить память для свойств формы. 
    
9. Вызовите метод **IUnknown::Release** формы, который соответствует **вызову AddRef,** выполненного на шаге 2. 
    
10. Возвращение S_OK.
    
> [!NOTE]
> После завершения этих действий единственными допустимыми методами объекта формы, которые можно назвать, являются методы интерфейса [IUnknown.](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Когда **ShutdownForm** возвращается, независимо от того, возвращается ли ошибка, отпустите форму, назвав ее **метод IUnknown::Release.** Вы можете безопасно игнорировать ошибки, возвращаемые **ShutdownForm.**
  
## <a name="see-also"></a>См. также



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

