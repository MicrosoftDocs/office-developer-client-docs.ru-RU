---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- Функция кслфри [Excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: de1c75ad65acacd44644e9bfb111b30abd0a578e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310222"
---
# <a name="xlfree"></a>xlFree

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Используется для высвобождения ресурсов памяти, выделенных Microsoft Excel при создании возвращаемого значения **XLOPER**/ **XLOPER12** в вызове [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)или [Excel12v](excel4v-excel12v.md). Функция **кслфри** освобождает вспомогательную память и сбрасывает указатель на **значение NULL** , но не уничтожает другие части **XLOPER**/ **XLOPER12**.
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Параметры

 _px_1,..., пкс_н_
  
Одна или несколько разпроцессоров **XLOPER**/ ****, которые должны быть освобождены. В версиях Excel до 2003 максимальное число указателей, которые можно передать: 30. Начиная с Excel 2007, это увеличено до 255.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Эта функция не возвращает значение.
  
## <a name="remarks"></a>Замечания

Необходимо освобождать каждую каждую **** из них, полученную в качестве возвращаемого значения из **Excel4** или **Excel4v** , и каждую **XLOPER12** , полученную в качестве возвращаемого значения из **Excel12** или **Excel12v** , если они имеют один из следующих типов: **кслтипестр **, **XltypeMulti**или **кслтипереф**. Всегда безопаснее освобождать другие типы, даже если они не используют вспомогательную память, если они получены из **Excel4** или **Excel12**.
  
Где вы возвращаете в Excel указатель на объект ****/ **XLOPER12** , который по-прежнему содержит выделенную для Excel память, необходимо настроить **кслбиткслфри** , чтобы приложение Excel освободило память. 
  
## <a name="example"></a>Пример

В этом примере вызывается **Get. WORKSPACE (1)** для возврата платформы, на которой в данный момент работает Excel в виде строки. Код копирует возвращаемую строку в буфер для последующего использования. Код поместит буфер обратно в **XLOPER12** для последующего использования с функцией Excel. И, наконец, код отображает строку в окне оповещения. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>См. также

- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

