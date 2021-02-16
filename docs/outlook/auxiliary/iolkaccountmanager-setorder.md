---
title: IOlkAccountManagerSetOrder
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

_pclsidCategory_
  
> [in] ИД класса категории, для которого необходимо установить порядок. Поддерживаются такие значения:
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_cAccts_
  
> [in] Количество учетных записей.
    
_rgAccts_
  
> [in] Массив ИД учетных записей. Размер массива — _cAccts._
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |Новый порядок сортировки имеет другое количество учетных записей, чем старый порядок сортировки.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько аргументов недопустимы.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Примечания

Вызываемая точка выделяет память для _prgAccts_ указателя массива, а также для массива, на котором _указывает prgAccts._ 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

