---
title: Иолкаккаунтманажерфиндаккаунт
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Находит учетную запись по значению свойства.
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322080"
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

_Двпроп_
  
> возврата Свойство, по которому необходимо выполнить поиск. Должен быть [проп_аккт_ид](prop_acct_id.md) или [проп_аккт_ис_ексч](prop_acct_is_exch.md).
    
_ПВАР_
  
> возврата Значение для сравнения.
    
_Ппаккаунт_
  
> вышли Учетная запись найдена. Этот объект поддерживает интерфейс [иолкаккаунт](iolkaccount.md) . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|Е_АККТ_НОТ_ФАУНД  <br/> |Не удается найти указанную учетную запись.  <br/> |
|Е_ОЛК_НОТ_ИНИТИАЛИЗЕД  <br/> |The account manager has not been initialized for use.  <br/> |
|Е_ОЛК_ПАРАМ_НОТ_СУППОРТЕД  <br/> |Один или несколько параметров являются недопустимыми.  <br/> |
   
## <a name="see-also"></a>См. также

- [ACCT_VARIANT](acct_variant.md)  
- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

