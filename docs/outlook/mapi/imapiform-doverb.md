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
ms.openlocfilehash: 9ea44c9ba75390f06ff12ddeed0c7b652538e07d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808915"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**Относится к**: Outlook 
  
Запросы, формы выполнить все задачи связывается с определенным команды.
  
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
  
> [in] Номер, связанный с одной из команд формы.
    
 _lpViewContext_
  
> [in] Указатель на объект контекста представления. Параметр _lpViewContext_ может иметь **значение null**.
    
 _hwndParent_
  
> [in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод. Значение параметра _hwndParent_ должно быть **значение null,** Если диалоговое окно или окно не является модальным. 
    
 _lprcPosRect_
  
> [in] Указатель на объект Win32 структуры [Прямоугольник](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) , содержащий размер и положение окна формы. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Команда успешно вызова.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> Команда, представленное параметром _iVerb_ является допустимым, но формы не могут выполнять операции, связанные с ним в настоящее время. 
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IMAPIForm::DoVerb** для запроса, что форма выполнения задач, связывается с каждой командой, которая поддерживает формы. 
  
Числовое значение, переданной в **DoVerb** с помощью параметра _iVerb_ отмечаются каждого из поддерживаемых команд. Типичная реализация **DoVerb** содержат операторе **switch** для проверки значения, подходящие для параметра _iVerb_ для формы. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если средство просмотра формы с помощью параметра _lpViewContext_ указывает контекст представления, используйте его в реализации **DoVerb** вместо контекст представления, переданные в более ранних вызова метода [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) . Внесите необходимые изменения, необходимые для вашего внутренних структур данных и не следует сохранять контекст представления. 
  
В реализации **DoVerb** выполните следующие задачи: 
  
- Выполнение код не требуется для конкретной команды, который связан с параметром _iVerb_ . 
    
- При необходимости восстановите исходное контекст представления.
    
- Если был передан на номер Неизвестный команды, возвратите MAPI_E_NO_SUPPORT. В противном случае возвращает результат на основании успешное или неудачное выполнены необходимые команды.
    
- Закройте форму. Отвечает всегда для закрытия формы после завершения вызова **DoVerb** . 
    
Некоторые действия, такие как печать, должны быть модальными по отношению к **DoVerb** звонок, то есть, указанный операция должна быть выполнена до возвращения вызова **DoVerb** . 
  
Для получения структуры **Прямоугольник** , используемых окно формы, вызовите функцию [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) . 
  
Не сохранять дескриптор в параметре _hwndParent_ , потому что несмотря на то, что обычно действует до завершения **DoVerb**, его можно удалять сразу же после возврата звонка.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно выполнять команды немодальную выступать в качестве модальные окна команд, указав _lpViewContext_ для реализации контекст представления, которое возвращает флаг VCSTATUS_MODAL из метода [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) . 
  
Дополнительные сведения о команд в MAPI можно [Команд формы](form-verbs.md). Дополнительные сведения об обработке команд в OLE можно [OLE и передачи данных](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |Mfcmapi (en) использует метод **IMAPIForm::DoVerb** для вызова команды на форме.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Команды форм](form-verbs.md)

