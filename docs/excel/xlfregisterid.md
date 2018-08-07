---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- функция xlfregisterid [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807363"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Может быть вызван из библиотеки DLL, которая был вызван с Microsoft Excel. Если функция уже зарегистрирован, она возвращает идентификатор регистрации для этой функции без повторная регистрация его. Если функция не зарегистрирован, он регистрирует его и возвращает итоговый код регистра.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Параметры

_pxModuleText_ (**xltypeStr**)
  
Имя DLL, содержащей функцию.
  
_pxProcedure_ (**xltypeStr** или **xltypeNum**)
  
Если строка, имя вызываемой функции. Если номер, порядковый номер экспорта число вызываемой функции. Для ясности и надежности всегда используйте форму строки.
  
_pxTypeText_ (**xltypeStr**)
  
Необязательный атрибут типа string, указав типов всех аргументов в функцию и типа возвращаемого значения функции. Дополнительные сведения см в разделе «Примечания». Этот аргумент можно опустить, для изолированной DLL (XLL) определение **xlAutoRegister**.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Возвращает идентификатор регистрации функции (**xltypeNum**), который можно использовать в последующих вызовов **xlfUnregister**.
  
## <a name="remarks"></a>Замечания

Эта функция полезна, когда требуется заниматься обслуживание кодом реестра, но необходимо одно более поздней версии для отмены регистрации. Также полезно для назначения для меню, средств и кнопки при функцию, которую необходимо назначить в библиотеке DLL.
  
Где зарегистрировала функции DLL или XLL с аргументом допустимый _pxFunctionText_ указан в **xlfRegister**Идентификатору register также можно получить, передав _pxFunctionText_ функция **xlfEvaluate**.
  
## <a name="see-also"></a>См. также

- [РЕГИСТРАЦИЯ](xlfregister-form-1.md)
- [ОТМЕНА РЕГИСТРАЦИИ](xlfunregister-form-1.md)
- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

