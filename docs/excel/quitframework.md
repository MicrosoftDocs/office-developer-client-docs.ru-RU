---
title: QuitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- QuitFramework
keywords:
- функция quitframework
localization_priority: Normal
ms.assetid: d17a3efe-c278-4ef1-b8f9-b958ae012361
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5c4b122b200d9de0cf098d2bc9e2fbd887ad9ff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807313"
---
# <a name="quitframework"></a>QuitFramework

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая отменяет инициализацию библиотеки Framework, который просто повторно инициализирует временные **XLOPER**/ структуры данных**XLOPER12** памяти, что освобождает память, которая уже была распределена. 
  
```cs
short WINAPI QuitFramework(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Эта функция не возвращает значение.
  
## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

