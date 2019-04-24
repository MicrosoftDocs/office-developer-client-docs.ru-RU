---
title: Иолкаккаунтманажержетордер
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Получает упорядочивание указанной категории учетных записей.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322031"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

Получает упорядочивание указанной категории учетных записей.
  
## <a name="quick-info"></a>Краткие сведения

Просмотр [иолкаккаунтманажер](iolkaccountmanager.md)
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>Параметры

_Пклсидкатегори_
  
> возврата Идентификатор класса Category, для которого требуется получить порядок. The value must be one of the following:
    
   - Клсид_олкмаил
    
   - Клсид_олкаддрессбук
    
   - Клсид_олксторе
    
_Пкакктс_
  
>  вышли Число учетных записей. 
    
_Пргакктс_
  
> вышли Указатель на массив учетных записей.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Вызов выполнен успешно  <br/> |
|E_INVALIDARG  <br/> |Один или несколько аргументов являются недопустимыми.  <br/> |
|Е_ОЛК_НОТ_ИНИТИАЛИЗЕД  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Замечания

Перед вызовом этого метода вызывающий абонент выделяет только указатель массива *пргакктс* , но не память для массива, в котором точки *пргакктс* . После возврата этого метода вызывающий должен использовать [иолкаккаунтманажер:: фримемори](iolkaccountmanager-freememory.md) для освобождения памяти, выделенной для *пргакктс* . 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

