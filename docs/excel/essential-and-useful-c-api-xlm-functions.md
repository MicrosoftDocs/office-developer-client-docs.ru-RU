---
title: Важные и полезная функции функции XLM В C API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции [Excel 2007], c API XLM
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d6acd5bb171fb2494f2adb23584f4e7f088e1b83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311125"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a>Важные и полезная функции функции XLM В C API

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функции, описанные в этом разделе, являются функциями обратного вызова Microsoft Excel, которые особенно удобны для разработчиков DLL и XLL. В этом случае функция **xlfRegister** важна для XLL-библиотек и библиотек DLL, которые хотят зарегистрировать свои функции и команды, чтобы их можно было вызывать непосредственно из Excel. Функции **xlfUnregister** и **xlfSetName** используются в сочетании для отмены регистрации DLL и функций XLL и команд. 
  
Многие другие функции Excel предоставляются с помощью API C, которые можно использовать при разработке XLL-модулей. Они соответствуют функциям и командам листа Excel, которые доступны на листах макросов XLM.
  
## <a name="in-this-section"></a>Содержание

[xlfCaller](xlfcaller.md)
  
[xlfEvaluate](xlfevaluate.md)
  
[xlfGetDef](xlfgetdef.md)
  
[xlfGetName](xlfgetname.md)
  
[xlfRegister (����� 1)](xlfregister-form-1.md)
  
[xlfRegister (форма 2)](xlfregister-form-2.md)
  
[xlfRegisterId](xlfregisterid.md)
  
[xlfUnregister (форма 1)](xlfunregister-form-1.md)
  
[xlfUnregister (форма 2)](xlfunregister-form-2.md)
  
[xlfSetName](xlfsetname.md)
  

