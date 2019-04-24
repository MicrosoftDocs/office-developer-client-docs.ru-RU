---
title: Иолкаккаунтжетпроп
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Получает значение свойства указанной учетной записи.
ms.openlocfilehash: d24df8cfa9d54bee4614c1f31e12268748b8c986
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321239"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

Получает значение свойства указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Параметры

_Двпроп_
  
> возврата Тег свойства для свойства Account, которое требуется получить.
    
_ПВАР_
  
> вышли Значение указанного свойства.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|Е_АККТ_НОТ_ФАУНД  <br/> |Свойство не найдено для заданной учетной записи.  <br/> |
|E_INVALIDARG  <br/> |Указан недопустимый тег свойства.  <br/> |
   
## <a name="remarks"></a>Замечания

После возврата этого метода, если значением свойства Account является двоичный или строковый тип, необходимо освободить *ПВАР* с помощью [Иолкаккаунт:: фримемори](iolkaccount-freememory.md).
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

