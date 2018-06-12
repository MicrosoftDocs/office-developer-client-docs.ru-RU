---
title: Доступ к экземпляру Excel и значками главное окно
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- доступ к excel обрабатывает маркеры [Excel 2007], доступ к экземпляры Excel, доступ к дескрипторов окна [Excel 2007], доступ к
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 035cd2a8423e3ab14f4b2ca4b73fbc39641e54d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807274"
---
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="cae50-104">Доступ к экземпляру Excel и значками главное окно</span><span class="sxs-lookup"><span data-stu-id="cae50-104">Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="cae50-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cae50-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cae50-106">В некоторых случаях для программирования в среде Windows, необходимо знать дескриптор экземпляра Microsoft Excel или обрабатывать главного окна.</span><span class="sxs-lookup"><span data-stu-id="cae50-106">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle.</span></span> <span data-ttu-id="cae50-107">К примеру эти маркеры полезны при создании и отображение настраиваемых диалоговых окон Windows.</span><span class="sxs-lookup"><span data-stu-id="cae50-107">For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="cae50-108">Существует две функции XLL-только для интерфейса API для C, которые предоставляют доступ к эти маркеры: функция [xlGetInst](xlgetinst.md) и [xlGetHwnd](xlgethwnd.md) работать соответственно.</span><span class="sxs-lookup"><span data-stu-id="cae50-108">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively.</span></span> <span data-ttu-id="cae50-109">В Win32 все дескрипторы, 32-разрядных целых чисел.</span><span class="sxs-lookup"><span data-stu-id="cae50-109">In Win32, all handles are 32-bit integers.</span></span> <span data-ttu-id="cae50-110">Тем не менее когда был разработан **XLOPER** , Windows не 16-разрядной системе.</span><span class="sxs-lookup"><span data-stu-id="cae50-110">However, when the **XLOPER** was designed, Windows was a 16-bit system.</span></span> <span data-ttu-id="cae50-111">Таким образом структура, допускается только для дескрипторов 16-разрядной.</span><span class="sxs-lookup"><span data-stu-id="cae50-111">Therefore, the structure only allowed for 16-bit handles.</span></span> <span data-ttu-id="cae50-112">В Win32 при вызове с **Excel4** или **Excel4v**функции **xlGetInst** и **xlGetHwnd** возвратить только низкой полный дескриптор 32-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="cae50-112">In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="cae50-113">В Excel 2007 и более поздних версий при вызове этих функций с помощью [Excel12](excel4-excel12.md) или [Excel12v](excel4v-excel12v.md), возвращенные **XLOPER12** содержит маркер 32-разрядная.</span><span class="sxs-lookup"><span data-stu-id="cae50-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="cae50-114">Получение маркера полного экземпляра прост в любой версии Excel, во время его передачи для обратного вызова Windows **DllMain**, который вызывается при загрузке DLL.</span><span class="sxs-lookup"><span data-stu-id="cae50-114">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded.</span></span> <span data-ttu-id="cae50-115">Запишите этот экземпляр обработчика в глобальную переменную никогда не требуется ли вызовите функцию **xlGetInst** .</span><span class="sxs-lookup"><span data-stu-id="cae50-115">If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="cae50-116">Получение дескриптора главного Excel в Excel 2003 и более ранних версий</span><span class="sxs-lookup"><span data-stu-id="cae50-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="cae50-117">Для получения основной дескриптор Excel в Excel 2003 и более ранних версий 32-разрядная версия, необходимо сначала вызовите функцию **xlGetHwnd** для получения низкой word фактический маркер.</span><span class="sxs-lookup"><span data-stu-id="cae50-117">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle.</span></span> <span data-ttu-id="cae50-118">Затем необходимо выполнять итерацию список окон верхнего уровня, поиск совпадения с возвращенные низкой word.</span><span class="sxs-lookup"><span data-stu-id="cae50-118">Then, you must iterate the list of top-level windows to search for a match with the returned low word.</span></span> <span data-ttu-id="cae50-119">В следующем коде показывается способ.</span><span class="sxs-lookup"><span data-stu-id="cae50-119">The following code illustrates the technique.</span></span> 
  
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
  // which match the LoWord retuned by xlGetHwnd.
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

## <a name="see-also"></a><span data-ttu-id="cae50-120">См. также</span><span class="sxs-lookup"><span data-stu-id="cae50-120">See also</span></span>



[<span data-ttu-id="cae50-121">Отображение диалоговых окон из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="cae50-121">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="cae50-122">Функции интерфейса API для C, которые могут вызываться только из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="cae50-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="cae50-123">���������� XLL-������� ��� Excel 2013</span><span class="sxs-lookup"><span data-stu-id="cae50-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

