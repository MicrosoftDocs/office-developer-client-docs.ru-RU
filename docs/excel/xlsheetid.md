---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- Функция кслшитид [Excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428433"
---
# <a name="xlsheetid"></a>xlSheetId

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Находит идентификатор именованного листа, чтобы создать внешние ссылки.
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>Параметры

_пксшитнаме_ (**кслтипестр**)
  
(Необязательно). Название книги и листа, о которых вы хотите узнать. Если этот параметр опущен, функция **кслшитид** возвращает идентификатор активного (переднего) листа. 
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает идентификатор листа в _пксрес —\>Val. мреф. идшит_. 
  
> [!NOTE]
> После этого вызова в указателе массива _пксрес-\>Val. мреф. лпмреф_ ЗАдается значение null, поэтому нет необходимости вызывать **кслфри** , чтобы освободить память, которую обычно содержит этот тип, хотя это совершенно безопасно для этого. 
  
## <a name="remarks"></a>Примечания

Чтобы использовать эту функцию, необходимо открыть книгу, содержащую указанный лист. Невозможно создать ссылку на неоткрытую книгу из библиотеки DLL. Дополнительные сведения об использовании **кслшитид** для создания ссылок приведены в статье [Управление памятью в Excel](memory-management-in-excel.md) для примера конструкции **кслтипереф** . 
  
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
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

