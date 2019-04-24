---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- Функция кслаутоадд [Excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303993"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Добавляется Microsoft Excel, когда пользователь активирует XLL во время сеанса Excel с помощью диспетчера надстроек. Эта функция не вызывается при запуске Excel и загрузке предварительно установленной надстройки.
  
Эту функцию можно использовать для отображения настраиваемого диалогового окна, которое сообщает пользователю, что надстройка активирована, а также для чтения или записи в реестр или для проверки сведений о лицензировании, например.
  
Для реализации и экспорта этой функции в Excel не требуется XLL.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Ваша реализация этой функции должна вернуть 1. (**int**).
  
## <a name="remarks"></a>Замечания

Используйте эту функцию, если у вас есть все, что нужно сделать для XLL, когда она добавляется с помощью диспетчера надстроек.
  
## <a name="example"></a>Пример

`\SAMPLES\GENERIC\GENERIC.C` В этой статье приведены `\SAMPLES\EXAMPLE\EXAMPLE.C` примеры реализации этой функции. Следующий код — из файла `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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

