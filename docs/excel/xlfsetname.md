---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- Функция xlfSetName [Excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310278"
---
# <a name="xlfsetname"></a>xlfSetName

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Используется для создания и удаления определенных имен, связанных с БИБЛИОТЕКой DLL.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Параметры

_пкснаметекст_ (**кслтипестр**)
  
Имя диапазона, которое должно соответствовать обычным ограничениям в Microsoft Excel по действительным именам.
  
_пкснамедефинитион_ (**кслтипестр**, **кслтипенум**, **кслтипебул**, **кслтипирр**, **xltypeMulti**, **кслтипесреф**, **кслтипереф**или **кслтипеинт**)
  
(НеОбязательно). Значение, набор значений, ячейка или диапазон ячеек, которые _пкснаметекст_ задают как. Если этот параметр не задан, имя удаляется. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

_пксрес_ (**кслтипебул** или **кслтипирр**)
  
ЗНАЧЕНИЕ TRUE, если операция завершилась успешно, или значение FALSE, если имя не удалось создать или удалить. Возвращает #VALUE! Если один или несколько аргументов являются недопустимыми.
  
## <a name="remarks"></a>Замечания

Если функция или команда зарегистрирована с помощью **xlfRegister** с допустимым аргументом _пксфунктионтекст_ , Excel создает имя, связанНОЕ с ресурсом DLL. При выгрузке библиотеки DLL такие имена необходимо удалить с помощью [функции xlfSetName](xlfsetname.md). Однако из-за известной проблемы в Excel эта операция удаления завершается с ошибкой. Дополнительные сведения см. в статье [Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Пример

Обратитесь к коду функции **xlAutoClose** в `\SAMPLES\GENERIC\GENERIC.C`файле.
  
## <a name="see-also"></a>См. также

- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

