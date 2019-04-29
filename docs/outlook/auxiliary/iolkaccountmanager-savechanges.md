---
title: Иолкаккаунтманажерсавечанжес
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Сохраняет изменения указанной учетной записи.
ms.openlocfilehash: dbb1dffa1725e96bd2ab635341718ce53738b864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429609"
---
# <a name="iolkaccountmanagersavechanges"></a>IOlkAccountManager::SaveChanges

Сохраняет изменения указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Параметры

_Двакктид_
  
> возврата Идентификатор учетной записи для сохранения. 
    
_dwFlags_
  
> [in] Flags to modify behavior. ОЛК_АККАУНТ_НО_ФЛАГС — единственное поддерживаемое значение.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Вызов выполнен успешно  <br/> |
|Е_АККТ_НОТ_ФАУНД  <br/> |Не удается найти указанную учетную запись.  <br/> |
|Е_ОЛК_НОТ_ИНИТИАЛИЗЕД  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Примечания

После изменения значения свойства учетной записи с помощью [иолкаккаунт:: сетпроп](iolkaccount-setprop.md), используйте **Иолкаккаунтманажер:: SaveChanges** или [иолкаккаунт:: SaveChanges](iolkaccount-savechanges.md) для сохранения таких изменений. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

