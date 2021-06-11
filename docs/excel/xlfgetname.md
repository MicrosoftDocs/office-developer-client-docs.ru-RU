---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436631"
---
# <a name="xlfgetname"></a>xlfGetName

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает определение имени, как оно отображается  в столбце Ссылается на диалоговое окно **Диспетчер**  имен, которое отображается при нажатии диспетчера имен в разделе **Определенные** имена на вкладке **Формулы.** Если определение содержит ссылки, они даются в качестве ссылок в стиле R1C1. Чтобы проверить значение, определенное именем, используйте **xlfGetName.** Чтобы получить имя, соответствующее определению, используйте [xlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parameters

_pxNameText_ **(xltypeStr)**
  
Может быть именем, определенным на листе; например, внешняя ссылка на имя, определенное в активной книге; или внешняя ссылка на имя, определенное в определенной открытой  `"!Sales"` книге, например  `"[Book1]SHEET1!Sales"` .  _pxNameText также_ может быть скрытым именем. 
  
_pxInfoType_ **(xltypeBool)**
  
Указывает тип сведений, возвращаемой о имени. Если **false** или опущено, определение возвращается. Если **TRUE,** возвращает **TRUE,** если имя определяется только для листа, **FALSE,** если имя определено для всей книги. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

_pxRes_ **(xltypeStr,** **xltypeBool** или **xltypeErr)**
  
В зависимости от значения, переданного _для pxInfoType,_ возвращает определение указанного имени **(xltypeStr),** или **TRUE** или **FALSE** **(xltypeBool).**
  
## <a name="remarks"></a>Примечания

Если  в диалоговом окне Protect **Sheet** для защиты книги, содержащей имя, выбран лист защиты и содержимое заблокированного окна ячейки, **xlfGetName** возвращает значение `#N/A` ошибки. Чтобы просмотреть диалоговое окно **Protect Sheet,** нажмите **кнопку Защитить лист** в разделе **Изменения** вкладки **Обзор.** 
  
В следующей таблице перечислены три примера значений, возвращаемого вызовом **xlfGetDef** с указанным _аргументом pxNameText._ 
  
|**Определение в Excel**|**_pxNameText_**|**Возвращено значение**|
|:-----|:-----|:-----|
|Имя Sales на листе определяется как номер 523.  <br/> |"Продажи"  <br/> |"=523"  <br/> |
|Имя Прибыль на активном листе определяется как формула =Sales-Costs.  <br/> |"! Прибыль"  <br/> |"=Sales-Costs"  <br/> |
|Имя Базы данных на активном листе определяется как диапазон A1:F500.  <br/> |"! База данных"  <br/> |"=R1C1:R500C6"  <br/> |
   
## <a name="see-also"></a>См. также

- [xlfGetDef](xlfgetdef.md)
- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

