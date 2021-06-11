---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- функция fdance [Excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409050"
---
# <a name="fdance"></a>fDance

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Пример команды, определяемой пользователем, которая изменяет выбранные ячейки на активном таблице, пока пользователь не нажмет **ESC.** При загрузке GENERIC.xll создается меню, определяемое пользователем, Generic, с помощью которого получается доступ к этой команде.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Parameters

Функция не принимает параметров.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция всегда возвращает 1.
  
## <a name="remarks"></a>Примечания

Это пример длительной операции. Иногда она вызывает [функцию xlAbort.](xlabort.md) Это дает процессору (помогает совместной многозадачности) и проверяет, нажал ли пользователь **ESC** на отмену операции. Если это так, он предоставляет пользователю возможность отменить отмену. 
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

