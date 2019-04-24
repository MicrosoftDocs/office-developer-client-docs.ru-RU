---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- Функция дебугпринтф [Excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311006"
---
# <a name="debugprintf"></a>debugPrintf

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая записывает строку байтов с завершающим нулем в активный отладчик с помощью функции **аутпутдебугстринга**в пакете Windows SDK. Если у приложения нет отладчика, системный отладчик отображает строку. Если приложение не имеет отладчика, а системный отладчик неактивен, **дебугпринтф** не выполняет никаких действий. 
  
Эта функция не возвращает значение.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Параметры

 _Лпформат (LPSTR)_
  
Строка формата, которая следует за синтаксисом и правилами, используемыми в функции **спринтф** . 
  
 _указаны_
  
Ноль или более аргументов, которые должны сопоставлять строку формата.
  
## <a name="example"></a>Пример

Эта функция печатает строку, чтобы показать, что элемент управления был передан. Перед компиляцией необходимо определить флаг _DEBUG, иначе эта функция не выполняет никаких действий.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

