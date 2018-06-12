---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- функция tempstr12 [excel 2007], функция TempStrConst [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807335"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функции библиотеки Framework, который создает временные **XLOPER и XLOPER12** , который содержит строку **xltypeStr** , используя строку символом null источника в качестве входных данных. Функция выделяет новый буфер памяти и копирует переданной строки в нее. Входной строки не изменятся и поэтому объявлен как **const**.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Parameters

 _STR_
  
Указатель на строке source символом null. В случае **XLOPER**s TempStrConst ограничивает длину строки, представляющие больше 255 байт. В случае **XLOPER12**s TempStr12Const ограничивает длину строки, представляющие более 32 767 символов Юникода.
  
## <a name="return-value"></a>������������ ��������

Возвращает строку **xltypeStr** , содержащий копию буфера переданной строки. 
  
## <a name="remarks"></a>Замечания

Обратите внимание, что строка **XLOPER** функция Framework, **TempStr**, отличающиеся пытается заменить первым символом указанная строка длиной последующие строки. Не всегда безопасных что следует сделать: Microsoft Excel может произойти сбой, если передается строка только для чтения. Этот способ создания временной строки теперь устаревшим способом рабочих **TempStrConst** и **TempStr12** . Таким образом первым символом входной строки обрабатывается как начала строки, то есть, не как длина символов или ввода символов длины. Не следует передавать строк, которые имеют длину символ, закодированный в начале, как можно отнести к непредсказуемым последствиям. 
  
## <a name="example"></a>Пример

В этом примере функция **TempStr12** используется для создания строки для окна сообщения. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке Framework](functions-in-the-framework-library.md)

