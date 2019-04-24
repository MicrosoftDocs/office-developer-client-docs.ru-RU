---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- Функция фексит [Excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310859"
---
# <a name="fexit"></a>fExit

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательской команды, которая выгружает GENERIC. XLL. При загрузке GENERIC. XLL создается пользовательское меню с общим доступом, через которое осуществляется доступ к этой команде. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Параметры

Функция не принимает параметры.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Функция всегда возвращает 1.
  
## <a name="remarks"></a>Замечания

Эта процедура вызывается пользователем для выхода из УНИВЕРСАЛЬНого объекта. XLL, поэтому не следует `UNREGISTER("GENERIC.XLL")` просто вызывать эту функцию. При этом будут принудительно отменены все функции в этой библиотеке DLL, даже если они были зарегистрированы в другом месте. Вместо этого отмените регистрацию функций по одному. 
  
### <a name="example"></a>Пример

Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

