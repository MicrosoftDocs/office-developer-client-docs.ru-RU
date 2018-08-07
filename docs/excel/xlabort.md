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
# <a name="xlabort"></a>xlAbort

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает процессор для других задач в системе и проверяет, нажатии пользователем клавиши **ESC** , чтобы отменить макроса. Если пользователь нажата клавиша **ESC** во время пересчета книги, его можно также обнаружен из функции листа путем вызова этой функции. 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a>Параметры

 _pxRetain_ (**xltypeBool**)
  
(Необязательно). Если **значение FALSE**, эта функция проверяет условия останова и очищает все ожидающие приостановки выполнения. Это позволяет пользователю продолжить несмотря на условие приостановки выполнения. Если этот аргумент указан или имеет **значение TRUE**, функция проверяет наличие прервано пользователем без его очистка.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Возвращает **значение TRUE** (**xltypeBool**), если нажата **клавиши ESC**.
  
## <a name="remarks"></a>Замечания

### 

#### <a name="frequent-calls-may-be-needed"></a>Часто используемые звонки могут понадобиться

Функции и команды, которые может уйти много времени должны вызвать эту функцию часто, чтобы получить процессор для других задач в системе.
  
#### <a name="avoid-sensitive-language"></a>Избегайте конфиденциальных языка

Избегайте использования термин «Отменить» в пользовательском интерфейсе. Подумайте об использовании «Отмена» «Остановка», «Приостановить» или «Stop». Вместо этого.
  
## <a name="example"></a>Пример

Приведенный ниже код повторно Перемещает активную ячейку на листе до истечения одну минуту или нажатии клавиши **ESC**. Периодически вызывает функцию **xlAbort** . Это дает процессора, замедление совместной многозадачности. 
  
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

