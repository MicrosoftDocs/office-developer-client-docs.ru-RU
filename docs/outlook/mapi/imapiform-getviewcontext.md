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
ms.openlocfilehash: 9f09f29d67bff6588c826b92d93aead491510cef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574820"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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
  
> Текущий контекст представления формы успешно возвращен. 
    
S_FALSE 
  
> Отсутствует контекст представления для формы.
    
## <a name="remarks"></a>Замечания

Средства просмотра формы вызов **GetViewContext** для получения указателя контекст представления, указанной в предыдущем вызов [IMAPIForm::SetViewContext](imapiform-setviewcontext.md). Если предыдущий вызов не выполнена в **SetViewContext**, **GetViewContext** задает _ppViewContext_ значение NULL. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Скопируйте указатель контекст представления формы в указатель, переданный по вызову средства просмотра формы с помощью параметра _ppViewContext_ . Если форма не имеет контекст представления, необходимо задайте _ppViewContext_ значение NULL. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |Mfcmapi (en) использует метод **IMAPIForm::GetViewContext** , чтобы проверить наличие контекст представления.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

