---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- Функция xlopertoxloper12 [Excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303908"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Процедура преобразования, используемая для преобразования старой версии **XLOPER** в новую **XLOPER12**.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Параметры

_пкслопер_ (**Лпкслопер**)
  
Указатель на исходную **XLOPER** , которую необходимо преобразовать. 
  
_pxloper12_ (**LPXLOPER12**)
  
Указатель на целевую объект **XLOPER12** , в котором будет содержаться преобразованное значение. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

**Значение true** , если преобразование выполнено успешно, в противном случае — **значение false** . 
  
## <a name="remarks"></a>Замечания

В зависимости от типа **XLOPER**эта функция выделяет новый буфер памяти для преобразованных значений, которые указывают на целевую **XLOPER12**. Вызывающий абонент отвечает за освобождение памяти, связанной с копией, если преобразование является успешным; **FreeXLOper12T** можно использовать, или он может быть выполнен напрямую с помощью **бесплатной**функции.
  
Если преобразование завершается неудачно, вызывающему объекту не требуется освобождать память.
  
Как правило, можно выполнить преобразование из любой **XLOPER** в **XLOPER12** . В отличие от этого, преобразование из **XLOPER12** в **XLOPER** может закончиться ошибкой, если **XLOPER12** содержит слишком большой массив или ссылку или слишком длинную строку для хранения в ней. **** 
  
**XLOPER** Строки байтов ASCII преобразуются **** в строки двухбайтовых символов Юникода, зависящие от языкового стандарта. 
  
### <a name="example"></a>Пример

В этом файле `\SAMPLES\FRAMEWRK\FRAMEWRK.C` содержится код для этой функции. 
  

