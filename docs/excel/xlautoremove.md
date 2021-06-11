---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- функция xlautoremove [Excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425479"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Вызвано Microsoft Excel, когда пользователь отключает XLL во время сеанса Excel с помощью Add-In Manager. Вызов этой функции не выполняется, если сеанс Excel закрывается (правильно или ненормально) при установленной надстройке.
  
Эта функция может использоваться для отображения настраиваемого диалоговое окно, в которое пользователь сообщает, что надстройка отключена, или, например, для чтения или записи в реестр.
  
Excel XLL не требуется для реализации и экспорта этой функции. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Внедрении этой функции должно возвратить значение 1 (**int**).
  
## <a name="remarks"></a>Замечания

Используйте эту функцию, если XLL необходимо выполнить любую задачу, если она удалена Add-In Manager.
  
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

