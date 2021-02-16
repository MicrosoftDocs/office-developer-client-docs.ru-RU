---
title: xlfUnregister (форма 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419907"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (форма 2)

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Может быть вызван из команды DLL или XLL, которая сама была вызвана Microsoft Excel. Это эквивалентно вызову **UNREGISTER** из листа макроса XLM Excel. 
  
**XlfUnregister** может быть вызван в двух формах: 
  
- Форма 1. Unregisters an individual command or function.
    
- Форма 2. Выгружает и деактивирует XLL.
    
Эта функция, вызванная в форме 2, заставляет полностью выгрузить DLL или ресурс кода. Он отрегистрет все функции в DLL, даже если они в настоящее время используются другим макросом, независимо от того, сколько используется. Эта функция вызывает **xlAutoClose,** а затем отозвет регистрацию всех функций в DLL.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Параметры

_pxModuleText_ (**xltypeStr)**
  
Имя DLL.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

В случае успешного **сбоя возвращается TRUE** (**xltypeBool).** В случае неудачи возвращает **false.**
  
## <a name="remarks"></a>Примечания

> [!NOTE] 
> Не вызывайте эту форму функции из вашей реализации [xlAutoClose,](xlautoclose.md) чтобы отозвать все ресурсы DLL одним вызовом простой функции. Это приводит к рекурсивным вызовам **xlAutoClose** и переполнению стека. 
  
### <a name="remember-to-delete-names"></a>Не забудьте удалить имена

Если вы указали аргумент  _pxFunctionText_ для **xlfRegister,** при регистрации функций и команд DLL необходимо явно удалить имена, вызывая **xlfSetName** для каждого из них, опустить второй аргумент, чтобы функция больше не появилась в мастере функций. Дополнительные сведения см. в статье [Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>См. также

- [xlfRegister (форма 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (форма 1)](xlfunregister-form-1.md)
- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

