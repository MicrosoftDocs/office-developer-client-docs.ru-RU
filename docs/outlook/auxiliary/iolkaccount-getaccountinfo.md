---
title: Иолкаккаунтжетаккаунтинфо
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Получает сведения о типе и категориях для указанной учетной записи.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437905"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Получает сведения о типе и категориях для указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Параметры

_Пклсидтипе_
  
> вышли Идентификатор класса для типа учетной записи. The value must be one of the following:
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - Клсид_олкмапиаккаунт 
    
   - Клсид_олкхотмаилаккаунт 
    
   - Клсид_олклдапаккаунт
    
_Пккатегориес_
  
> вышли Количество категорий в _пргклсидкатегори_.
    
_Пргклсидкатегори_
  
> вышли Массив категорий, с которыми связана эта учетная запись. Массив имеет размер * _пккатегориес_. Значение каждой категории в массиве должно быть одним из следующих:
    
   - Клсид_олкмаил
    
   - Клсид_олкаддрессбук
    
   - Клсид_олксторе
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

После возврата этого метода необходимо освободить *пргклсидкатегори* с помощью [Иолкаккаунт:: фримемори](iolkaccount-freememory.md).
  
**Иолкаккаунт:: жетаккаунтинфо** не поддерживает категорию адресной книги для учетной записи Exchange. Если учетная запись является учетной записью Exchange (*пклсидтипе* — **клсид_олкмапиаккаунт** ), а учетная запись реализует адресную книгу, вызов **иолкаккаунт:: Жетаккаунтинфо** не будет возвращать **клсид_олкаддрессбук** в качестве категории в * Пргклсидкатегори* . 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

