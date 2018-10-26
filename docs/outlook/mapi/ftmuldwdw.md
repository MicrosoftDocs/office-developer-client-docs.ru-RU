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
ms.openlocfilehash: 8002698b1644fb63292b4242d4fb3d784a99a03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592026"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Умножает один целых 32-разрядная версия на другой.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Параметры

 _Множитель_
  
> [in] Двойное слово, содержащий целых 32-разрядная версия умножается на значение параметра _Множитель_ . 
    
 _Множитель_
  
> [in] Двойное слово, содержащий множитель неподписанных 32-разрядное целое число.
    
## <a name="return-value"></a>Возвращаемое значение

Функция **FtMulDwDw** возвращает структуру [FILETIME](filetime.md) , содержащую произведение двух целых чисел. Два входных параметра не изменяются. 
  

