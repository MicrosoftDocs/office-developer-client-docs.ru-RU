---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- функция initframework [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2d7e3286d794d6f21da9ef83ca44d18ec242c063
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807256"
---
# <a name="initframework"></a>InitFramework

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, инициализирует библиотеки Framework, который просто инициализирует временные **XLOPER**/ структуры данных**XLOPER12** памяти, что освобождает память, которая уже была распределена. 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>Parameters

Эта функция не имеет аргументов.
  
## <a name="return-value"></a>������������ ��������

Эта функция не возвращает значение.
  
## <a name="example"></a>Пример

В этом примере используется функция **InitFramework** для освобождения всех временной памяти. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке Framework](functions-in-the-framework-library.md)

