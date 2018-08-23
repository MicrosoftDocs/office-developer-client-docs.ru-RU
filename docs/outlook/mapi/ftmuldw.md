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
ms.openlocfilehash: c823a4e3d08d9082a3b5ac5c4bd8169612caa16e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583997"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Умножает целых 64-разрядная версия с 32-разрядное целое число без знака.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Параметры

 _Множитель_
  
> [in] Двойное слово, содержащий множитель неподписанных 32-разрядное целое число. 
    
 _Множитель_
  
> [in] Структура [FILETIME](filetime.md) , содержащую целых 64-разрядная версия умножается на значение параметра _Множитель_ . 
    
## <a name="return-value"></a>������������ ��������

Функция **FtMulDw** возвращает структуру **FILETIME** , содержащую произведение двух целых чисел. Два входных параметра не изменяются. 
  

