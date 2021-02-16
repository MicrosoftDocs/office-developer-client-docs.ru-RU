---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- Функция xlsheetnm [excel 2007]
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
  
Возвращает имя листа или листа макроса из его внутреннего ИД листа, который содержится во внешней ссылке, или имя текущего листа, если передана внутренняя ссылка.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Параметры

_pxExtref_ (**xltypeRef** или **xltypeSRef)**
  
Ссылка на лист, имя которого необходимо.
  
При передаче внешней ссылки **(xltypeRef)** она должна содержать только ИД листа. Структуры данных, описывая ячейки на этом сайте, игнорируются и не требуются. Если для ИД установлено нулевое значение, **xlSheetNm** возвращает имя текущего листа. 
  
Если вы передаете внутреннюю ссылку (**xltypeSef),** **xlSheetNm** возвращает имя текущего листа. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает имя листа **(xltypeStr)** в  `[Book1]Sheet1` форме.
  
## <a name="example"></a>Пример

В следующем примере отображается имя листа, из которого была вызвана функция. Функция работает правильно, только если она вызвана с листа макроса при выполнении макроса команды XLM. Это вызвано тем, что **вызывается xlcAlert,** который может делать только команды, и его необходимо вызывает с листа, а не из диалоговых окна, меню или панели команд, чтобы **xlfCaller** возвращал ссылку. 
  
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

