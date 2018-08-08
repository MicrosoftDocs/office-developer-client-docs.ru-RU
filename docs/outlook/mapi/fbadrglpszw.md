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
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808413"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Относится к**: Outlook 
  
Проверяет все строки в массив строк в кодировке Юникод. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
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
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Один или несколько строк в указанном массиве являются недопустимыми. 
    
FALSE 
  
> Допустимы строки из указанного массива.
    

