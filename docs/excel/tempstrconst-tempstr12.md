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
- функция TempStr12 [Excel 2007], функция Темпстрконст [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d93f9de021c7ba325d9c11af2cede0245ffbbf6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407153"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая создает временную структуру **XLOPER/XLOPER12** , содержащую строку **кслтипестр** , в качестве входных данных принимается строка источника, заканчивающаяся нулем. Функция выделяет новый буфер памяти и копирует переданную строку в нее. Входная строка не изменена, поэтому она объявлена **** как константа.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Параметры

 _str_
  
Указатель на строку источника, заканчивающуюся нулем. В случае **XLOPER**s темпстрконст усекает строки, размер которых превышает 255 байт. В случае **XLOPER12**s TempStr12Const усекает строки, длина которых превышает 32 767 символов Юникода.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает строку **кслтипестр** , содержащую копию переданного строкового буфера. 
  
## <a name="remarks"></a>Примечания

Обратите внимание, что функция Framework структуры **XLOPER** , **темпстр**, работает по-разному и пытается перезаписать первый символ предоставленной строки с длиной следующей строки. Это не всегда является безопасным действием: Microsoft Excel может выполнить сбой, если передать строку, доступную только для чтения. Такой способ создания временных строк теперь является нерекомендуемым в пользу того, как работают как в **темпстрконст** , так и в **TempStr12** . Таким образом, первый символ входной строки обрабатывается как начало строки, то есть не как символ длины или как пробел для знака длины. Не следует передавать строки, закодированные с помощью знака длины, в начале, так как последствия могут быть непредсказуемыми. 
  
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



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

