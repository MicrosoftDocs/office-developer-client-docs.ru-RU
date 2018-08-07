---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807369"
---
# <a name="xlfgetdef"></a>xlfGetDef

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает имя, в виде текста, определенное для конкретной области, значение или формулу в книге. В Excel, это значение отображается в столбце **имя** диалогового окна **Диспетчер имен** , которая отображается при нажатии кнопки **Диспетчер имен** в разделе **Определенные имена** на вкладке **формул** использования **xlfGetDef** для получения имя, соответствующее определение. Чтобы получить определения имени, используйте [xlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Параметры

_pxDefText_ (**xltypeStr**)
  
Может быть любым можно определить имя для ссылки, включая ссылки, значение, объект или формулы.
  
Справочные материалы должно быть задано в формате R1C1, таких как `"R3C5"`. Если _pxDefText_ значение или формула, не нужно добавить знак равенства, который отображается в столбце **Относится к** в диалоговом окне **Диспетчер имен** . При наличии более одного имени для _pxDefText_, **xlfGetDef** возвращает имя. Если имя не соответствует _pxDefText_, **xlfGetDef** возвращает `#NAME?` значение ошибки. 
  
_pxDocumentText_ (**xltypeStr**)
  
Указывает листа, _pxDefText_ включен. Если _pxDocumentText_ указан, то предполагается, что оно является активный лист. 
  
_pxTypeNum_ (**xltypeNum**)
  
Число от 1 до 3, определяющее, какие типы имен возвращаются.
  
|**_pxTypeNum_**|**Возвращаемое значение**|
|:-----|:-----|
|1 или опущен  <br/> |Только обычный имена.  <br/> |
|2  <br/> |Только скрытые имена.  <br/> |
|3  <br/> |Все имена.  <br/> |
   
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

 _pxRes_ (**xltypeStr** или **xltypeErr**)
  
Возвращает имя, связанное с указанным определением.
  
## <a name="remarks"></a>Замечания

Ниже перечислены четыре примеры значений, возвращаемых вызовом **xlfGetDef** с заданными параметрами. 
  
|**Имя, определенное в Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Возвращаемое значение**|
|:-----|:-----|:-----|:-----|:-----|
|Указанный диапазон в Лист4 именем Sales.  <br/> |«R2C2:R9C6»  <br/> |«Лист4»  <br/> |\<опускается, если\>  <br/> |«Продажи»  <br/> |
|Значение 100 в Лист4 определяется как константа.  <br/> |«100»  <br/> |«Лист4»  <br/> |\<опускается, если\>  <br/> |«Константу»  <br/> |
|Указанную формулу в Лист4 называется SumTotal.  <br/> |«SUM(R1C1:R10C1)»  <br/> |«Лист4»  <br/> |\<опускается, если\>  <br/> |«SumTotal»  <br/> |
|3 — это скрытый имя счетчика на активном листе.  <br/> |«3»  <br/> |\<опускается, если\>  <br/> |2  <br/> |«Счетчик»  <br/> |
   
## <a name="see-also"></a>См. также

- [xlfGetName](xlfgetname.md)
- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

