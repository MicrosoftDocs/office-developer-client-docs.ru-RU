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
ms.openlocfilehash: 2c463252aa029ac4c7cb2fac6e962a5d8af31b97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808879"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**Относится к**: Outlook 
  
Возвращает текущий контекст представления для формы. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Параметры

 _ppViewContext_
  
> [out] Указатель на указатель на контекст представления формы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Текущий контекст представления формы успешно возвращен. 
    
S_FALSE 
  
> Отсутствует контекст представления для формы.
    
## <a name="remarks"></a>Замечания

Средства просмотра формы вызов **GetViewContext** для получения указателя контекст представления, указанной в предыдущем вызов [IMAPIForm::SetViewContext](imapiform-setviewcontext.md). Если предыдущий вызов не выполнена в **SetViewContext**, **GetViewContext** задает _ppViewContext_ значение NULL. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Скопируйте указатель контекст представления формы в указатель, переданный по вызову средства просмотра формы с помощью параметра _ppViewContext_ . Если форма не имеет контекст представления, необходимо задайте _ppViewContext_ значение NULL. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |Mfcmapi (en) использует метод **IMAPIForm::GetViewContext** , чтобы проверить наличие контекст представления.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

