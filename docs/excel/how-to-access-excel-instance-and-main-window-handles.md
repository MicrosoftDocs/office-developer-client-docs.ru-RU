---
title: Обработки Excel экземпляров и главных окон
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- доступ к ручкам Excel, обработкам [Excel 2007 г.),доступ к экземплярам Excel, доступ, ручки окон [Excel 2007 г.], доступ
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4b71ccd428e60c9ba2e59fea0e56eb2fc61390db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310761"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Обработки Excel экземпляров и главных окон

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Чтобы запрограммировать Windows среде, иногда необходимо знать Microsoft Excel экземпляра или основную ручку окна. Например, эти ручки полезны при создании и отображение настраиваемого Windows диалогов.
  
Существует две функции API C API только для XLL, которые предоставляют доступ к этим ручкам: функции [xlGetInst](xlgetinst.md) и [функции xlGetHwnd](xlgethwnd.md) соответственно. В Win32 все ручки — это 32-битные integers. Однако при конструировании **XLOPER** Windows была 16-битной системой. Таким образом, структура разрешена только для 16-битных рули. В Win32 при обращении с **Excel4** или **Excel4v** функция **xlGetInst** и **функция xlGetHwnd** возвращают только низкую часть полной 32-битной ручки. 
  
В Excel 2007 и более поздних версиях, когда эти функции называются [с Excel12](excel4-excel12.md) или [Excel12v,](excel4v-excel12v.md)возвращенная **XLOPER12** содержит полную 32-битную ручку. 
  
Получение ручки полного экземпляра просто в любой версии Excel, так как она передается в Windows **вызова DllMain,** который называется при загрузке DLL. Если вы записывете эту ручку экземпляра в глобальной переменной, вам не нужно вызывать **функцию xlGetInst.** 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Получение главной Excel в Excel 2003 и более ранних

Чтобы получить основную Excel в Excel 2003 и более ранних 32-битных версиях, сначала необходимо вызвать функцию **xlGetHwnd,** чтобы получить низкое слово фактической ручки. Затем необходимо итерировать список окон верхнего уровня для поиска совпадения с возвращенным низким словом. Следующий код иллюстрирует метод. 
  
```cs
typedef struct _EnumStruct
{
  HWND hwnd;  // Return value for Excel main hWnd.
  unsigned short wLoword; //Contains LowWord of the Excel main hWnd
} EnumStruct;
#define CLASS_NAME_BUFFER  50
BOOL CALLBACK EnumProc(HWND hwnd, EnumStruct * pEnum)
{
  // First check the class of the window. Must be "XLMAIN".
  char rgsz[CLASS_NAME_BUFFER];
  GetClassName(hwnd, rgsz, CLASS_NAME_BUFFER);
  if (!lstrcmpi(rgsz, "XLMAIN"))
  {
    // If that hits, check the loword of the window handle.
    if (LOWORD((DWORD) hwnd) == pEnum->wLoword)
    {
      // We have a match, return Excel main hWnd.
      pEnum->hwnd = hwnd;
      return FALSE;
    }
  }
  // No match - continue the enumeration.
  return TRUE;
}
BOOL GetHwnd(HWND * pHwnd)
{
  XLOPER x;
  //
  // xlGetHwnd only returns the LoWord of Excel hWnd
  // so all the windows have to be enumerated to see
  // which match the LoWord returned by xlGetHwnd.
  //
  if (Excel4(xlGetHwnd, &x, 0) == xlretSuccess)
  {
    EnumStruct enm;
    enm.hwnd = NULL;
    enm.wLoword = x.val.w;
    EnumWindows((WNDENUMPROC) EnumProc, (LPARAM) &enm);
    if (enm.hwnd != NULL)
    {
      *pHwnd = enm.hwnd;
      return TRUE;
    }
  }
  return FALSE;
}
```

## <a name="see-also"></a>См. также



[Отображение диалоговых окон из библиотеки DLL или XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Разработка XLL-файлов для Excel](developing-excel-xlls.md)

