---
title: Иолкаккаунтфримемори
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Освобождает память, выделенную интерфейсом Иолкаккаунт.
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321338"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

Освобождает память, выделенную интерфейсом [иолкаккаунт](iolkaccount.md) . 
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>Параметры

_плата_
  
> возврата Указатель на память, которую необходимо освободить.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Замечания

Используйте этот метод для освобождения памяти, выделенной [иолкаккаунт::-Prop](iolkaccount-getprop.md) (если значение указанного свойства учетной записи является двоичным или строковым типом), и [Иолкаккаунт:: жетаккаунтинфо](iolkaccount-getaccountinfo.md).
  
## <a name="see-also"></a>См. также

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

