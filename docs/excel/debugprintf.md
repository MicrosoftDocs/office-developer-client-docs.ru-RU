---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- функция debugprintf [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807146"
---
# <a name="debugprintf"></a>debugPrintf

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая записывает символом null байтов строку активного отладчика с помощью пакета SDK Windows функция **OutputDebugStringA**. Если приложение не отладчик, отладчик система отображает строку. Если приложение имеет отладчик не и отладчик система не активен, **debugPrintf** не имеет никакого эффекта. 
  
Эта функция не возвращает значение.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Параметры

 _lpFormat (LPSTR)_
  
Строка формата образом синтаксис и правила, которые используются с **достаточен** . 
  
 _аргументы_
  
Ноль или больше аргументов в соответствии с строку формата.
  
## <a name="example"></a>Пример

Эта функция печатает строку, которую нужно показать, что элемент управления был передан на него. Перед компиляцией необходимо определить флаг _DEBUG, или же эта функция не выполняет никаких действий.
  
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

