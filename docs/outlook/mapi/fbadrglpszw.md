---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436442"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет все строки в массиве строк Юникод. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a>Параметры

 _lppszW_
  
> [in] Указатель на массив строк Юникод с null-terminated. 
    
 _cStrings_
  
> [in] Количество строк в массиве, на который указывает параметр _lppszW._ 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Одна или несколько строк в указанном массиве являются недействительными. 
    
FALSE 
  
> Строки в указанном массиве допустимы.
    

