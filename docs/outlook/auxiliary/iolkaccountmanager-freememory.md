---
title: Иолкаккаунтманажерфримемори
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Освобождает память, выделенную интерфейсом Иолкаккаунтманажер.
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408490"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

Освобождает память, выделенную интерфейсом [иолкаккаунтманажер](iolkaccountmanager.md) . 
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>Параметры

_плата_
  
> возврата Указатель на память, которую требуется освободить.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Этот метод используется для освобождения памяти, выделенной [иолкаккаунтманажер::.](iolkaccountmanager-getorder.md)
  
## <a name="see-also"></a>См. также

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

