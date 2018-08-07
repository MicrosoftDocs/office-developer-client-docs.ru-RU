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
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a><span data-ttu-id="9a5e5-104">Вызов функций XLL из диалоговых окон "Мастер функций" и "Замена"</span><span class="sxs-lookup"><span data-stu-id="9a5e5-104">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>

 <span data-ttu-id="9a5e5-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9a5e5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9a5e5-106">Microsoft Excel обычно вызывает функции XLL во время обычных пересчета книги или его части, если расчет управления макроса.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-106">Microsoft Excel usually calls XLL functions during the normal recalculation of the workbook, or a part of it if the calculation is under the control of a macro.</span></span> <span data-ttu-id="9a5e5-107">Помните, что функция не могут находиться в формуле ячейки, но могут быть частью определения именованный диапазон или выражение условного форматирования.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-107">Remember that the function might not reside in a cell formula but might be part of a named range definition, or a conditional formatting expression.</span></span>
  
<span data-ttu-id="9a5e5-108">Существуют две ситуации, в которых функции могут вызываться из диалогового окна с Excel.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-108">There are two circumstances where a function can be called from an Excel dialog box.</span></span> <span data-ttu-id="9a5e5-109">Один — это диалоговое окно **Аргументы функции Вставить** , где пользователи имеют возможность создавать один аргумент вызова функции за раз.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-109">One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time.</span></span> <span data-ttu-id="9a5e5-110">Другое — при формулы изменения и введен в Excel в поле **Заменить** снова.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-110">The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box.</span></span> <span data-ttu-id="9a5e5-111">Для диалогового окна **Вставить функцию аргументов** не может оказаться функции на выполнение в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-111">For the **Paste Function Arguments** dialog box, you might not want your function to execute normally.</span></span> <span data-ttu-id="9a5e5-112">Возможно, занимает много времени на выполнение и снизить использование диалогового окна не требуется.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-112">This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box.</span></span> 
  
<span data-ttu-id="9a5e5-113">Диалоговое окно " **Вставить функцию** " и диалоговое окно **Заменить** иметь n **bosa_sdm_XL**имя класса Windows, где n — число.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-113">Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL**n, where n is a number.</span></span> <span data-ttu-id="9a5e5-114">Windows предоставляет функции API, **GetClassName**, который получает это имя из дескриптора Windows с типом переменной HWND.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-114">Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type.</span></span> <span data-ttu-id="9a5e5-115">Он также предоставляет другой функции **EnumWindows**, которая вызывает функцию заданный обратного вызова (в пределах DLL) один раз для каждого окна верхнего уровня, открытой в текущий момент.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-115">It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.</span></span>
  
<span data-ttu-id="9a5e5-116">Если функция обратного вызова необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9a5e5-116">The callback function needs to perform only the following steps:</span></span>
  
1. <span data-ttu-id="9a5e5-117">Проверьте, если родительский это окно текущего экземпляра Excel (если существует несколько экземпляров).</span><span class="sxs-lookup"><span data-stu-id="9a5e5-117">Check if the parent of this window is the current instance of Excel (in case there are multiple instances running).</span></span>
    
2. <span data-ttu-id="9a5e5-118">Получите имя класса из дескриптор, переданный в операционной системой Windows.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-118">Get the class name from the handle passed in by Windows.</span></span>
    
3. <span data-ttu-id="9a5e5-119">Проверьте, если имя класса n **bosa_sdm_XL**формы.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-119">Check if the class name is of the form **bosa_sdm_XL**n.</span></span>
    
4. <span data-ttu-id="9a5e5-120">Если вам требуется для проведения различия между двумя диалоговых окон, проверьте наличие идентификационные текст Заголовок диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-120">If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text.</span></span> <span data-ttu-id="9a5e5-121">Заголовок окна получены с помощью вызов Windows API **GetWindowText**.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-121">The window title is obtained using the Windows API call **GetWindowText**.</span></span>
    
<span data-ttu-id="9a5e5-122">В следующем коде C++ показан класс и обратного вызова для передачи Windows, который выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-122">The following C++ code shows a class and callback to be passed to Windows that performs these steps.</span></span> <span data-ttu-id="9a5e5-123">Этот процесс называется функциями тест вызова специально для одного из беспокоятся диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-123">This is called by the functions that call test specifically for either of the dialog boxes concerned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9a5e5-124">Заголовки окон будущих версий Excel могут изменить и объявить недействительным этот код.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-124">Window titles of future Excel versions might change and invalidate this code.</span></span> <span data-ttu-id="9a5e5-125">Обратите внимание, что установка **window_title_text** **значения NULL** действует как без учета заголовок окна поиска обратного вызова в.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-125">Note also that setting **window_title_text** to **NULL** has the effect of ignoring window title in the callback search.</span></span> 
  
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

<span data-ttu-id="9a5e5-126">Диалоговое окно " **Вставить функцию** " не имеет название, поэтому следующая функция передает строку заголовка поиска «», то есть пустая строка, обратный вызов означает, что условие соответствия окна не должно быть название.</span><span class="sxs-lookup"><span data-stu-id="9a5e5-126">The **Paste Function** dialog box does not have a title, so the following function passes a search title string of "", that is, an empty string, to the callback to indicate that the match condition is that the window should not have a title.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="9a5e5-127">См. также</span><span class="sxs-lookup"><span data-stu-id="9a5e5-127">See also</span></span>



[<span data-ttu-id="9a5e5-128">Доступ к коду XLL в Excel</span><span class="sxs-lookup"><span data-stu-id="9a5e5-128">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
[<span data-ttu-id="9a5e5-129">����� � Excel �� DLL ��� XLL</span><span class="sxs-lookup"><span data-stu-id="9a5e5-129">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
[<span data-ttu-id="9a5e5-130">���������� XLL-������� ��� Excel 2013</span><span class="sxs-lookup"><span data-stu-id="9a5e5-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

