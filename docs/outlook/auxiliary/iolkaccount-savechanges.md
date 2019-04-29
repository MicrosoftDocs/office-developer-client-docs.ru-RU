---
title: Иолкаккаунтсавечанжес
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Фиксирует изменения объекта Account, записывая в хранилище реестра.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425836"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

Фиксирует изменения объекта Account, записывая в хранилище реестра.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Параметры

_dwFlags_
  
> [in] Flags to modify behavior. ОЛК_АККАУНТ_НО_ФЛАГС — единственное поддерживаемое значение.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Метод выполнен успешно.  <br/> |
|Е_АККТ_НОТ_ФАУНД  <br/> |Не удается найти указанную учетную запись.  <br/> |
|Е_ОЛК_НОТ_ИНИТИАЛИЗЕД  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Примечания

После изменения значения свойства учетной записи с помощью [иолкаккаунт:: сетпроп](iolkaccount-setprop.md), используйте **Иолкаккаунт:: SaveChanges** , чтобы сохранить такие изменения. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

