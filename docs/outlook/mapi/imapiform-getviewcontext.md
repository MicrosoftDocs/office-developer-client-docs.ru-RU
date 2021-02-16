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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает текущий контекст представления для формы. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Параметры

 _ppViewContext_
  
> [out] Указатель на указатель на контекст представления формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Был успешно возвращен текущий контекст представления формы. 
    
S_FALSE 
  
> Контекст представления для формы не существует.
    
## <a name="remarks"></a>Примечания

Посетители форм **звонят GetViewContext,** чтобы получить указатель на контекст представления, установленный в предыдущем вызове [IMAPIForm::SetViewContext.](imapiform-setviewcontext.md) Если до вызова **SetViewContext** не было выполнено, **GetViewContext** устанавливает  _для ppViewContext_ nULL. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Скопируйте указатель контекста представления формы в указатель, переданный вызываемой просматриваемой формой в параметре _ppViewContext._ Если форма не имеет контекста представления, установите  _для ppViewContext_ nULL. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI использует метод **IMAPIForm::GetViewContext,** чтобы проверить, имеет ли форма контекст представления.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

