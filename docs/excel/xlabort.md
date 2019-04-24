---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- функция xlAbort [Excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08ab69252520e76a5631c5e32a3970d2d95b1ff4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310257"
---
# <a name="xlabort"></a><span data-ttu-id="fc119-104">xlAbort</span><span class="sxs-lookup"><span data-stu-id="fc119-104">xlAbort</span></span>

 <span data-ttu-id="fc119-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fc119-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fc119-106">Передает процессор другим задачам в системе и проверяет, нажал ли пользователь клавишу **ESC** для отмены макроса.</span><span class="sxs-lookup"><span data-stu-id="fc119-106">Yields the processor to other tasks in the system and checks whether the user has pressed **ESC** to cancel a macro.</span></span> <span data-ttu-id="fc119-107">Если во время пересчета книги пользователь нажал **клавишу ESC** , его также можно обнаружить в функции листа, вызвав эту функцию.</span><span class="sxs-lookup"><span data-stu-id="fc119-107">If the user has pressed **ESC** during a workbook recalculation, it can also be detected from within a worksheet function by calling this function.</span></span> 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a><span data-ttu-id="fc119-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc119-108">Parameters</span></span>

 <span data-ttu-id="fc119-109">_пксретаин_ (**кслтипебул**)</span><span class="sxs-lookup"><span data-stu-id="fc119-109">_pxRetain_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="fc119-110">(НеОбязательно).</span><span class="sxs-lookup"><span data-stu-id="fc119-110">(Optional).</span></span> <span data-ttu-id="fc119-111">Если задано **значение false**, эта функция проверяет наличие условия останова и удаляет все ожидающие прерывания.</span><span class="sxs-lookup"><span data-stu-id="fc119-111">If **FALSE**, this function checks for the break condition and clears any pending break.</span></span> <span data-ttu-id="fc119-112">Это позволяет пользователю продолжить работу, несмотря на условие останова.</span><span class="sxs-lookup"><span data-stu-id="fc119-112">This enables the user to continue despite the break condition.</span></span> <span data-ttu-id="fc119-113">Если этот аргумент опущен или имеет **значение true**, функция выполняет проверку отмены для пользователя без очистки.</span><span class="sxs-lookup"><span data-stu-id="fc119-113">If this argument is omitted or is **TRUE**, the function checks for a user abort without clearing it.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="fc119-114">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc119-114">Property value/Return value</span></span>

<span data-ttu-id="fc119-115">Возвращает **значение true** (**кслтипебул**), если пользователь нажал клавишу **ESC**.</span><span class="sxs-lookup"><span data-stu-id="fc119-115">Returns **TRUE** (**xltypeBool**) if the user has pressed **ESC**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fc119-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="fc119-116">Remarks</span></span>

### 

#### <a name="frequent-calls-may-be-needed"></a><span data-ttu-id="fc119-117">Может потребоваться частое обращение</span><span class="sxs-lookup"><span data-stu-id="fc119-117">Frequent Calls May Be Needed</span></span>

<span data-ttu-id="fc119-118">Функции и команды, которые могут занять много времени, должны вызывать эту функцию часто, чтобы передавать процессор другим задачам в системе.</span><span class="sxs-lookup"><span data-stu-id="fc119-118">Functions and commands that could take a long time should call this function frequently to yield the processor to other tasks in the system.</span></span>
  
#### <a name="avoid-sensitive-language"></a><span data-ttu-id="fc119-119">Избегайте конфиденциального языка</span><span class="sxs-lookup"><span data-stu-id="fc119-119">Avoid Sensitive Language</span></span>

<span data-ttu-id="fc119-120">Избегайте использования термина "Abort" в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="fc119-120">Avoid using the term "Abort" in your user interface.</span></span> <span data-ttu-id="fc119-121">Вместо этого рекомендуется использовать "Cancel", "остановить", "приостановить", "приостановить" или "остановить".</span><span class="sxs-lookup"><span data-stu-id="fc119-121">Consider using "Cancel," "Halt," "Break," or "Stop" instead.</span></span>
  
## <a name="example"></a><span data-ttu-id="fc119-122">Пример</span><span class="sxs-lookup"><span data-stu-id="fc119-122">Example</span></span>

<span data-ttu-id="fc119-123">Приведенный ниже код многократно перемещает активную ячейку на листе до тех пор, пока не истечет одна минута или пока пользователь не нажмет клавишу **ESC**.</span><span class="sxs-lookup"><span data-stu-id="fc119-123">The following code repeatedly moves the active cell on a sheet until one minute has elapsed or until the user presses **ESC**.</span></span> <span data-ttu-id="fc119-124">Он иногда вызывает функцию **xlAbort** .</span><span class="sxs-lookup"><span data-stu-id="fc119-124">It calls the function **xlAbort** occasionally.</span></span> <span data-ttu-id="fc119-125">Это позволяет процессору замедлению совместной многозадачности.</span><span class="sxs-lookup"><span data-stu-id="fc119-125">This yields the processor, easing cooperative multitasking.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="fc119-126">См. также</span><span class="sxs-lookup"><span data-stu-id="fc119-126">See also</span></span>



[<span data-ttu-id="fc119-127">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="fc119-127">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

