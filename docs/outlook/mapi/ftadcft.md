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
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429707"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Добавляет одно неподписаное 64-битное 64-битное другое, при желании с помощью флага переноса.
  
|||
|:-----|:-----|
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>Параметры

 _ft1_
  
> [in] Структура [FILETIME,](filetime.md) которая содержит первое неподписаное 64-битное количество, которое необходимо добавить. 
    
 _ft2_
  
> [in] Структура FILETIME, которая содержит второе 64-битное неподписаенное 64-битное, которое необходимо добавить.
    
 _pwCarry_
  
> [in, out, optional] При вводе указатель на входящий флаг переноса. При выходе указатель на результат переноса для добавления. Этот параметр может иметь NULL, если результат переноса не требуется.
    
## <a name="return-value"></a>Возвращаемое значение

Функция **FtAdcFt** возвращает структуру **FILETIME,** которая содержит сумму двух integers. Два входных параметра остаются без изменений. Если **pwCarry** не имеет NULL, он содержит результат переноса для суммы, 0 или 1. 
  
## <a name="remarks"></a>Примечания

Функция **FtAdcFt** идентична **функции FtAddFt,**  _если pwCarry_ имеет NULL. Если _pwCarry не_ имеет значение NULL и указывает на 0, **FtAdcFt** возвращает то же **значение FILETIME,** что **и FtAddFt.** 
  
## <a name="see-also"></a>См. также



[FtAddFt](ftaddft.md)

