---
title: Call XLL Functions from the Function Wizard or Replace Dialog Boxes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции xll [Excel 2007], вызов из заменить диалоговое окно, заменить диалоговое окно [Excel 2007], вызов функций XLL, Мастер функций [Excel 2007], вызов функций XLL, функции XLL [Excel 2007], вызов из мастер функций
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11189beed13e2ceb99ef04b7a2f966cb4171915c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410751"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>Call XLL Functions from the Function Wizard or Replace Dialog Boxes

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel обычно вызывает функции XLL во время обычного пересчета книги или ее части, если расчет находится под контролем макроса. Помните, что функция может не находиться в формуле ячейки, но может быть частью именуемого определения диапазона или условного выражения форматирования.
  
Существует два обстоятельства, при которых функция может быть вызвана из Excel диалоговом окне. Один из них **— диалоговое окно Аргументы** функции вклейки, в котором пользователи могут создавать один аргумент по одному вызову функции. Другой момент — когда формулы меняются и Excel в диалоговом окне **Replace.** В **диалоговом окне Аргументы** функции вклейки может не потребоваться нормальное выполнение функции. Это может быть потому, что для выполнения требуется много времени, и вы не хотите замедлять использование диалоговое окно. 
  
Диалоговое **окно Функции** вклейки и диалоговое окно **Replace** имеют имя Windows класса **bosa_sdm_XL** n, где n — это номер. Windows предоставляет функцию API **GetClassName,** которая получает это имя из Windows, типа переменной HWND. Кроме того, она предоставляет еще одну функцию **EnumWindows,** которая вызывает поставляемую функцию вызова (в DLL) один раз для каждого открытого окна верхнего уровня.
  
Функция вызова должна выполнять только следующие действия:
  
1. Проверьте, является ли родительский экземпляр этого окна текущим экземпляром Excel (если запущено несколько экземпляров).
    
2. Получите имя класса из ручки, переданной Windows.
    
3. Проверьте, является ли имя класса формой **bosa_sdm_XL** n.
    
4. Если необходимо различать два диалоговых окна, проверьте, содержит ли заголовок диалогового окна определенный текст. Название окна получается с помощью Windows API **GetWindowText**.
    
В следующем коде C++ показан класс и вызов для передачи Windows, который выполняет эти действия. Это вызывается функциями, которые тестировать вызов специально для любого из диалоговых полей, заинтересованных. 
  
> [!NOTE]
> Названия окон будущих Excel могут изменить и сделать этот код недействительным. Обратите внимание также, **что window_title_text** **NULL** имеет эффект игнорирования названия окна в поиске вызова. 
  
```cs
#define CLASS_NAME_BUFFSIZE  50
#define WINDOW_TEXT_BUFFSIZE  50
// Data structure used as input to xldlg_enum_proc(), called by
// called_from_paste_fn_dlg(), called_from_replace_dlg(), and
// called_from_Excel_dlg(). These functions tell the caller whether
// the current worksheet function was called from one or either of
// these dialog boxes.
typedef struct
{
  bool is_dlg;
  short low_hwnd;
  char *window_title_text; // set to NULL if don't care
}
  xldlg_enum_struct;
// The callback function called by Windows for every top-level window.
BOOL CALLBACK xldlg_enum_proc(HWND hwnd, xldlg_enum_struct *p_enum)
{
// Check if the parent window is Excel.
// Note: Because of the change from MDI (Excel 2010)
// to SDI (Excel 2013), comment out this step in Excel 2013.
  if(LOWORD((DWORD)GetParent(hwnd)) != p_enum->low_hwnd)
    return TRUE; // keep iterating
  char class_name[CLASS_NAME_BUFFSIZE + 1];
//  Ensure that class_name is always null terminated for safety.
  class_name[CLASS_NAME_BUFFSIZE] = 0;
  GetClassName(hwnd, class_name, CLASS_NAME_BUFFSIZE);
//  Do a case-insensitve comparison for the Excel dialog window
//  class name with the Excel version number truncated.
  size_t len; // The length of the window's title text
  if(_strnicmp(class_name, "bosa_sdm_xl", 11) == 0)
  {
// Check if a searching for a specific title string
    if(p_enum->window_title_text) 
    {
// Get the window's title and see if it matches the given text.
      char buffer[WINDOW_TEXT_BUFFSIZE + 1];
      buffer[WINDOW_TEXT_BUFFSIZE] = 0;
      len = GetWindowText(hwnd, buffer, WINDOW_TEXT_BUFFSIZE);
      if(len == 0) // No title
      {
        if(p_enum->window_title_text[0] != 0)
          return TRUE; // No match, so keep iterating
      }
// Window has a title so do a case-insensitive comparison of the
// title and the search text, if provided.
      else if(p_enum->window_title_text[0] != 0
      && _stricmp(buffer, p_enum->window_title_text) != 0)
        return TRUE; // Keep iterating
    }
    p_enum->is_dlg = true;
    return FALSE; // Tells Windows to stop iterating.
  }
  return TRUE; // Tells Windows to continue iterating.
}
```

Диалоговое **окно Функции** в пасте не имеет названия, поэтому следующая функция передает строку заголовка поиска "", то есть пустую строку, в вызываемую строку, чтобы указать, что условие совпадения состоит в том, что окно не должно иметь заголовка. 
  
```cs
bool called_from_paste_fn_dlg(void)
{
    XLOPER xHwnd;
// Calls Excel4, which only returns the low part of the Excel
// main window handle. This is OK for the search however.
    if(Excel4(xlGetHwnd, &xHwnd, 0))
        return false; // Couldn't get it, so assume not
// Search for bosa_sdm_xl* dialog box with no title string.
    xldlg_enum_struct es = {FALSE, xHwnd.val.w, ""};
    EnumWindows((WNDENUMPROC)xldlg_enum_proc, (LPARAM)&es);
    return es.is_dlg;
}
```

## <a name="see-also"></a>См. также



[Доступ к коду XLL в Excel](accessing-xll-code-in-excel.md)
  
[Вызов Excel из библиотеки DLL или XLL](calling-into-excel-from-the-dll-or-xll.md)
  
[Разработка XLL-файлов для Excel](developing-excel-xlls.md)

