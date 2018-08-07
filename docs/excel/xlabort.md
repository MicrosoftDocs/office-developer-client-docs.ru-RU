---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- функция xlAbort [excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e90cbe496404b4cc602dee1ad21c91c8f5f91bfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807342"
---
# <a name="xlabort"></a><span data-ttu-id="d4fce-104">xlAbort</span><span class="sxs-lookup"><span data-stu-id="d4fce-104">xlAbort</span></span>

 <span data-ttu-id="d4fce-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d4fce-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d4fce-106">Возвращает процессор для других задач в системе и проверяет, нажатии пользователем клавиши **ESC** , чтобы отменить макроса.</span><span class="sxs-lookup"><span data-stu-id="d4fce-106">Yields the processor to other tasks in the system and checks whether the user has pressed **ESC** to cancel a macro.</span></span> <span data-ttu-id="d4fce-107">Если пользователь нажата клавиша **ESC** во время пересчета книги, его можно также обнаружен из функции листа путем вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="d4fce-107">If the user has pressed **ESC** during a workbook recalculation, it can also be detected from within a worksheet function by calling this function.</span></span> 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a><span data-ttu-id="d4fce-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4fce-108">Parameters</span></span>

 <span data-ttu-id="d4fce-109">_pxRetain_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="d4fce-109">_pxRetain_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="d4fce-110">(Необязательно).</span><span class="sxs-lookup"><span data-stu-id="d4fce-110">(Optional).</span></span> <span data-ttu-id="d4fce-111">Если **значение FALSE**, эта функция проверяет условия останова и очищает все ожидающие приостановки выполнения.</span><span class="sxs-lookup"><span data-stu-id="d4fce-111">If **FALSE**, this function checks for the break condition and clears any pending break.</span></span> <span data-ttu-id="d4fce-112">Это позволяет пользователю продолжить несмотря на условие приостановки выполнения.</span><span class="sxs-lookup"><span data-stu-id="d4fce-112">This enables the user to continue despite the break condition.</span></span> <span data-ttu-id="d4fce-113">Если этот аргумент указан или имеет **значение TRUE**, функция проверяет наличие прервано пользователем без его очистка.</span><span class="sxs-lookup"><span data-stu-id="d4fce-113">If this argument is omitted or is **TRUE**, the function checks for a user abort without clearing it.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d4fce-114">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4fce-114">Property value/Return value</span></span>

<span data-ttu-id="d4fce-115">Возвращает **значение TRUE** (**xltypeBool**), если нажата **клавиши ESC**.</span><span class="sxs-lookup"><span data-stu-id="d4fce-115">Returns **TRUE** (**xltypeBool**) if the user has pressed **ESC**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d4fce-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d4fce-116">Remarks</span></span>

### 

#### <a name="frequent-calls-may-be-needed"></a><span data-ttu-id="d4fce-117">Часто используемые звонки могут понадобиться</span><span class="sxs-lookup"><span data-stu-id="d4fce-117">Frequent Calls May Be Needed</span></span>

<span data-ttu-id="d4fce-118">Функции и команды, которые может уйти много времени должны вызвать эту функцию часто, чтобы получить процессор для других задач в системе.</span><span class="sxs-lookup"><span data-stu-id="d4fce-118">Functions and commands that could take a long time should call this function frequently to yield the processor to other tasks in the system.</span></span>
  
#### <a name="avoid-sensitive-language"></a><span data-ttu-id="d4fce-119">Избегайте конфиденциальных языка</span><span class="sxs-lookup"><span data-stu-id="d4fce-119">Avoid Sensitive Language</span></span>

<span data-ttu-id="d4fce-120">Избегайте использования термин «Отменить» в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d4fce-120">Avoid using the term "Abort" in your user interface.</span></span> <span data-ttu-id="d4fce-121">Подумайте об использовании «Отмена» «Остановка», «Приостановить» или «Stop». Вместо этого.</span><span class="sxs-lookup"><span data-stu-id="d4fce-121">Consider using "Cancel," "Halt," "Break," or "Stop" instead.</span></span>
  
## <a name="example"></a><span data-ttu-id="d4fce-122">Пример</span><span class="sxs-lookup"><span data-stu-id="d4fce-122">Example</span></span>

<span data-ttu-id="d4fce-123">Приведенный ниже код повторно Перемещает активную ячейку на листе до истечения одну минуту или нажатии клавиши **ESC**.</span><span class="sxs-lookup"><span data-stu-id="d4fce-123">The following code repeatedly moves the active cell on a sheet until one minute has elapsed or until the user presses **ESC**.</span></span> <span data-ttu-id="d4fce-124">Периодически вызывает функцию **xlAbort** .</span><span class="sxs-lookup"><span data-stu-id="d4fce-124">It calls the function **xlAbort** occasionally.</span></span> <span data-ttu-id="d4fce-125">Это дает процессора, замедление совместной многозадачности.</span><span class="sxs-lookup"><span data-stu-id="d4fce-125">This yields the processor, easing cooperative multitasking.</span></span> 
  
 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
int WINAPI fDance(void)
{
   DWORD dtickStart;
   XLOPER12 xAbort, xConfirm;
   int boolSheet;
   int col=0;
   XCHAR rgch[32];
//
// Check what kind of sheet is active. If it is a worksheet or macro
// sheet, this function will move the selection in a loop to show
// activity. In any case, it will update the status bar with a countdown.
//
// Call xlSheetId; if that fails the current sheet is not a macro sheet or
// worksheet. Next, get the time at which to start. Then start a while
// loop that will run for one minute. During the while loop, check if the
// user has pressed ESC. If true, confirm the abort. If the abort is
// confirmed, clear the message bar and return; if the abort is not
// confirmed, clear the abort state and continue. After checking for an
// abort, move the active cell if on a worksheet or macro. Then
// update the status bar with the time remaining.
//
// This block uses TempActiveCell12(), which creates a temporary XLOPER12.
// The XLOPER12 contains a reference to a single cell on the active sheet.
// This function is part of the framework library.
//
   boolSheet = (Excel12f(xlSheetId, 0, 0) == xlretSuccess);
   dtickStart = GetTickCount();
   while (GetTickCount() < dtickStart + 60000L)
   {
      Excel12f(xlAbort, &xAbort, 0);
      if (xAbort.val.xbool)
      {
         Excel12f(xlcAlert, &xConfirm, 2,
           TempStr12(L"Are you sure you want to cancel this operation?"),
              TempNum12(1));
         if (xConfirm.val.xbool)
         {
            Excel12f(xlcMessage, 0, 1, TempBool12(0));
            return 1;
         }
         else
         {
            Excel12f(xlAbort, 0, 1, TempBool12(0));
         }
      }
      if (boolSheet)
      {
         Excel12f(xlcSelect, 0, 1,
            TempActiveCell12(0,(BYTE)col));
         col = (col + 1) & 3;
      }
      wsprintfW(rgch,L"0:%lu",
         (60000 + dtickStart - GetTickCount()) / 1000L);
      Excel12f(xlcMessage, 0, 2, TempBool12(1), TempStr12(rgch));
   }
   Excel12f(xlcMessage, 0, 1, TempBool12(0));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d4fce-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d4fce-126">See also</span></span>



[<span data-ttu-id="d4fce-127">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="d4fce-127">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

