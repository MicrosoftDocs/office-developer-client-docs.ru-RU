---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- Функция кслшитнм [Excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5d62be7ebef71547de3a903db4c1a030984b8640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303873"
---
# <a name="xlsheetnm"></a>xlSheetNm

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает имя листа или листа макроса из внутреннего идентификатора листа, содержащегося во внешней ссылке, или имя текущего листа при передаче внутренней ссылки.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Параметры

_пксекстреф_ (**кслтипереф** или **кслтипесреф**)
  
Ссылка на лист, имя которого требуется получить.
  
При передаче внешней ссылки (**кслтипереф**) она должна содержать только идентификатор листа. Структуры данных, описывающие ячейки на листе, игнорируются и не обязательно должны быть предоставлены. Если для идентификатора задано значение 0, **кслшитнм** возвращает имя текущего листа. 
  
При передаче внутренней ссылки (**кслтипесеф**) **кслшитнм** возвращает имя текущего листа. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает имя листа (**кслтипестр**) в форме `[Book1]Sheet1`.
  
## <a name="example"></a>Пример

В приведенном ниже примере отображается имя листа, из которого вызывалась функция. Функция работает правильно только в том случае, если она вызывается из листа макросов во время выполнения командного макроса XLM. Это вызвано тем, что он вызывает **кслкалерт**, который может выполнять только команды, и его необходимо вызывать из листа, а не с помощью диалогового окна, меню или панели команд, чтобы **xlfCaller** возвращал ссылку. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a>См. также

- [xlSheetId](xlsheetid.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

