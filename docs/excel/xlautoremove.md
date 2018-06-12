---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- функция xlautoremove [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 6e5daac21a6d89472a7d84a25e9aeaea56db1ae1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807351"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Вызывается с Microsoft Excel, если пользователь деактивирует XLL во время сеанса обмена Excel с помощью диспетчера надстроек. Эта функция не вызывается при сеанс Excel закрывается, обычно или аварийно, с установленной надстройкой.
  
Эта функция используется для отображения настраиваемого диалогового окна о том, что надстройка отключен, чтение или запись в реестр, например.
  
Excel не требуется XLL внедрение и экспорт этой функции. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Parameters

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Реализация этой функции необходимо вернуть 1 (**int**).
  
## <a name="remarks"></a>Замечания

Эта функция вашей XLL должны быть выполнены все задачи при удалении с диспетчер надстроек.
  
## <a name="example"></a>Пример

Файлы `\SAMPLES\EXAMPLE\EXAMPLE.C` и `\SAMPLES\GENERIC\GENERIC.C` для примера реализации этой функции. Следующий код является из `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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


[Диспетчер надстроек и функции XLL интерфейса](add-in-manager-and-xll-interface-functions.md)

