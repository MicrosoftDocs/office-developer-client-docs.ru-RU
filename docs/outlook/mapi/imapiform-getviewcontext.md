---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430905"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает текущий контекст представления для формы. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Parameters

 _ppViewContext_
  
> [вышел] Указатель на указатель на контекст представления формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Текущий контекст представления формы был успешно возвращен. 
    
S_FALSE 
  
> Контекст представления формы не существует.
    
## <a name="remarks"></a>Примечания

Зрители формы звонят **в GetViewContext,** чтобы получить указатель на контекст представления, установленный в предыдущем вызове [в IMAPIForm::SetViewContext](imapiform-setviewcontext.md). Если предварительного вызова в **SetViewContext** не было, **GetViewContext** задает  _ppViewContext_ в NULL. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Скопируйте указатель контекста представления формы в указатель, переданный вызываемой формой в _параметре ppViewContext._ Если в форме нет контекста представления, установите  _ppViewContext_ в NULL. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI использует **метод IMAPIForm::GetViewContext,** чтобы проверить, имеет ли форма контекст представления.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

