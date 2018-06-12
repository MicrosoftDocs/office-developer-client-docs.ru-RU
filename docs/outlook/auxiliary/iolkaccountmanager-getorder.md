---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Получает порядок использования учетных записей в указанной категории.
ms.openlocfilehash: d05e354e25d49a51b3d3f8f053c2b39dc37b333f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807853"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

Получает порядок использования учетных записей в указанной категории.
  
## <a name="quick-info"></a>Краткие сведения

Просмотреть [IOlkAccountManager](iolkaccountmanager.md)
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>Parameters

_pclsidCategory_
  
> [in] Идентификатор класса категории, для которого необходимо получить порядке. The value must be one of the following:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  [out] Число учетных записей. 
    
_prgAccts_
  
> [out] Указатель на массив учетных записей.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |Вызов успешно завершен  <br/> |
|E_INVALIDARG  <br/> |Один или несколько аргументов являются недопустимыми.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Remarks

Прежде чем вызывать этот метод, вызывающего выделяет только массива указатель *prgAccts* , но не памяти для массива, на который указывает *prgAccts* . После этот метод возвращает, вызывающего необходимо использовать [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) для освобождения памяти, выделенной для *prgAccts* . 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

