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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает контекст представления для формы. 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>Parameters

 _pViewContext_
  
> [in] Указатель на новый контекст представления формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Контекст представления был успешно за установлен.
    
## <a name="remarks"></a>Примечания

Зрители формы называют **метод IMAPIForm::SetViewContext,** чтобы установить определенный контекст представления формы как текущий. Форма может иметь только один контекст представления одновременно. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Большинство серверов форм **реализуют SetViewContext** с помощью следующего алгоритма: 
  
- Если контекст представления уже существует для формы, отмените регистрацию формы, назвав метод [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) с **null** в параметре  _pmnvs,_ а затем позвоните в метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) контекста представления, чтобы усугубит его количество ссылок. 
    
- Если новый контекст представления не является **null,** позвоните **в службу IMAPIViewContext::SetAdviseSink** с помощью параметра  _pViewContext_ для настройка нового представления. 
    
- Если новый контекст представления не является **null,** позвоните по методу [IMAPIViewContext::GetViewStatus,](imapiviewcontext-getviewstatus.md) чтобы определить, какие флаги состояния установлены. 
    
- Если новый контекст представления не является **null,** сберегайте его и вызывайте его метод [IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) чтобы прибавить количество ссылок. 
    
- Обновление всех элементов пользовательского интерфейса, зависят от контекста представления. 
    
В зависимости от флагов состояния, возвращенных **из IMAPIViewContext::GetViewStatus,** **SetViewContext** также может выполнять другие действия. Например, если VCSTATUS_NEXT и VCSTATUS_PREV флаги возвращаются, **SetViewContext** может включить кнопки **Next** и **Previous** для нового контекста представления. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI использует **метод IMAPIForm::SetViewContext** для набора контекста представления MFCMAPI в форме перед отображением формы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

