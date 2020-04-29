---
title: иолкеррорункновнжетластеррор
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Получает строку сообщения для указанной ошибки.
ms.openlocfilehash: 4d2aa3a7513687484988921734eb4c0e6f91226b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431703"
---
# <a name="iolkerrorunknowngetlasterror"></a>IOlkErrorUnknown::GetLastError

Получает строку сообщения для указанной ошибки. 
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкеррорункновн](iolkerrorunknown.md).
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a>Параметры

_hr_
  
> возврата Код ошибки для поиска.
    
_ппвсзеррор_
  
> вышли Сообщение об ошибке, соответствующее *HR* . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько аргументов являются недопустимыми.  <br/> |
   
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)

