---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- функция tempstr [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807332"
---
# <a name="tempstr"></a>TempStr

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Устаревшие функции библиотеки Framework, который создает временные **XLOPER** , содержащее строку **xltypeStr** байтов. Строка исходного символом null принимает в качестве входных данных. Она пытается заменить первым символом указанная строка длиной последующие строки. Не всегда безопасных что следует сделать: Microsoft Excel может произойти сбой, если передается строка только для чтения. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Параметры

 _str_
  
Указатель на строке source символом null. **TempStr** ограничивает длину строки, представляющие больше 255 байт. 
  
## <a name="return-value"></a>������������ ��������

Возвращает строку **xltypeStr** , содержащий указатель на буфер переданной строки. 
  
## <a name="remarks"></a>Замечания

Этот способ создания временной строки теперь устаревшим способом обоих рабочих [TempStrConst и TempStr12](tempstrconst-tempstr12.md) . Эти функции выделить новый буфер памяти и скопируйте в него переданной строки. Входные строки для **TempStrConst** и **TempStr12** не изменятся и поэтому объявлен как **const**. С другой стороны ввода строку, которую нужно **TempStr** изменения и поэтому не может быть объявлен как **const**. Первым символом входной строки рассматривается как пространство для знаков длины и перезаписанного этой функции.
  
## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

