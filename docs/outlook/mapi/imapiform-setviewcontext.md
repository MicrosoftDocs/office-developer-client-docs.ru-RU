---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350948"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Устанавливает контекст представления для формы. 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>Параметры

 _pViewContext_
  
> [in] Указатель на новый контекст представления для формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Контекст представления успешно установлен.
    
## <a name="remarks"></a>Примечания

Посетители форм **звонят методу IMAPIForm::SetViewContext,** чтобы установить определенный контекст представления формы как текущий. Одновременно форма может иметь только один контекст представления. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Большинство серверов форм **реализуют SetViewContext** с помощью следующего алгоритма: 
  
- Если контекст представления уже существует для формы, отмените регистрацию формы, вызывая метод [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) с нулью в параметре _pmnvs,_ а затем вызовите метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) контекста представления, чтобы понижить количество ссылок.  
    
- Если новый контекст представления не имеет **null,** вызовите **IMAPIViewContext::SetAdviseSink** с помощью параметра  _pViewContext_ для того, чтобы настроить новый окн. 
    
- Если новый контекст представления не имеет **null,** вызовите метод [IMAPIViewContext::GetViewStatus,](imapiviewcontext-getviewstatus.md) чтобы определить, какие флаги состояния были установлены. 
    
- Если новый контекст представления не имеет **null,** храните его и вызовите его метод [IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) чтобы повысьть количество ссылок. 
    
- Обновление всех элементов пользовательского интерфейса, которые зависят от контекста представления. 
    
В зависимости от флагов состояния, возвращаемого **из IMAPIViewContext::GetViewStatus,** **SetViewContext** также может выполнять другие действия. Например, если VCSTATUS_NEXT и VCSTATUS_PREV флаги, **SetViewContext** может включить кнопки **"Далее"** и "Назад" для нового контекста представления.  
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI использует метод **IMAPIForm::SetViewContext,** чтобы настроить контекст представления MFCMAPI в форме перед отображением формы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

