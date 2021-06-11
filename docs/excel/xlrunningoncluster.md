---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f5c630c73899b07e2727a7d42b18eb1891797bab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418290"
---
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает значение, которое указывает, работает ли функция, определяемая пользователем, в кластере. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameters

Эта функция не имеет аргументов.
  
## <a name="return-value"></a>Возвращаемое значение

Если функция работает в процессе Excel, возвращается 0 в **XLOPER12** типа **xlTypeInt**. Если функция работает в кластере, тип и значение возврата определяются поставщиком соединители кластера.
  
## <a name="requirements"></a>Требования

Эта функция определяется в файле загона Xlcall.h.
  
## <a name="see-also"></a>См. также

- [Функции защиты кластеров](cluster-safe-functions.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

