---
title: xlfUnregister (форма 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfUnregister [Excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310166"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (форма 2)

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Может вызываться из команды DLL или XLL, которая вызывается Microsoft Excel. Это эквивалентно вызову **Unregister** из листа макросов Excel XLM. 
  
**xlfUnregister** можно вызывать в двух формах: 
  
- Форма 1: Отмена регистрации отдельной команды или функции.
    
- Форма 2: выгрузка и деактивация XLL.
    
Эта функция вызывает полную выгрузку DLL или ресурсов кода в форме 2. Он отменяет регистрацию всех функций в библиотеке DLL, даже если они используются другим макросом, независимо от числа используемых элементов. Эта функция вызывает **xlAutoClose**, а затем отменяет регистрацию всех функций в DLL.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Параметры

_пксмодулетекст_ (**кслтипестр**)
  
Имя библиотеки DLL.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

В случае успеха возвращает **значение true** (**кслтипебул**). В случае неудачной попытки возвращает **значение false**.
  
## <a name="remarks"></a>Замечания

> [!NOTE] 
> Не вызывайте эту форму функции из реализации [xlAutoClose](xlautoclose.md) при попытке отменить регистрацию всех ресурсов библиотеки DLL с помощью одного вызова простой функции. Это приводит к рекурсивному вызову **xlAutoClose** и переполнению стека. 
  
### <a name="remember-to-delete-names"></a>Не заБудьте удалить имена

Если для параметра _пксфунктионтекст_ задано значение **xlfRegister**, то при регистрации функций и команд DLL необходимо явно удалить имена, вызвав **xlfSetName** для каждого из них, опустив второй аргумент, чтобы функция больше не отображается в мастере функций. Дополнительные сведения см. в статье [Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>См. также

- [xlfRegister (форма 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (форма 1)](xlfunregister-form-1.md)
- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

