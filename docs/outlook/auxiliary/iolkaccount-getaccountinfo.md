---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Получает сведения о типа и категорий для указанной учетной записи.
ms.openlocfilehash: 85f27d1d5f47a372090b208821b52656a56559ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807776"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Получает сведения о типа и категорий для указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Parameters

_pclsidType_
  
> [out] Идентификатор класса для типа учетной записи. The value must be one of the following:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [out] Число категорий в _prgclsidCategory_.
    
_prgclsidCategory_
  
> [out] Массив категории, которые связаны с этой учетной записи. Массив имеет размер * _pcCategories_. Значение каждой категории в массиве должно быть одно из следующих:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

После возврата этим методом, должен освободить *prgclsidCategory* с помощью [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
**IOlkAccount::GetAccountInfo** не поддерживает категории адресной книги для учетной записи Exchange. Если учетная запись Exchange учетной записи (*pclsidType* — **CLSID_OlkMAPIAccount** ) и учетную запись реализует адресной книги, вызывающий **IOlkAccount::GetAccountInfo** не будет возвращать **CLSID_OlkAddressBook** как категории в * prgclsidCategory* . 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

