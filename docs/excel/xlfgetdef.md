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
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422000"
---
# <a name="xlfgetdef"></a>xlfGetDef

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает имя в виде текста, определенное для конкретной области, значения или формулы в книге. В Excel это значение отображается в столбце  "Имя" диалоговых окна диспетчера  имен, которое  отображается при нажатии кнопки "Диспетчер имен" в разделе "Определенные имена" на вкладке **"Формулы".**  Используйте **xlfGetDef,** чтобы получить имя, соответствующее определению. Чтобы получить определение имени, используйте [xlfGetName.](xlfgetname.md)
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Параметры

_pxDefText_ (**xltypeStr)**
  
Это может быть все, на что можно определить имя, включая ссылку, значение, объект или формулу.
  
Ссылки должны быть предоставлены в стиле R1C1, например  `"R3C5"` . Если _pxDefText_ является значением или формулой, нет необходимости включать знак равного значения,  отображаемого в столбце **"Ссылок** на" в диалоговом окне диспетчера имен. Если у  _pxDefText_ несколько имен, **xlfGetDef** возвращает имя. Если имя не соответствует  _pxDefText,_ **xlfGetDef** возвращает значение  `#NAME?` ошибки. 
  
_pxDocumentText_ (**xltypeStr)**
  
Указывает лист, на который установлен _pxDefText._ Если  _pxDocumentText_ опущен, он считается активным листом. 
  
_pxTypeNum_ (**xltypeNum)**
  
Число от 1 до 3, указывав, какие типы имен возвращаются.
  
|**_pxTypeNum_**|**Возвращаемое значение**|
|:-----|:-----|
|1 или пропущено  <br/> |Только обычные имена.  <br/> |
|2   <br/> |Только скрытые имена.  <br/> |
|3   <br/> |Все имена.  <br/> |
   
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

 _pxRes_ (**xltypeStr** или **xltypeErr)**
  
Возвращает имя, связанное с указанным определением.
  
## <a name="remarks"></a>Примечания

В следующей таблице перечислены четыре примера значений, возвращаемого вызовом **xlfGetDef** с указанными аргументами. 
  
|**Имя, определенное в Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Возвращаемая величина**|
|:-----|:-----|:-----|:-----|:-----|
|Указанный диапазон в листе Sheet4 называется Sales.  <br/> |"R2C2:R9C6"  <br/> |"Sheet4"  <br/> |\<опущен\>  <br/> |"Sales" (Продажи)  <br/> |
|Значение 100 в листе Sheet4 определяется как Константа.  <br/> |"100"  <br/> |"Sheet4"  <br/> |\<опущен\>  <br/> |"Constant"  <br/> |
|Указанная формула в листе Sheet4 называется SumTotal.  <br/> |"SUM(R1C1:R10C1)"  <br/> |"Sheet4"  <br/> |\<опущен\>  <br/> |"SumTotal"  <br/> |
|3 определяется как скрытый счетчик имен на активном листе.  <br/> |"3"  <br/> |\<опущен\>  <br/> |2   <br/> |"Counter"  <br/> |
   
## <a name="see-also"></a>См. также

- [xlfGetName](xlfgetname.md)
- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

