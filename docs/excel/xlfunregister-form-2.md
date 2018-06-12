---
title: xlfUnregister (формы 2)
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
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807373"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (формы 2)

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Может быть вызван из DLL или XLL команду, которая был вызван с Microsoft Excel. Это эквивалентно вызову **Отменить РЕГИСТРАЦИЮ** из таблицы Excel XLM макрос. 
  
**xlfUnregister** может быть вызван в двух вариантах: 
  
- Форма 1: Отменяет отдельные команды или функции.
    
- Форма 2: Выгрузка и деактивирует надстройке XLL.
    
Принудительно вызывает в виде 2, эта функция DLL или кода ресурса, выгрузки полностью. Она отменяет все функции в DLL, даже в том случае, если они находятся в настоящее время используется другой макрос, независимо от того, какие счетчика. Эта функция вызывает **xlAutoClose**и затем отменяет регистрацию всех функций в DLL-Библиотеке.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameters

_pxModuleText_ (**xltypeStr**)
  
Имя библиотеки DLL.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

В случае успешного выполнения возвращает **значение TRUE** (**xltypeBool**). В случае неудачи возвращает **значение FALSE**.
  
## <a name="remarks"></a>Замечания

> [!NOTE] 
> Не вызывайте эту форму функции от внедрения [xlAutoClose](xlautoclose.md) при попытке отменить регистрацию всех ресурсов DLL-Библиотеку с одной простой функции вызова. Это приводит к рекурсивный вызов **xlAutoClose** и переполнение стека. 
  
### <a name="remember-to-delete-names"></a>Не забудьте удалить имена

Если аргумент _pxFunctionText_ **xlfRegister**указан при регистрации функции DLL-Библиотеку и команды, необходимо явно удалить имена путем вызова **xlfSetName** для каждого из них, пропуск второй аргумент, чтобы функция больше не отображается в Мастер функций. Для получения дополнительных сведений см [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>См. также

- [xlfRegister (����� 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (формы 1)](xlfunregister-form-1.md)
- [Функции API XLM важные и полезные C](essential-and-useful-c-api-xlm-functions.md)

