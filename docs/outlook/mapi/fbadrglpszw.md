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
ms.openlocfilehash: 3b3b6b5ca0b06fc55a60e035ffd9118391cab8f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565916"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет все строки в массив строк в кодировке Юникод. 
  
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
  
> [in] Указатель на массив строк Юникод, завершающуюся символом null. 
    
 _cStrings_
  
> [in] Количество строк в массиве, на который указывает параметр _lppszW_ . 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Один или несколько строк в указанном массиве являются недопустимыми. 
    
FALSE 
  
> Допустимы строки из указанного массива.
    

