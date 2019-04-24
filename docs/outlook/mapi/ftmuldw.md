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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328002"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Умножает 64 — разрядное целое число без знака на 32 — разрядное целое число.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Параметры

 _Умножителя_
  
> возврата Двойное слово, содержащее Неподписанное 32 — разрядное значение множителя. 
    
 _Мултипликанд_
  
> возврата Структура [fileTime](filetime.md) , которая содержит неподписанное 64 — разрядное целое число, умноженное на значение параметра _множителя_ . 
    
## <a name="return-value"></a>Возвращаемое значение

Функция **фтмулдв** возвращает структуру **fileTime** , содержащую произведение двух целых чисел. Два входных параметра остаются неизменными. 
  

