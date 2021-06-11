---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fexit function [Excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429917"
---
# <a name="fexit"></a>fExit

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Пример команды, определяемой пользователем, которая разгружает GENERIC.xll. При загрузке GENERIC.xll создается меню, определяемое пользователем, Generic, с помощью которого получается доступ к этой команде. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Parameters

Функция не принимает параметров.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция всегда возвращает 1.
  
## <a name="remarks"></a>Примечания

Это процедура, инициированная пользователем, чтобы выйти из GENERIC.xll. Следует избегать простого вызова  `UNREGISTER("GENERIC.XLL")` в этой функции. Это принудительно отрегистрирует все функции в этом DLL, даже если они зарегистрированы в другом месте. Вместо этого отрегистрим функции по одному. 
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

