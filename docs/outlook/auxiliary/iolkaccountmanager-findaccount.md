---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Находит учетную запись по значению свойства.
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428804"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

Находит учетную запись по значению свойства.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a>Параметры

_dwProp_
  
> [in] Свойство для поиска. Должен быть [PROP_ACCT_ID](prop_acct_id.md) или [PROP_ACCT_IS_EXCH.](prop_acct_is_exch.md)
    
_pVar_
  
> [in] Значение для совпадения.
    
_ppAccount_
  
> [out] Найденная учетная запись. Этот объект поддерживает интерфейс [IOlkAccount.](iolkaccount.md) 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Не удается найти указанную учетную запись.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |Один или несколько параметров недопустимы.  <br/> |
   
## <a name="see-also"></a>См. также

- [ACCT_VARIANT](acct_variant.md)  
- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

