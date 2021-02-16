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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Умножает одно неподписаное 32-битное 32-битное на другое.
  
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

## <a name="parameters"></a>Параметры

 _Multiplicand_
  
> [in] Двойное слово, которое содержит неподписаное 32-разрядное значение, умноженное на значение параметра _Multiplier._ 
    
 _Множитель_
  
> [in] Двойное слово, которое содержит 32-разрядный множитель неподписаных 32-разрядных номеров.
    
## <a name="return-value"></a>Возвращаемое значение

Функция **FtMulDwDw** возвращает структуру [FILETIME,](filetime.md) которая содержит продукт двух integers. Два входных параметра остаются без изменений. 
  

