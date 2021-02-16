---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406348"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Умножает неподписаное 64-битное 64-битное на неподписаное 32-битное.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Параметры

 _Множитель_
  
> [in] Двойное слово, которое содержит 32-разрядный множитель неподписаных 32-разрядных номеров. 
    
 _Multiplicand_
  
> [in] Структура [FILETIME,](filetime.md) которая содержит неподписаенное 64-битное 64-битное значение, умноженное на значение параметра _Multiplier._ 
    
## <a name="return-value"></a>Возвращаемое значение

Функция **FtMulDw** возвращает структуру **FILETIME,** которая содержит продукт двух integers. Два входных параметра остаются без изменений. 
  

