---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- Функция кслауторемове [Excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310285"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Вызывается Microsoft Excel, когда пользователь отключает XLL во время сеанса Excel с помощью диспетчера надстроек. Вызов этой функции не выполняется, если сеанс Excel закрывается (правильно или ненормально) при установленной надстройке.
  
Эта функция может использоваться для отображения настраиваемого диалогового окна, указывающего на то, что надстройка была отключена, а также для чтения или записи в реестре, например.
  
Для реализации и экспорта этой функции в Excel не требуется XLL. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Внедрении этой функции должно возвратить значение 1 (**int**).
  
## <a name="remarks"></a>Замечания

Используйте эту функцию, если XLL-модуль должен выполнить любую задачу, когда она удалена с помощью диспетчера надстроек.
  
## <a name="example"></a>Пример

В файлах `\SAMPLES\EXAMPLE\EXAMPLE.C` и `\SAMPLES\GENERIC\GENERIC.C` приведены примеры внедрения этой функции. Следующий код — из файла `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a>См. также



[xlAutoAdd](xlautoadd.md)


[Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)

