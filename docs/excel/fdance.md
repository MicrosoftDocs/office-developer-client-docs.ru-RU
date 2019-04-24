---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- Функция фданце [Excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311041"
---
# <a name="fdance"></a>fDance

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательской команды, которая изменяет выбранные ячейки на активном листе до тех пор, пока пользователь не нажмет клавишу **ESC**. При загрузке GENERIC. XLL создается пользовательское меню с общим доступом, через которое осуществляется доступ к этой команде.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Параметры

Функция не принимает параметры.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция всегда возвращает 1.
  
## <a name="remarks"></a>Замечания

Это пример длительной операции. Он иногда вызывает функцию [xlAbort](xlabort.md) . Это дает процессор (способствует совместной работе с многозадачными задачами) и проверяет, нажал ли пользователь клавишу **ESC** , чтобы отменить операцию. Если да, то пользователь может отменить прерывание. 
  
### <a name="example"></a>Пример

Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

