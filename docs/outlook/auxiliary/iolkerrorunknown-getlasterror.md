---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Получает строку сообщения для заданной ошибки.
ms.openlocfilehash: 7b00392cdf65d1d4990f2231769e5126c9ae26dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807874"
---
# <a name="iolkerrorunknowngetlasterror"></a>IOlkErrorUnknown::GetLastError

Получает строку сообщения для заданной ошибки. 
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkErrorUnknown](iolkerrorunknown.md).
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a>Parameters

_управления персоналом_
  
> [in] Код ошибки для поиска.
    
_ppwszError_
  
> [out] Сообщение об ошибке, соответствующее для *отдела кадров* . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |The call succeeded.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько аргументов являются недопустимыми.  <br/> |
   
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)

