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
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a><span data-ttu-id="d43c9-104">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span><span class="sxs-lookup"><span data-stu-id="d43c9-104">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>

 <span data-ttu-id="d43c9-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d43c9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d43c9-106">Microsoft Excel обычно вызывает функции XLL во время обычного пересчета книги или ее части, если расчет находится под контролем макроса.</span><span class="sxs-lookup"><span data-stu-id="d43c9-106">Microsoft Excel usually calls XLL functions during the normal recalculation of the workbook, or a part of it if the calculation is under the control of a macro.</span></span> <span data-ttu-id="d43c9-107">Помните, что функция может не находиться в формуле ячейки, но может быть частью именуемого определения диапазона или условного выражения форматирования.</span><span class="sxs-lookup"><span data-stu-id="d43c9-107">Remember that the function might not reside in a cell formula but might be part of a named range definition, or a conditional formatting expression.</span></span>
  
<span data-ttu-id="d43c9-108">Существует два обстоятельства, при которых функция может быть вызвана из Excel диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="d43c9-108">There are two circumstances where a function can be called from an Excel dialog box.</span></span> <span data-ttu-id="d43c9-109">Один из них **— диалоговое окно Аргументы** функции вклейки, в котором пользователи могут создавать один аргумент по одному вызову функции.</span><span class="sxs-lookup"><span data-stu-id="d43c9-109">One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time.</span></span> <span data-ttu-id="d43c9-110">Другой момент — когда формулы меняются и Excel в диалоговом окне **Replace.**</span><span class="sxs-lookup"><span data-stu-id="d43c9-110">The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box.</span></span> <span data-ttu-id="d43c9-111">В **диалоговом окне Аргументы** функции вклейки может не потребоваться нормальное выполнение функции.</span><span class="sxs-lookup"><span data-stu-id="d43c9-111">For the **Paste Function Arguments** dialog box, you might not want your function to execute normally.</span></span> <span data-ttu-id="d43c9-112">Это может быть потому, что для выполнения требуется много времени, и вы не хотите замедлять использование диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d43c9-112">This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box.</span></span> 
  
<span data-ttu-id="d43c9-113">Диалоговое **окно Функции** вклейки и диалоговое окно **Replace** имеют имя Windows класса **bosa_sdm_XL** n, где n — это номер.</span><span class="sxs-lookup"><span data-stu-id="d43c9-113">Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL** n, where n is a number.</span></span> <span data-ttu-id="d43c9-114">Windows предоставляет функцию API **GetClassName,** которая получает это имя из Windows, типа переменной HWND.</span><span class="sxs-lookup"><span data-stu-id="d43c9-114">Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type.</span></span> <span data-ttu-id="d43c9-115">Кроме того, она предоставляет еще одну функцию **EnumWindows,** которая вызывает поставляемую функцию вызова (в DLL) один раз для каждого открытого окна верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d43c9-115">It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.</span></span>
  
<span data-ttu-id="d43c9-116">Функция вызова должна выполнять только следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d43c9-116">The callback function needs to perform only the following steps:</span></span>
  
1. <span data-ttu-id="d43c9-117">Проверьте, является ли родительский экземпляр этого окна текущим экземпляром Excel (если запущено несколько экземпляров).</span><span class="sxs-lookup"><span data-stu-id="d43c9-117">Check if the parent of this window is the current instance of Excel (in case there are multiple instances running).</span></span>
    
2. <span data-ttu-id="d43c9-118">Получите имя класса из ручки, переданной Windows.</span><span class="sxs-lookup"><span data-stu-id="d43c9-118">Get the class name from the handle passed in by Windows.</span></span>
    
3. <span data-ttu-id="d43c9-119">Проверьте, является ли имя класса формой **bosa_sdm_XL** n.</span><span class="sxs-lookup"><span data-stu-id="d43c9-119">Check if the class name is of the form **bosa_sdm_XL** n.</span></span>
    
4. <span data-ttu-id="d43c9-120">Если необходимо различать два диалоговых окна, проверьте, содержит ли заголовок диалогового окна определенный текст.</span><span class="sxs-lookup"><span data-stu-id="d43c9-120">If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text.</span></span> <span data-ttu-id="d43c9-121">Название окна получается с помощью Windows API **GetWindowText**.</span><span class="sxs-lookup"><span data-stu-id="d43c9-121">The window title is obtained using the Windows API call **GetWindowText**.</span></span>
    
<span data-ttu-id="d43c9-122">В следующем коде C++ показан класс и вызов для передачи Windows, который выполняет эти действия.</span><span class="sxs-lookup"><span data-stu-id="d43c9-122">The following C++ code shows a class and callback to be passed to Windows that performs these steps.</span></span> <span data-ttu-id="d43c9-123">Это вызывается функциями, которые тестировать вызов специально для любого из диалоговых полей, заинтересованных.</span><span class="sxs-lookup"><span data-stu-id="d43c9-123">This is called by the functions that call test specifically for either of the dialog boxes concerned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d43c9-124">Названия окон будущих Excel могут изменить и сделать этот код недействительным.</span><span class="sxs-lookup"><span data-stu-id="d43c9-124">Window titles of future Excel versions might change and invalidate this code.</span></span> <span data-ttu-id="d43c9-125">Обратите внимание также, **что window_title_text** **NULL** имеет эффект игнорирования названия окна в поиске вызова.</span><span class="sxs-lookup"><span data-stu-id="d43c9-125">Note also that setting **window_title_text** to **NULL** has the effect of ignoring window title in the callback search.</span></span> 
  
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

<span data-ttu-id="d43c9-126">Диалоговое **окно Функции** в пасте не имеет названия, поэтому следующая функция передает строку заголовка поиска "", то есть пустую строку, в вызываемую строку, чтобы указать, что условие совпадения состоит в том, что окно не должно иметь заголовка.</span><span class="sxs-lookup"><span data-stu-id="d43c9-126">The **Paste Function** dialog box does not have a title, so the following function passes a search title string of "", that is, an empty string, to the callback to indicate that the match condition is that the window should not have a title.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="d43c9-127">См. также</span><span class="sxs-lookup"><span data-stu-id="d43c9-127">See also</span></span>



[<span data-ttu-id="d43c9-128">Доступ к коду XLL в Excel</span><span class="sxs-lookup"><span data-stu-id="d43c9-128">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
[<span data-ttu-id="d43c9-129">Вызов Excel из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="d43c9-129">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
[<span data-ttu-id="d43c9-130">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="d43c9-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

