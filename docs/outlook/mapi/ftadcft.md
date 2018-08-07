---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9be25dc655536ff5d32a635da57c54ebd12fea0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808515"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**Относится к**: Outlook 
  
Добавляет один целых 64-разрядная версия на другой, при необходимости с помощью реализуемые флаг.
  
|||
|:-----|:-----|
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>Параметры

 _FT1_
  
> [in] Структура [FILETIME](filetime.md) , содержащую первого целого числа без знака 64-разрядная версия будет добавлена. 
    
 _ft2_
  
> [in] Структура FILETIME, содержащий второй целого числа без знака 64-разрядная версия будет добавлена.
    
 _pwCarry_
  
> [in, out, необязательно] На входе указатель входящего выполнение флаг. На выходе указатель мыши на результат выполнения для добавления. Этот параметр может быть NULL, если в результате выполнения не требуется.
    
## <a name="return-value"></a>������������ ��������

Функция **FtAdcFt** возвращает структуру **FILETIME** , содержащую сумма двух целых чисел. Два входных параметра не изменяются. Если **pwCarry** не равно NULL, в результате выполнения содержит для сумм, 0 или 1. 
  
## <a name="remarks"></a>Замечания

Функция **FtAdcFt** идентична **FtAddFt** при _pwCarry_ имеет значение NULL. Если _pwCarry_ не равно NULL и указывает на 0, **FtAdcFt** возвращает значение **FILETIME** , которое возвращает **FtAddFt** . 
  
## <a name="see-also"></a>См. также



[FtAddFt](ftaddft.md)

