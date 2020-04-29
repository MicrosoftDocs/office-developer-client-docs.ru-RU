---
title: Доступ к дескрипторам основного окна и экземпляра Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- доступ к дескрипторам Excel, дескрипторам [Excel 2007], доступу, экземплярам Excel, доступу, доступу, дескрипторам окон [Excel 2007], доступу
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
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="075aa-104">Доступ к дескрипторам основного окна и экземпляра Excel</span><span class="sxs-lookup"><span data-stu-id="075aa-104">Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="075aa-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="075aa-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="075aa-106">Чтобы программировать в среде Windows, иногда необходимо знать дескриптор экземпляра Microsoft Excel или дескриптор главного окна.</span><span class="sxs-lookup"><span data-stu-id="075aa-106">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle.</span></span> <span data-ttu-id="075aa-107">Например, эти дескрипторы удобно использовать при создании и отображении настраиваемых диалоговых окон Windows.</span><span class="sxs-lookup"><span data-stu-id="075aa-107">For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="075aa-108">Существует две функции API C, которые обеспечивают доступ к этим дескрипторам: функция [кслжетинст](xlgetinst.md) и функция [кслжесвнд](xlgethwnd.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="075aa-108">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively.</span></span> <span data-ttu-id="075aa-109">В Win32 все дескрипторы являются 32 — битным целым числом.</span><span class="sxs-lookup"><span data-stu-id="075aa-109">In Win32, all handles are 32-bit integers.</span></span> <span data-ttu-id="075aa-110">Тем не менее, когда была разработана **XLOPER** , Windows была 16 – разрядной системой.</span><span class="sxs-lookup"><span data-stu-id="075aa-110">However, when the **XLOPER** was designed, Windows was a 16-bit system.</span></span> <span data-ttu-id="075aa-111">Таким образом, структура доступна только для 16 – разрядных дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="075aa-111">Therefore, the structure only allowed for 16-bit handles.</span></span> <span data-ttu-id="075aa-112">В Win32 при вызове с **Excel4** или **Excel4v**функция **кслжетинст** и функция **кслжесвнд** возвращают только младшую часть всего 32 бит.</span><span class="sxs-lookup"><span data-stu-id="075aa-112">In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="075aa-113">В Excel 2007 и более поздних версиях, когда эти функции вызываются с помощью [Excel12](excel4-excel12.md) или [Excel12v](excel4v-excel12v.md), возвращаемое значение **XLOPER12** содержит полный 32 разрядный дескриптор.</span><span class="sxs-lookup"><span data-stu-id="075aa-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="075aa-114">Получение полного дескриптора экземпляра является простым в любой версии Excel, так как оно передается в **DllMain**функции обратного вызова Windows, которая вызывается при загрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="075aa-114">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded.</span></span> <span data-ttu-id="075aa-115">Если вы записываете этот дескриптор экземпляра в глобальную переменную, вам не придется вызывать функцию **кслжетинст** .</span><span class="sxs-lookup"><span data-stu-id="075aa-115">If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="075aa-116">Получение основного дескриптора Excel в Excel 2003 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="075aa-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="075aa-117">Чтобы получить основной дескриптор Excel в Excel 2003 и более ранних версий 32 — более ранних версий, сначала необходимо вызвать функцию **кслжесвнд** , чтобы получить минимальное слово реального маркера.</span><span class="sxs-lookup"><span data-stu-id="075aa-117">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle.</span></span> <span data-ttu-id="075aa-118">Затем необходимо выполнить итерацию списка окон верхнего уровня, чтобы найти сравнение с возвращаемым небольшим словом.</span><span class="sxs-lookup"><span data-stu-id="075aa-118">Then, you must iterate the list of top-level windows to search for a match with the returned low word.</span></span> <span data-ttu-id="075aa-119">В приведенном ниже коде показан метод.</span><span class="sxs-lookup"><span data-stu-id="075aa-119">The following code illustrates the technique.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="075aa-120">См. также</span><span class="sxs-lookup"><span data-stu-id="075aa-120">See also</span></span>



[<span data-ttu-id="075aa-121">Отображение диалоговых окон из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="075aa-121">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="075aa-122">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="075aa-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="075aa-123">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="075aa-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

