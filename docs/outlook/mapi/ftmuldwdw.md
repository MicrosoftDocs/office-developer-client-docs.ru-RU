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
ms.openlocfilehash: 16dca82b94225afc88bcb6c4e698a50565d6b088
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808517"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Относится к**: Outlook 
  
Умножает один целых 32-разрядная версия на другой.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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
    
## <a name="return-value"></a>������������ ��������

Функция **FtMulDwDw** возвращает структуру [FILETIME](filetime.md) , содержащую произведение двух целых чисел. Два входных параметра не изменяются. 
  

