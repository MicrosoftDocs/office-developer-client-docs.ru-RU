---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- Функция xlfsetname [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404262"
---
# <a name="xlfsetname"></a>xlfSetName

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Используется для создания и удаления определенных имен, связанных с DLL.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Параметры

_pxNameText_ (**xltypeStr)**
  
Имя диапазона, которое должно соответствовать обычным ограничениям в Microsoft Excel для допустимого имени.
  
_pxNameDefinition_ (**xltypeStr,** **xltypeNum,** **xltypeBool,** **xltypeErr,** **xltypeMulti,** **xltypeSRef,** **xltypeRef** или **xltypeInt)**
  
(Необязательно). Значение, набор значений, ячейка или диапазон ячеек, как определено _в pxNameText._ Если опущен, имя удаляется. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

_pxRes_ (**xltypeBool** или **xltypeErr)**
  
ИМЕЕТ true, если операция была успешной, или FALSE, если имя не удалось создать или удалить. Возвращает #VALUE! если один или несколько аргументов недействительны.
  
## <a name="remarks"></a>Примечания

При регистрации функции или команды с помощью **xlfRegister** с допустимым аргументом  _pxFunctionText_ Excel создает имя, связанное с ресурсом DLL. При выгрузке DLL такие имена следует удалять с помощью функции [xlfSetName.](xlfsetname.md) Однако из-за известной проблемы в Excel операция удаления не удаться. Дополнительные сведения см. в статье [Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Пример

См. код функции **xlAutoClose** в  `\SAMPLES\GENERIC\GENERIC.C` .
  
## <a name="see-also"></a>См. также

- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

