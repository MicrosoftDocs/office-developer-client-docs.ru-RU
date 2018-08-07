---
title: Вызов функций XLL из диалоговых окон "Мастер функций" и "Замена"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции XLL [excel 2007], вызов из диалоговое окно "Заменить", диалоговое окно Заменить поле [Excel 2007] вызывать функции XLL, Мастер функций [Excel 2007], вызов функции XLL, функции XLL [Excel 2007], вызов из Мастер функций
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7ebb33a5b98cebedfca7fb5923e62486bfd85696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807271"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>Вызов функций XLL из диалоговых окон "Мастер функций" и "Замена"

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel обычно вызывает функции XLL во время обычных пересчета книги или его части, если расчет управления макроса. Помните, что функция не могут находиться в формуле ячейки, но могут быть частью определения именованный диапазон или выражение условного форматирования.
  
Существуют две ситуации, в которых функции могут вызываться из диалогового окна с Excel. Один — это диалоговое окно **Аргументы функции Вставить** , где пользователи имеют возможность создавать один аргумент вызова функции за раз. Другое — при формулы изменения и введен в Excel в поле **Заменить** снова. Для диалогового окна **Вставить функцию аргументов** не может оказаться функции на выполнение в обычном режиме. Возможно, занимает много времени на выполнение и снизить использование диалогового окна не требуется. 
  
Диалоговое окно " **Вставить функцию** " и диалоговое окно **Заменить** иметь n **bosa_sdm_XL**имя класса Windows, где n — число. Windows предоставляет функции API, **GetClassName**, который получает это имя из дескриптора Windows с типом переменной HWND. Он также предоставляет другой функции **EnumWindows**, которая вызывает функцию заданный обратного вызова (в пределах DLL) один раз для каждого окна верхнего уровня, открытой в текущий момент.
  
Если функция обратного вызова необходимо выполнить следующие действия:
  
1. Проверьте, если родительский это окно текущего экземпляра Excel (если существует несколько экземпляров).
    
2. Получите имя класса из дескриптор, переданный в операционной системой Windows.
    
3. Проверьте, если имя класса n **bosa_sdm_XL**формы.
    
4. Если вам требуется для проведения различия между двумя диалоговых окон, проверьте наличие идентификационные текст Заголовок диалогового окна. Заголовок окна получены с помощью вызов Windows API **GetWindowText**.
    
В следующем коде C++ показан класс и обратного вызова для передачи Windows, который выполняет следующие действия. Этот процесс называется функциями тест вызова специально для одного из беспокоятся диалоговых окон. 
  
> [!NOTE]
> Заголовки окон будущих версий Excel могут изменить и объявить недействительным этот код. Обратите внимание, что установка **window_title_text** **значения NULL** действует как без учета заголовок окна поиска обратного вызова в. 
  
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

Диалоговое окно " **Вставить функцию** " не имеет название, поэтому следующая функция передает строку заголовка поиска «», то есть пустая строка, обратный вызов означает, что условие соответствия окна не должно быть название. 
  
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
  
[����� � Excel �� DLL ��� XLL](calling-into-excel-from-the-dll-or-xll.md)
  
[���������� XLL-������� ��� Excel 2013](developing-excel-xlls.md)

