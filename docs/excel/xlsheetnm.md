---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- xlsheetnm function [Excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5d62be7ebef71547de3a903db4c1a030984b8640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437415"
---
# <a name="xlsheetnm"></a>xlSheetNm

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает имя листа или макроса из его внутреннего ID листа, содержатого во внешней ссылке, или имя текущего листа, если прошло внутреннее упоминание.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Parameters

_pxExtref_ **(xltypeRef** или **xltypeSRef)**
  
Ссылка на лист, имя которого необходимо.
  
Если вы проходите внешнюю ссылку **(xltypeRef),** она должна содержать только ID листа. Структуры данных, описывая ячейки на таблице, игнорируются и не требуются. Если для ID установлено значение нуля, **xlSheetNm** возвращает имя текущего листа. 
  
Если вы передаете внутреннюю ссылку **(xltypeSef),** **xlSheetNm** возвращает имя текущего листа. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает имя листа **(xltypeStr)** в форме  `[Book1]Sheet1` .
  
## <a name="example"></a>Пример

В следующем примере отображается имя листа, из которого была вызвана функция. Функция работает правильно, только если она вызвана с макроса при выполнении макроса команды XLM. Это вызвано тем, что он вызывает **xlcAlert,** который может делать только команды, и его нужно звонить из листа, а не из диалогового окна, меню или панели команд, чтобы **xlfCaller** вернул ссылку. 
  
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

