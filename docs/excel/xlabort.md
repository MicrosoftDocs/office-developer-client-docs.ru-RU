---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- Функция xlabort [excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08ab69252520e76a5631c5e32a3970d2d95b1ff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436659"
---
# <a name="xlabort"></a>xlAbort

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Передает процессор другим задачам в системе и проверяет, нажал ли пользователь **ESC,** чтобы отменить макрос. Если пользователь нажал **КЛАВИШУ ESC** во время пересчета книги, ее также можно обнаружить из функции таблицы, вызывая эту функцию. 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a>Параметры

 _pxRetain_ (**xltypeBool)**
  
(Необязательно). Если **заложено false,** эта функция проверяет состояние приорва и очищает ожидающих разрывов. Это позволяет пользователю продолжить работу, несмотря на условие приорвать работу. Если этот аргумент опущен или имеет **true,** функция проверяет, не очищает ли пользователь его.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает **true** (**xltypeBool),** если пользователь нажал **ESC.**
  
## <a name="remarks"></a>Примечания

### 

#### <a name="frequent-calls-may-be-needed"></a>Могут потребоваться частые вызовы

Функции и команды, которые могут занять много времени, должны часто вызывать эту функцию, чтобы дать процессору другие задачи в системе.
  
#### <a name="avoid-sensitive-language"></a>Избегайте конфиденциального языка

Избегайте использования термина "Отменить" в пользовательском интерфейсе. Вместо них можно использовать "Отмена", "Остановка", "Приостановка" или "Остановка".
  
## <a name="example"></a>Пример

Следующий код несколько раз перемещает активную ячейку на листе до тех пор, пока не проошел одну минуту или пока пользователь не нажал **клавишу ESC.** Она периодически вызывает **функцию xlAbort.** Это дает процессор, упрощая совместную многозадачность. 
  
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

## <a name="see-also"></a>См. также



[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

