---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- функция fshowdialog [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807266"
---
# <a name="fshowdialog"></a>fShowDialog

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательской команды, загружает и отображает пример собственный диалоговое окно Windows. При загрузке GENERIC.xll, он создает пользовательских меню, общая, через который доступ к этой команды.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Параметры

Функция не принимает параметры.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Функция возвращаемое целое число ноль для указания успешное завершение работы
  
## <a name="remarks"></a>Замечания

Доступны следующие действия, чтобы открыть диалоговое окно собственного Windows:
  
1. Получите Microsoft Excel основной обработчик Windows с помощью **GetHwnd**.
    
2. Внедрение главного окна Excel с помощью **HookExcelWindow**.
    
3. Отображать диалоговое окно с помощью **следующейтаблице**.
    
4. Отсоедините главного окна Excel с помощью **UnhookExcelWindow**.
    
### <a name="example"></a>Пример

Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[Функции из универсальной библиотеки DLL](functions-in-the-generic-dll.md)

