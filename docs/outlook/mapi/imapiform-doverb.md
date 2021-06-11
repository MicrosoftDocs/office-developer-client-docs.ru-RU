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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запрашивает, чтобы форма выполняла любые задачи, которые она связывает с определенным глаголом.
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a>Parameters

 _iVerb_
  
> [in] Число, связанное с одним из глаголов формы.
    
 _lpViewContext_
  
> [in] Указатель на объект контекста представления. Параметр  _lpViewContext может_ быть **null**.
    
 _hwndParent_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемая этим методом. Параметр  _hwndParent должен_ быть **null,** если диалоговое окно или окно не являются модальными. 
    
 _lprcPosRect_
  
> [in] Указатель на структуру [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) Win32, которая содержит размер и положение окна формы. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Глагол успешно вызывался.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> Глагол, представленный  _параметром iVerb,_ действителен, но форма не может выполнять операции, связанные с ним в настоящее время. 
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по **методу IMAPIForm::D oVerb,** чтобы запросить, чтобы форма выполняла задачи, которые она связывает с каждым глаголом, поддерживаемым формой. 
  
Каждый из поддерживаемых глаголов идентифицирован по числовому значению, передается **в DoVerb** в _параметре iVerb._ Типичные реализации **DoVerb содержат** заявление **коммутатора,** которое проверяет значения, допустимые для  _параметра iVerb_ для формы. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если зритель формы указывает контекст представления в параметре _lpViewContext,_ используйте его в реализации **DoVerb** вместо контекста представления, переданного в предыдущий вызов методу [IMAPIForm::SetViewContext.](imapiform-setviewcontext.md) Внести все необходимые изменения в внутренние структуры данных и не сохранять контекст представления. 
  
Выполните следующие задачи в реализации **DoVerb:** 
  
- Выполните любой код, необходимый для определенного глагола, связанного с параметром _iVerb._ 
    
- При необходимости восстановим исходный контекст представления.
    
- Если неизвестный номер глагола был передан, верни MAPI_E_NO_SUPPORT. В противном случае возвращаем результат, основанный на успешности или сбое любого выполненного глагола.
    
- Закрой форму. После завершения вызова **DoVerb** вы всегда несете ответственность за закрытие формы. 
    
Некоторые глаголы, например Print, должны быть модальными в отношении вызова **DoVerb,** то есть указанная операция должна быть завершена до возвращения вызова **DoVerb.** 
  
Чтобы получить **структуру RECT,** используемую в окне формы, позвоните в [функцию GetWindowRect.](https://msdn.microsoft.com/library/ms633519) 
  
Не сохраните ручку в параметре  _hwndParent,_ так как, хотя она обычно остается допустимой до завершения **DoVerb,** она может быть уничтожена сразу после возвращения вызова.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно заставить немодальные глаголы выступать в качестве модальных глаголов, указав _lpViewContext_ на реализацию контекста представления, которая возвращает флаг VCSTATUS_MODAL из метода [IMAPIViewContext::GetViewStatus.](imapiviewcontext-getviewstatus.md) 
  
Дополнительные сведения о глаголах в MAPI см. в [виде глаголов.](form-verbs.md) Дополнительные сведения о том, как обрабатываются глаголы в OLE, см. в [OLE и Передаче данных.](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI использует **метод IMAPIForm::D oVerb** для вызова глагола в форме.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Глаголы формы](form-verbs.md)

