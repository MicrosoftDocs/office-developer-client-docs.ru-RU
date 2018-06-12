---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- функция xlFree [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807361"
---
# <a name="xlfree"></a>xlFree

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Используется, чтобы освободить память, ресурсы, выделенные Microsoft Excel при создании возвращаемое значение **XLOPER**/ **XLOPER12** к вызову [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)или [Excel12v](excel4v-excel12v.md). Функция **xlFree** освобождает память, дополнительный и сбрасывает указатель на **значение NULL** , но не уничтожает другим частям **XLOPER**/ **XLOPER12**.
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Parameters

 _px_1,..., px_n_
  
Один или несколько **XLOPER**/ **XLOPER12**s, чтобы освободить. В версиях Excel до 2003 максимальное число указателей, может быть передан: 30. Начиная с версии Excel 2007, это увеличивается до 255.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Эта функция не возвращает значение.
  
## <a name="remarks"></a>Замечания

Необходимо освободить каждые **XLOPER** , получаемые как возвращаемое значение из **Excel4** или **Excel4v** и каждые **XLOPER12** , который можно получить как возвращаемое значение от **Excel12** или **Excel12v** если они находятся на один из следующих типов: **xltypeStr **, **xltypeMulti**или **xltypeRef**. Всегда безопасно Бесплатная загрузка других типов даже в том случае, если не используют дополнительный объем памяти до тех пор, пока полученный в **Excel4** или **Excel12**.
  
Где возвращается в Excel указатель **XLOPER**/ **XLOPER12** , по-прежнему содержит памяти Excel, выделенный для освобождения, необходимо установить **xlbitXLFree** для обеспечения выпуски Excel объем памяти. 
  
## <a name="example"></a>Пример

В этом примере вызывается **ПОЛУЧИТЕ. WORKSPACE(1)** для возврата платформу, на какие Excel — в настоящее время работает в виде строки. Код копирует этот возвращенный строки в буфер для дальнейшего использования. Код помещает буфера обратно в **XLOPER12** для дальнейшего использования с помощью функции Excel. И, наконец код отображает строку сообщение об ошибке. 
  
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

- [Функции интерфейса API для C, которые могут вызываться только из DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

