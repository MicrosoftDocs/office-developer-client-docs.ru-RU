---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- функция xlsheetid [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807366"
---
# <a name="xlsheetid"></a>xlSheetId

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Находит идентификатор листа именованные таблицы для создания внешних ссылок.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Parameters

_pxSheetName_ (**xltypeStr**)
  
(Необязательно). Имя из книг и листов, которое можно найти сведения о. Если этот параметр опущен, функция **xlSheetId** возвращает идентификатор листа листа активный (передний план). 
  
## <a name="return-value"></a>������������ ��������

Возвращает идентификатор листа в _pxRes -\>val.mref.idSheet_. 
  
> [!NOTE]
> _PxRes -\>val.mref.lpmref_ указатель массив имеет значение NULL после этого вызова, чтобы не требуется для вызова **xlFree** для освобождения объем памяти, этот тип обычно содержит, хотя это и полностью безопасно. 
  
## <a name="remarks"></a>Замечания

Книга, содержащая указанный лист должен быть открыт для использования этой функции. Нет возможности для создания ссылку неоткрытый книги из библиотеки DLL. Дополнительные сведения об использовании **xlSheetId** для создания ссылки на [Управление памятью в Excel](memory-management-in-excel.md) для примеров конструкции **xltypeRef** см. 
  
## <a name="example"></a>Пример

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>См. также

- [xlSheetNm](xlsheetnm.md)
- [Функции интерфейса API для C, которые могут вызываться только из DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

