---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- кслруннингонклустер
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f5c630c73899b07e2727a7d42b18eb1891797bab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310103"
---
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает значение, которое указывает, выполняется ли пользовательская функция в кластере. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Параметры

У этой функции нет аргументов.
  
## <a name="return-value"></a>Возвращаемое значение

Если функция выполняется в процессе Excel, возвращает значение 0 в **XLOPER12** типа **кслтипеинт**. Если функция выполняется на кластере, тип возвращаемого значения и его значение определяются поставщиком соединителей кластера.
  
## <a name="requirements"></a>Требования

Эта функция определена в файле заголовка Xlcall. h.
  
## <a name="see-also"></a>См. также

- [Функции защиты кластеров](cluster-safe-functions.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

