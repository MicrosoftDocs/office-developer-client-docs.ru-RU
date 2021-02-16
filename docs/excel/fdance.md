---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- функция fdance [excel 2007]
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
  
Пример пользовательской команды, которая изменяет выбранные ячейки активного таблицы, пока пользователь не нажмет **КЛАВИШУ ESC.** При загрузке GENERIC.xll создается пользовательское меню Generic, через которое можно получить доступ к этой команде.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Параметры

Функция не принимает никаких параметров.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция всегда возвращает 1.
  
## <a name="remarks"></a>Примечания

Это пример продолжительной операции. Она периодически вызывает [функцию xlAbort.](xlabort.md) Это дает процессор (помогает совместной многозадачности) и проверяет, нажал ли пользователь **ESC,** чтобы отменить операцию. В этом случае пользователь может отменить отмену. 
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

