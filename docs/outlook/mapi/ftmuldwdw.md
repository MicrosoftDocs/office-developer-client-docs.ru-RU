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
  
Умножает одно целое число без знака 32 на другое.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Параметры

 _мултипликанд_
  
> возврата Двойное слово, содержащее Неподписанное 32 — разрядное целое число, умноженное на значение параметра _множителя_ . 
    
 _Умножителя_
  
> возврата Двойное слово, содержащее Неподписанное 32 — разрядное значение множителя.
    
## <a name="return-value"></a>Возвращаемое значение

Функция **фтмулдвдв** возвращает структуру [fileTime](filetime.md) , содержащую произведение двух целых чисел. Два входных параметра остаются неизменными. 
  

