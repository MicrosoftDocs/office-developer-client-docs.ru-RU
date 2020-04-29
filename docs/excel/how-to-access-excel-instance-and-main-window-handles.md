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
# <a name="access-excel-instance-and-main-window-handles"></a>Доступ к дескрипторам основного окна и экземпляра Excel

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Чтобы программировать в среде Windows, иногда необходимо знать дескриптор экземпляра Microsoft Excel или дескриптор главного окна. Например, эти дескрипторы удобно использовать при создании и отображении настраиваемых диалоговых окон Windows.
  
Существует две функции API C, которые обеспечивают доступ к этим дескрипторам: функция [кслжетинст](xlgetinst.md) и функция [кслжесвнд](xlgethwnd.md) соответственно. В Win32 все дескрипторы являются 32 — битным целым числом. Тем не менее, когда была разработана **XLOPER** , Windows была 16 – разрядной системой. Таким образом, структура доступна только для 16 – разрядных дескрипторов. В Win32 при вызове с **Excel4** или **Excel4v**функция **кслжетинст** и функция **кслжесвнд** возвращают только младшую часть всего 32 бит. 
  
В Excel 2007 и более поздних версиях, когда эти функции вызываются с помощью [Excel12](excel4-excel12.md) или [Excel12v](excel4v-excel12v.md), возвращаемое значение **XLOPER12** содержит полный 32 разрядный дескриптор. 
  
Получение полного дескриптора экземпляра является простым в любой версии Excel, так как оно передается в **DllMain**функции обратного вызова Windows, которая вызывается при загрузке библиотеки DLL. Если вы записываете этот дескриптор экземпляра в глобальную переменную, вам не придется вызывать функцию **кслжетинст** . 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Получение основного дескриптора Excel в Excel 2003 и более ранних версиях

Чтобы получить основной дескриптор Excel в Excel 2003 и более ранних версий 32 — более ранних версий, сначала необходимо вызвать функцию **кслжесвнд** , чтобы получить минимальное слово реального маркера. Затем необходимо выполнить итерацию списка окон верхнего уровня, чтобы найти сравнение с возвращаемым небольшим словом. В приведенном ниже коде показан метод. 
  
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

## <a name="see-also"></a>См. также



[Отображение диалоговых окон из библиотеки DLL или XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Разработка XLL-файлов для Excel](developing-excel-xlls.md)

