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
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424800"
---
# <a name="debugprintf"></a>debugPrintf

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая записывает строку byte-terminated null в активный отладчик с помощью функции Windows SDK **OutputDebugStringA.** Если в приложении нет отладка, системный отладок отображает строку. Если приложение не имеет отладка и системный отладок не активен, **debugPrintf** ничего не делает. 
  
Эта функция не возвращает значение.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Параметры

 _lpFormat (LPSTR)_
  
Строка формата, которая следует за синтаксис и правилами, используемыми с функцией **sprintf.** 
  
 _arguments_
  
Ноль или больше аргументов для совпадения со строкой формата.
  
## <a name="example"></a>Пример

Эта функция печатает строку, чтобы показать, что управление передано в нее. Флаг _DEBUG должен быть определен перед компиляторией, иначе эта функция ничего не делает.
  
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

