---
title: имапиформшутдовнформ
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

 _улсавеоптионс_
  
> возврата Значение, определяющее способ сохранения данных формы перед ее закрытием. Можно задать один из следующих флагов:
    
SAVEOPTS_NOSAVE 
  
> Данные формы не должны быть сохранены.
    
SAVEOPTS_PROMPTSAVE 
  
> Пользователю должно быть предложено сохранить все измененные данные в форме.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Данные формы необходимо сохранить, если они были изменены с момента последнего сохранения. Если пользовательский интерфейс не отображается, форму можно дополнительно переключить на использование функций для параметра SAVEOPTS_NOSAVE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма была закрыта.
    
E_UNEXPECTED 
  
> Форма уже закрыта при предыдущем вызове **шутдовнформ**.
    
## <a name="remarks"></a>Примечания

Средства просмотра форм вызывают метод **имапиформ:: шутдовнформ** для закрытия формы. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Выполните следующие задачи в реализации **шутдовнформ**:
  
1. Убедитесь, что средство просмотра еще не вызвало **шутдовнформ**, и возвращайте E_UNEXPECTED, если он есть. Хотя это маловероятно, необходимо проверить.
    
2. Вызовите метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) формы, чтобы хранилище для формы и все внутренние структуры данных оставались доступными до завершения обработки. 
    
3. Определите, нет ли несохраненных изменений данных формы. Сохраните несохраненные данные в соответствии с определением параметра _улсавеоптионс_ , вызвав метод [Имапимессажесите:: савемессаже](imapimessagesite-savemessage.md) . 
    
4. Удалите окно пользовательского интерфейса формы.
    
5. Освободите объекты-сообщения и сообщения формы, вызвав их методы [выпусков IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . 
    
6. Сообщите обо всех зарегистрированных средствах просмотра ожидания завершения, вызвав их методы [имапивиевадвисесинк:: OnShutdown](imapiviewadvisesink-onshutdown.md) . 
    
7. Вызовите метод [имапивиевконтекст:: сетадвисесинк](imapiviewcontext-setadvisesink.md) , чтобы отменить регистрацию формы для уведомления, задав для указателя приемника уведомлений **значение NULL**.
    
8. Вызовите функцию [мапифрибуффер](mapifreebuffer.md) , чтобы освободить память для свойств формы. 
    
9. Вызовите метод **IUnknown:: Release** формы, который соответствует вызову **AddRef** , выполненному на этапе 2. 
    
10. Возврат S_OK.
    
> [!NOTE]
> После выполнения этих действий единственные допустимые методы в объекте Form, которые могут быть вызваны, — это из интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Когда **шутдовнформ** возвращает значение, независимо от того, возвращает ли ошибка, освобождайте форму, вызвав ее метод **IUnknown:: Release** . Вы можете спокойно игнорировать все ошибки, возвращенные **шутдовнформ**.
  
## <a name="see-also"></a>См. также



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

