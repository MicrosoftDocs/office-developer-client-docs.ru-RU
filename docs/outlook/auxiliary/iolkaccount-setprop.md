---
title: Иолкаккаунтсетпроп
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Задает значение указанного свойства учетной записи.
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431990"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

Задает значение указанного свойства учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Параметры

_Двпроп_
  
> возврата Тег свойства для свойства Account, которое необходимо задать.
    
_ПВАР_
  
> возврата Значение указанного свойства.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Вызов метода выполнен успешно.  <br/> |
|E_INVALIDARG  <br/> |Указан недопустимый тег свойства.  <br/> |
   
## <a name="remarks"></a>Примечания

Используйте [иолкаккаунт:: SaveChanges](iolkaccount-savechanges.md) , чтобы сохранить изменения в значении свойств учетной записи. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

