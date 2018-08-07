---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Освобождает память, выделенную с помощью интерфейса IOlkAccountManager.
ms.openlocfilehash: 85ba4d0d47eb5c879fa562e3147860533ef59f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807841"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

Освобождает память, выделенную с помощью интерфейса [IOlkAccountManager](iolkaccountmanager.md) . 
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>Parameters

_pv_
  
> [in] Указатель на память, чтобы освободить место.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

Используйте этот метод для освобождения памяти, выделенной [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).
  
## <a name="see-also"></a>См. также

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

