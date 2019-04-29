---
title: Иолкаккаунтманажерсетордер
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Изменяет порядок указанной категории учетных записей.
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422861"
---
# <a name="iolkaccountmanagersetorder"></a>IOlkAccountManager::SetOrder

Изменяет порядок указанной категории учетных записей.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a>Параметры

_Пклсидкатегори_
  
> возврата Идентификатор класса категории, для которого требуется задать порядок. Поддерживаются такие значения:
    
   - Клсид_олкаддрессбук
    
   - Клсид_олксторе
    
_Какктс_
  
> возврата Число учетных записей.
    
_Ргакктс_
  
> возврата Массив идентификаторов учетных записей. Размер массива — _какктс_.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|Е_АККТ_ВРОНГ_СОРТ_ОРДЕР  <br/> |Для нового порядка сортировки используется разное число учетных записей, чем у старого порядка сортировки.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько аргументов являются недопустимыми.  <br/> |
|Е_ОЛК_НОТ_ИНИТИАЛИЗЕД  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Примечания

Вызывающий абонент выделяет память для указателя массива _пргакктс_ , а также для массива, в котором точки _пргакктс_ . 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

