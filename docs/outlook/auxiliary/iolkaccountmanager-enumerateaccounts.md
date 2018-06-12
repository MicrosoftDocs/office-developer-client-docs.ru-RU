---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Gets an enumerator for the accounts of the specific category or type.
ms.openlocfilehash: f9b332c0bbc90b1a8f5f944492448055f23c0668
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807848"
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

## <a name="parameters"></a>Parameters

_pclsidCategory_
  
> [in] The class identifier of the category to enumerate. The value must be one of the following:
    
   - CLSID_OlkMail 
    
   -  CLSID_OlkAddressBook 
    
   - CLSID_OlkStore 
    
_pclsidType_
  
> [in] The class identifier of the account type to enumerate. The value must be one of the following:
    
   - CLSID_OlkPOP3Account
    
   - CLSID_OlkIMAP4Account
    
   - CLSID_OlkMAPIAccount
    
   - CLSID_OlkHotmailAccount
    
   - CLSID_OlkLDAPAccount
    
_dwFlags_
  
> [in] Flags to modify behavior. The only supported value is OLK_ACCOUNT_NO_FLAGS.
    
_ppEnum_
  
> [out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface. 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |The call succeeded.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Remarks

Specifying NULL for category returns an enumerator of all accounts of the specified type. Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.
  
 **IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account. Если учетная запись является учетной записью Exchange (*pclsidType* — **CLSID_OlkMAPIAccount** ), и вы пытаетесь перечисление учетных записей, которые реализуют адресной книги (*prgclsidCategory* — **CLSID_OlkAddressBook** ), вызов ** IOlkAccountManager::EnumerateAccounts** не возвращает учетную запись Exchange в перечислителя учетные записи *ppEnum* . 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkEnum](iolkenum.md)

