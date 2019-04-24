---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- Функция фшовдиалог [Excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310852"
---
# <a name="fshowdialog"></a>fShowDialog

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательской команды, которая загружает и отображает пример собственного диалогового окна Windows. При загрузке GENERIC. XLL создается пользовательское меню с общим доступом, через которое осуществляется доступ к этой команде.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Параметры

Функция не принимает параметры.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция возвращает целочисленный ноль, указывающий на успешность выполнения
  
## <a name="remarks"></a>Замечания

Ниже приведены действия по отображению собственного диалогового окна Windows.
  
1. Получите основной дескриптор Windows Excel с помощью метода **** getHandler.
    
2. Подключите главное окно Excel с помощью **хукексцелвиндов**.
    
3. Откройте диалоговое окно с помощью **DialogBox**.
    
4. Отсоедините главное окно Excel с помощью **унхукексцелвиндов**.
    
### <a name="example"></a>Пример

Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

