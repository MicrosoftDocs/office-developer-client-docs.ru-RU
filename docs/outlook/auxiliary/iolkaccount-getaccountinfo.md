---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Получает сведения о типах и категориях указанной учетной записи.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437905"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Получает сведения о типах и категориях указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

См. [iOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Parameters

_pclsidType_
  
> [вышел] Идентификатор класса для типа учетной записи. The value must be one of the following:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [вышел] Количество категорий в  _prgclsidCategory_.
    
_prgclsidCategory_
  
> [вышел] Массив категорий, с которые связана эта учетная запись. Массив имеет размер * _pcCategories_. Значение каждой категории массива должно быть одним из следующих:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

После возвращения этого метода необходимо освободить *prgclsidCategory* с помощью [IOlkAccount::FreeMemory.](iolkaccount-freememory.md)
  
**IOlkAccount::GetAccountInfo** не поддерживает категорию адресной книги для Exchange учетной записи. Если учетная запись является учетной записью Exchange *(pclsidType* — **CLSID_OlkMAPIAccount),** а учетная запись реализует адресную книгу, вызов **IOlkAccount::GetAccountInfo** не возвращается CLSID_OlkAddressBook как категория *в prgclsidCategory* .  
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

