---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- функция xlUDF [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8f45f800ca50d2a46792e7cf5e00ac25bd099e8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807377"
---
# <a name="xludf"></a>xlUDF

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Вызов пользовательской функции (UDF). Эта функция позволяет DLL для вызова Visual Basic для приложений (VBA) пользовательские функции, функции языка макросов XLM и зарегистрированных функции, содержащиеся в другие надстройки.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Parameters

_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** или **xltypeNum**)
  
Справочник по функции, которому нужно позвонить. Это может быть макрос листа ссылки на ячейки, зарегистрированное имя функции, что строка или идентификатор регистрации функции. Для добавления в функции XLL зарегистрировано с помощью **xlfRegister** или **ЗАРЕГИСТРИРУЙТЕ** с аргумента _pxFunctionText_ указано идентификатор можно получить с помощью **xlfEvaluate** для поиска имени. 
  
_pxArg1..._
  
Ноль или больше аргументов пользовательских функций. При вызове этой функции в версиях более ранних версий, чем Excel 2007, максимальное число дополнительные аргументы, которые можно передавать — 29, которая является 30 включая _pxFnRef_. Начиная с версии Excel 2007, это ограничение возникает до 254, которая является 255 включая _pxFnRef_.
  
## <a name="return-value"></a>������������ ��������

Возвращает значение, возвращаемое пользовательской функции.
  
## <a name="example"></a>Пример

Следующий пример запускает **TestMacro** на листе Macro1 Книга1. XLS. Убедитесь, что макрос на лист с именем Macro1. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a>См. также

- [Функции интерфейса API для C, которые могут вызываться только из DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

