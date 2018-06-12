---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- функция xlfSetName [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807349"
---
# <a name="xlfsetname"></a>xlfSetName

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Используется для создания и удаления определенных имен, связанные с DLL.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Parameters

_pxNameText_ (**xltypeStr**)
  
Имя диапазона, который должен соответствовать типу обычным ограничения в Microsoft Excel в допустимых имен.
  
_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**или **xltypeInt**)
  
(Необязательно). Значение, набор значений, ячейки или диапазона ячеек этой _pxNameText_ определяется как. Если этот параметр опущен, имя будет удален. 
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

_pxRes_ (**xltypeBool** или **xltypeErr**)
  
Значение TRUE, если операция выполнена успешно, или значение FALSE, если имя не может быть создан или удален. Возвращает #VALUE! Если один или несколько аргументов недопустима.
  
## <a name="remarks"></a>Замечания

При команду или функция регистрируется с помощью **xlfRegister** с аргументом допустимый _pxFunctionText_ , Excel создает имя, связанное с DLL-Библиотеку ресурсов. После выгрузки библиотеки DLL, такие имена следует удалить с помощью [функции xlfSetName](xlfsetname.md). Тем не менее из-за известная проблема в Excel, эта операция удаления не удается выполнить. Для получения дополнительных сведений см [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Пример

Просмотр кода для функции **xlAutoClose** в `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>См. также

- [Функции API XLM важные и полезные C](essential-and-useful-c-api-xlm-functions.md)

