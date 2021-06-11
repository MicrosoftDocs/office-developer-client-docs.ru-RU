---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- xlautoadd function [Excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413761"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Добавлено Microsoft Excel, когда пользователь активирует XLL во время сеанса Excel с помощью Add-In Manager. Эта функция не называется, Excel запускается и загружает предварительно установленную надстройку.
  
Эта функция может использоваться для отображения настраиваемого диалогового окна, которое сообщает пользователю о том, что надстройка активирована, или для чтения или записи в реестр или проверки сведений о лицензировании, например.
  
Excel XLL не требуется для реализации и экспорта этой функции.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Реализация этой функции должна возвращать 1. (**int**).
  
## <a name="remarks"></a>Примечания

Используйте эту функцию, если XLL должен что-либо сделать, если он добавлен Add-In Manager.
  
## <a name="example"></a>Пример

См.  `\SAMPLES\EXAMPLE\EXAMPLE.C`  `\SAMPLES\GENERIC\GENERIC.C` и, например, реализацию этой функции. Следующий код — из файла `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a>См. также



[xlAutoRemove](xlautoremove.md)


[Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)

