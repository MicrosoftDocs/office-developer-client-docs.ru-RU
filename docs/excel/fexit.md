---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- функция fexit [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807247"
---
# <a name="fexit"></a>fExit

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательской команды, выгружает GENERIC.xll. При загрузке GENERIC.xll, он создает пользовательских меню, общая, через который доступ к этой команды. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Parameters

Функция не принимает параметры.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Функция всегда возвращает 1.
  
## <a name="remarks"></a>Замечания

Это инициированных пользователем процедуру, чтобы выйти из GENERIC.xll следует избегать просто вызова `UNREGISTER("GENERIC.XLL")` в этой функции. Это будет принудительно отменить регистрацию всех функций в данной библиотеки DLL, даже в том случае, если они являются зарегистрированными где-либо другим способом. Вместо этого отменить регистрацию функции одному за раз. 
  
### <a name="example"></a>Пример

Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[В универсальные библиотеки DLL](functions-in-the-generic-dll.md)

