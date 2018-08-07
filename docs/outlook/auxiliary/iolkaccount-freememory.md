---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Освобождает память, выделенную с помощью интерфейса IOlkAccount.
ms.openlocfilehash: ce3046db29cb2cac7d7ee72a3e4e9125346a4ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807785"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

Освобождает память, выделенную с помощью интерфейса [IOlkAccount](iolkaccount.md) . 
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>Параметры

_pv_
  
> [in] Указатель на память освобождения.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

Используйте этот метод для освобождения памяти, выделенной с [IOlkAccount::GetProp](iolkaccount-getprop.md) (если значение свойства указанную учетную запись типа двоичный или строки) и [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).
  
## <a name="see-also"></a>См. также

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

