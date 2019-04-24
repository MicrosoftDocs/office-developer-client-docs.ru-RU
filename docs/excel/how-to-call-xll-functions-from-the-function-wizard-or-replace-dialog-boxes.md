---
title: Вызов функций XLL из диалоговых окон "Мастер функций" и "замена"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- функции XLL [Excel 2007], вызов из диалогового окна "заменить", диалоговое окно "заменить" [Excel 2007], вызов функций XLL, мастер функций [Excel 2007], вызов функций XLL, функций XLL [Excel 2007], вызов из мастера функций XLL
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11189beed13e2ceb99ef04b7a2f966cb4171915c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304020"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>Вызов функций XLL из диалоговых окон "Мастер функций" и "замена"

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel обычно вызывает функции XLL во время обычного пересчета книги или ее части, если вычисление находится под управлением макроса. Помните, что функция может не располагаться в формуле ячейки, но может быть частью определения именованного диапазона или выражения условного форматирования.
  
Существует два обстоятельства, в которых функция может вызываться из диалогового окна Excel. Один из них — диалоговое окно " **Вставка аргументов функции** ", в котором пользователи могут создавать функции по одному аргументу за раз. Другой — при изменении и повторном вводе формул в Excel в диалоговом окне **заменить** . В диалоговом окне **Вставка аргументов функции** , возможно, вы не хотите, чтобы функция выполнялась нормально. Это может быть вызвано долгим временем выполнения и немедленным использованием диалогового окна. 
  
В диалоговом окне **Вставка функции** и диалоговом окне **Замена** задано имя класса Windows **боса_сдм_ксл**n, где n — число. Windows предоставляет функцию API с расширением **className**, которая получает это имя из дескриптора Windows, типа переменной HWND. Кроме того, она предоставляет другую **** функцию, которая вызывает предоставленную функцию обратного вызова (в библиотеке DLL) один раз для каждого открытого в данный момент окна верхнего уровня.
  
Функция обратного вызова должна выполнять только следующие действия:
  
1. Проверьте, является ли родительский элемент этого окна текущим экземпляром Excel (в случае, если запущено несколько экземпляров).
    
2. Получите имя класса из дескриптора, переданного Windows.
    
3. Убедитесь, что имя класса имеет вид **боса_сдм_ксл**n.
    
4. Если необходимо различать два диалоговых окна, проверьте, содержит ли заголовок диалогового окна некоторый идентифицирующий текст. Заголовок окна получается с помощью **жетвиндовтекст**вызовов Windows API.
    
В приведенном ниже коде на языке C++ показан класс и обратный вызов, передаваемый в Windows, который выполняет эти действия. Это вызывается функциями, которые вызывают проверку, специально для любого из диалоговых окон. 
  
> [!NOTE]
> Названия окон в будущих версиях Excel могут измениться и сделать этот код недействительным. Кроме того, обратите внимание, что установка **виндов_титле_текст** в **null** влияет на игнорирование заголовка окна при поиске обратного вызова. 
  
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

В диалоговом окне **Вставка функции** отсутствует название, поэтому следующая функция передает строку заголовка поиска "", то есть пустую строку, в обратный вызов, чтобы указать, что в окне не должно быть заголовка. 
  
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

