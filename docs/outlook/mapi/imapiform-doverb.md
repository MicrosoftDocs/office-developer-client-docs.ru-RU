---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329463"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Запрашивает выполнение формы любых задач, которые она связывает с определенной глаголом.
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a>Параметры

 _iVerb_
  
> [in] Номер, связанный с одной из глаголов формы.
    
 _lpViewContext_
  
> [in] Указатель на объект контекста представления. Параметр _lpViewContext_ может иметь **null.**
    
 _hwndParent_
  
> [in] Handle to the parent window of any dialog boxes or windows this method displays. Параметр  _hwndParent должен_ иметь **null,** если диалоговое окно или окно не является модальным. 
    
 _lprcPosRect_
  
> [in] Указатель на структуру [Win32 RECT,](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) содержаную размер и положение окна формы. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Глагол успешно вызван.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> Глагол, представленный параметром  _iVerb,_ действителен, но форма не может выполнять связанные с ней операции. 
    
## <a name="remarks"></a>Примечания

Посетители форм звонят **методу IMAPIForm::D oVerb,** чтобы запрашивать выполнение формы задач, которые она связывает с каждым глаголом, поддерживаемым формой. 
  
Каждая из поддерживаемых глаголов определена числом, переданным **в DoVerb** в _параметре iVerb._ Типичные реализации **DoVerb содержат** коммутатор, который проверяет значения, допустимые для  _параметра iVerb_ для формы. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если просмотр формы указывает контекст представления в параметре _lpViewContext,_ используйте его в реализации **DoVerb** вместо контекста представления, переданного в более ранних вызовах метода [IMAPIForm::SetViewContext.](imapiform-setviewcontext.md) Внести все необходимые изменения во внутренние структуры данных и не сохранять контекст представления. 
  
Выполните следующие задачи в реализации **DoVerb:** 
  
- Выполните любой код, необходимый для конкретной команды, связанной с параметром _iVerb._ 
    
- При необходимости восстановим исходный контекст представления.
    
- Если передан неизвестный номер команды, вернетесь MAPI_E_NO_SUPPORT. В противном случае возвращается результат на основе успешности или сбоя выполненной команды.
    
- Закроем форму. Вы всегда несете ответственность за то, чтобы закрыть форму после завершения вызова **DoVerb.** 
    
Некоторые команды, например Print, должны быть модальными по отношению к вызову **DoVerb,** то есть указанная операция должна быть завершена до возврата вызова **DoVerb.** 
  
Чтобы получить **структуру RECT,** используемую окном формы, вызовите [функцию GetWindowRect.](https://msdn.microsoft.com/library/ms633519) 
  
Не следует сохранять окне в параметре  _hwndParent,_ так как, хотя он обычно остается действительным до завершения **doVerb,** он может быть уничтожен сразу после возврата вызова.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете сделать так, чтобы не модальные команды выступают в качестве модальных глаголов, указав _lpViewContext_ на реализацию контекста представления, которая возвращает флаг VCSTATUS_MODAL из метода [IMAPIViewContext::GetViewStatus.](imapiviewcontext-getviewstatus.md) 
  
Дополнительные сведения о глаголах в MAPI [см. в поддоменах Form Verbs.](form-verbs.md) Дополнительные сведения об обработке глаголов в OLE см. в [OLE и передаче данных.](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI использует метод **IMAPIForm::D oVerb** для вызова команды в форме.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Команды формы](form-verbs.md)

