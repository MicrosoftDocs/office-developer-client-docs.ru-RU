---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Получает упорядочение указанной категории учетных записей.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424625"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

Получает упорядочение указанной категории учетных записей.
  
## <a name="quick-info"></a>Краткие сведения

См. [в окне IOlkAccountManager](iolkaccountmanager.md)
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>Parameters

_pclsidCategory_
  
> [in] ID класса категории, для которого необходимо получить заказ. The value must be one of the following:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  [вышел] Количество учетных записей. 
    
_prgAccts_
  
> [вышел] Указатель на массив учетных записей.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Вызов удался  <br/> |
|E_INVALIDARG  <br/> |Один или несколько аргументов являются недействительными.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Примечания

Перед вызовом этого метода вызываемая компания выделяет только *prgAccts* указателя массива, но не имеет памяти для массива, на котором *указывает prgAccts.* После возвращения этого метода звонящего необходимо использовать [IOlkAccountManager::FreeMemory,](iolkaccountmanager-freememory.md) чтобы освободить память, выделенную *для prgAccts.* 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

