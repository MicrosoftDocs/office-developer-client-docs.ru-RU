---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- функция fdialog [Excel 2007], функция fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431528"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Пример команды, определяемой пользователем, которая демонстрирует, как создать Microsoft Excel UDD (диалоговое окно с пользовательским определением) в DLL с помощью возможностей диалоговых полей в API C. При загрузке GENERIC.xll создается меню, определяемое пользователем, Generic, с помощью которого получается доступ к этой команде.
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>Parameters

Функция не принимает параметров.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция всегда возвращает 1.
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

