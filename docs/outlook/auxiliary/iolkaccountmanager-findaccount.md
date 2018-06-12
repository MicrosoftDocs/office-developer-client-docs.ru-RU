---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Поиск учетной записи по значению свойства.
ms.openlocfilehash: a7d016ab7e265e547b33940c16f96979bd5fa87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807846"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

Поиск учетной записи по значению свойства.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a>Parameters

_dwProp_
  
> [in] Свойство для поиска. Должно быть [PROP_ACCT_ID](prop_acct_id.md) или [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).
    
_pVar_
  
> [in] Значение в соответствии с.
    
_ppAccount_
  
> [out] Учетная запись найдена. Этот объект поддерживает интерфейс [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |The call succeeded.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Не удается найти указанную учетную запись.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
   
## <a name="see-also"></a>См. также

- [ACCT_VARIANT](acct_variant.md)  
- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

