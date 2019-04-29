---
title: Иолкаккаунтманажеренумератеаккаунтс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Gets an enumerator for the accounts of the specific category or type.
ms.openlocfilehash: d0d383dee0e76dd6310d01bd1482e307c2374856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423050"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a>IOlkAccountManager::EnumerateAccounts

Gets an enumerator for the accounts of the specific category or type.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a>Параметры

_Пклсидкатегори_
  
> [in] The class identifier of the category to enumerate. The value must be one of the following:
    
   - Клсид_олкмаил 
    
   -  Клсид_олкаддрессбук 
    
   - Клсид_олксторе 
    
_Пклсидтипе_
  
> [in] The class identifier of the account type to enumerate. The value must be one of the following:
    
   - CLSID_OlkPOP3Account
    
   - CLSID_OlkIMAP4Account
    
   - Клсид_олкмапиаккаунт
    
   - Клсид_олкхотмаилаккаунт
    
   - Клсид_олклдапаккаунт
    
_dwFlags_
  
> [in] Flags to modify behavior. The only supported value is OLK_ACCOUNT_NO_FLAGS.
    
_Ппенум_
  
> [out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface. 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|Е_ОЛК_НОТ_ИНИТИАЛИЗЕД  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Примечания

Specifying NULL for category returns an enumerator of all accounts of the specified type. Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.
  
 **IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account. Если учетная запись является учетной записью Exchange (*пклсидтипе* — **клсид_олкмапиаккаунт** ), и вы пытаетесь перечислить учетные записи, которые реализуют адресную книгу (*пргклсидкатегори* — **клсид_олкаддрессбук** ), вызов ** Иолкаккаунтманажер:: EnumerateAccounts** не будет возвращать учетную запись Exchange в перечислителе учетных записей *ппенум* . 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkEnum](iolkenum.md)

