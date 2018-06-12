---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- функция xlautoadd [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ae0b4ae2d5f5fc58c3e18ffa9d79ec4128cb4639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807333"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Когда пользователь активирует XLL во время сеанса обмена Excel с помощью диспетчера надстроек, добавляемые в Microsoft Excel. Эта функция не вызывается при запуске и загрузка предварительно установленные надстройки Excel.
  
Эта функция может использоваться для отображения настраиваемого диалогового окна, о том, что надстройка была активирована, чтение или запись в реестр или проверьте сведения о лицензировании, например.
  
Excel не требуется XLL внедрение и экспорт этой функции.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Parameters

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Реализация этой функции должен возвращать 1. (**int**).
  
## <a name="remarks"></a>Замечания

Использование этой функции, что-то, что ваше XLL необходимо сделать при добавлении, диспетчер надстроек.
  
## <a name="example"></a>Пример

Просмотреть `\SAMPLES\EXAMPLE\EXAMPLE.C` и `\SAMPLES\GENERIC\GENERIC.C` для примера реализации этой функции. Следующий код является из `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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


[Диспетчер надстроек и функции XLL интерфейса](add-in-manager-and-xll-interface-functions.md)

