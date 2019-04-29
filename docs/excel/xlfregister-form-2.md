---
title: xlfRegister (форма 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- функция xlfRegister [Excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416043"
---
# <a name="xlfregister-form-2"></a>xlfRegister (форма 2)

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Может вызываться из команды DLL или XLL, которая вызывается Microsoft Excel. Это эквивалентно вызову **Register** из листа макросов Microsoft Office XLM. 
  
Функцию **xlfRegister** можно вызвать в двух формах: 
  
- [xlfRegister (форма 1)](xlfregister-form-1.md): регистрирует отдельные команды или функции.
    
- xlfRegister (форма 2): Загрузка и активация XLL-модуля.
    
Эта функция, выЗываемая в форме 2, может использоваться только для загрузки и активации XLL, содержащего процедуру [xlAutoOpen](xlautoopen.md) . 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Параметры

 _пксмодулетекст_ (**кслтипестр**)
  
Имя библиотеки DLL, которая должна быть загружена и активирована.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

В случае успешного выполнения возвращается имя DLL (**кслтипестр**). В противном случае возвращается #VALUE! ошибкой.
  
## <a name="see-also"></a>См. также



[Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

