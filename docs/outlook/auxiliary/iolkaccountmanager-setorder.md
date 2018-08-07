---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Изменяет порядок использования учетных записей в указанной категории.
ms.openlocfilehash: fcb27404471c9b551320027b0ed6979926ad3d58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807849"
---
# <a name="iolkaccountmanagersetorder"></a>IOlkAccountManager::SetOrder

Изменяет порядок использования учетных записей в указанной категории.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a>Parameters

_pclsidCategory_
  
> [in] КОД класса категории, для которого необходимо задать порядок. The value must be one of the following:
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_cAccts_
  
> [in] Число учетных записей.
    
_rgAccts_
  
> [in] Массив идентификаторов учетной записи. Размер массива — _cAccts_.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |The call succeeded.  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |Порядок сортировки имеет ряд различных учетных записей более старые порядок сортировки.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько аргументов являются недопустимыми.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Remarks

Звонящий выделение памяти для массива указатель _prgAccts_ , а также для массива, на который указывает _prgAccts_ . 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

