---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412914"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Умножает одну неподписаную 32-битную на другую.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Parameters

 _Multiplicand_
  
> [in] Двойное слово с неподписаным 32-разрядным набором, которое должно быть умножено на значение параметра _Multiplier._ 
    
 _Мультипликатор_
  
> [in] Двойное слово с неподписаным 32-разрядным множителем.
    
## <a name="return-value"></a>Возвращаемое значение

Функция **FtMulDwDw** возвращает структуру [FILETIME,](filetime.md) которая содержит продукт двух integers. Два параметра ввода остаются неизменными. 
  

