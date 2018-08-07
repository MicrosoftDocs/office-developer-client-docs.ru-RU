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
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f42ccbeb94e1fc6b6cf880f1b32ee1bfeb24997e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807386"
---
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает значение, которое указывает, выполняется ли пользовательской функции в кластере. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Параметры

Эта функция не содержит аргументов.
  
## <a name="return-value"></a>������������ ��������

Если функция выполняется в процессе Excel, возвращает 0 в **XLOPER12** из типа **xlTypeInt**. Если функция выполняется в кластере, тип возвращаемого значения и значение определяется поставщиком соединитель кластера.
  
## <a name="requirements"></a>Требования

Эта функция определяется в файле Xlcall.h заголовка.
  
## <a name="see-also"></a>См. также

- [Функции защиты кластеров](cluster-safe-functions.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

