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
  
Возвращает имя в виде текста, которое определяется для определенной области, значения или формулы в книге. В Excel это значение отображается в столбце Имя диалоговое окно **Диспетчер** имен, которое отображается  при нажатии диспетчера имен в разделе **Определенные** имена на вкладке **Формулы.**  Чтобы получить имя, соответствующее определению, используйте **xlfGetDef.** Чтобы получить определение имени, используйте [xlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Parameters

_pxDefText_ **(xltypeStr)**
  
Может быть все, что можно определить имя для ссылки, включая ссылку, значение, объект или формулу.
  
Ссылки должны быть даны в стиле R1C1, например  `"R3C5"` . Если  _pxDefText_ — это значение или формула, необязательно включать равный знак, отображаемый в столбце **Refer To** в диалоговом окне **Диспетчер** имен. Если у  _pxDefText_ несколько имен, **xlfGetDef** возвращает имя. Если имя не совпадает  _с pxDefText,_ **xlfGetDef** возвращает  `#NAME?` значение ошибки. 
  
_pxDocumentText_ **(xltypeStr)**
  
Указывает лист, на который _установлен pxDefText._ Если  _pxDocumentText_ опущен, предполагается, что это активный лист. 
  
_pxTypeNum_ **(xltypeNum)**
  
Число от 1 до 3, указывав, какие типы имен возвращаются.
  
|**_pxTypeNum_**|**Возвращаемое значение**|
|:-----|:-----|
|1 или пропущено  <br/> |Только нормальные имена.  <br/> |
|2  <br/> |Только скрытые имена.  <br/> |
|3  <br/> |Все имена.  <br/> |
   
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

 _pxRes_ **(xltypeStr** или **xltypeErr)**
  
Возвращает имя, связанное с указанным определением.
  
## <a name="remarks"></a>Примечания

В следующей таблице перечислены четыре примера значений, возвращаемых вызовом **xlfGetDef** с указанными аргументами. 
  
|**Имя, определенное в Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Возвращено значение**|
|:-----|:-----|:-----|:-----|:-----|
|Указанный диапазон в Sheet4 называется Sales.  <br/> |"R2C2:R9C6"  <br/> |"Sheet4"  <br/> |\<опущено\>  <br/> |"Продажи"  <br/> |
|Значение 100 в sheet4 определяется как Constant.  <br/> |"100"  <br/> |"Sheet4"  <br/> |\<опущено\>  <br/> |"Константа"  <br/> |
|Указанная формула в Sheet4 называется SumTotal.  <br/> |"SUM(R1C1:R10C1)"  <br/> |"Sheet4"  <br/> |\<опущено\>  <br/> |"SumTotal"  <br/> |
|3 определяется как скрытый счетчик имени на активном листе.  <br/> |"3"  <br/> |\<опущено\>  <br/> |2  <br/> |"Счетчик"  <br/> |
   
## <a name="see-also"></a>См. также

- [xlfGetName](xlfgetname.md)
- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

