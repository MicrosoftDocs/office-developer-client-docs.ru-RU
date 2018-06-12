---
title: xlfRegister (формы 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- функция xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807350"
---
# <a name="xlfregister-form-2"></a>xlfRegister (формы 2)

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Может быть вызван из DLL или XLL команду, которая был вызван с Microsoft Excel. Это эквивалентно вызову **регистрации** из таблицы Excel XLM макрос. 
  
Функция **xlfRegister** может быть вызвана в двух вариантах: 
  
- [xlfRegister (формы 1)](xlfregister-form-1.md): регистрирует отдельные команды или функции.
    
- xlfRegister (формы 2): загружает и активирует надстройке XLL.
    
Вызывает в виде 2, эта функция может использоваться только для загружать и активировать XLL, содержащий процедуру [xlAutoOpen](xlautoopen.md) . 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameters

 _pxModuleText_ (**xltypeStr**)
  
Имя библиотеки DLL, загружать и активирован.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

В случае успешного выполнения возвращает имя DLL (**xltypeStr**). В противном случае возвращается #VALUE! Ошибка.
  
## <a name="see-also"></a>См. также



[Функции API XLM важные и полезные C](essential-and-useful-c-api-xlm-functions.md)

