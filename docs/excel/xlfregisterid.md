---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- функция xlfregisterid [Excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420061"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Может быть вызвано из DLL, которое само по себе было вызвано Microsoft Excel. Если функция уже зарегистрирована, она возвращает существующий ID реестра для этой функции без ее перерегистрации. Если функция еще не зарегистрирована, она регистрирует ее и возвращает итоговую регистрацию.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Parameters

_pxModuleText_ **(xltypeStr)**
  
Имя DLL, содержащего функцию.
  
_pxProcedure_ **(xltypeStr** или **xltypeNum)**
  
Если строка, имя вызываемой функции. Если номер, ordinal export number of the function to call. Для ясности и надежности всегда используйте строковую форму.
  
_pxTypeText_ **(xltypeStr)**
  
Необязательная строка, указывая типы всех аргументов для функции и тип возвращаемого значения функции. Дополнительные сведения см. в разделе "Замечания". Этот аргумент может быть опущен для отдельной DLL (XLL), определяющей **xlAutoRegister**.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает зарегистрированный ID функции **(xltypeNum),** который можно использовать в последующих вызовах **xlfUnregister**.
  
## <a name="remarks"></a>Примечания

Эта функция полезна, если вы не хотите беспокоиться о сохранении регистрации, но вам потребуется один позже для незарегистрации. Это также полезно для назначения меню, инструментов и кнопок, когда функции, которые вы хотите назначить, находится в DLL.
  
Если функция DLL или XLL была зарегистрирована с допустимым аргументом  _pxFunctionText,_ предоставленным **xlfRegister,** его удостоверение регистра также можно получить, передав  _pxFunctionText_ функции **xlfEvaluate**.
  
## <a name="see-also"></a>См. также

- [РЕГИСТРАЦИЯ](xlfregister-form-1.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

