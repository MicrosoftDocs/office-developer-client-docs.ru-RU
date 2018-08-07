---
title: Доступ к дескрипторам основного окна и экземпляра Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- доступ к excel обрабатывает маркеры [Excel 2007], доступ к экземпляры Excel, доступ к дескрипторов окна [Excel 2007], доступ к
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 035cd2a8423e3ab14f4b2ca4b73fbc39641e54d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807274"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Доступ к дескрипторам основного окна и экземпляра Excel

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
В некоторых случаях для программирования в среде Windows, необходимо знать дескриптор экземпляра Microsoft Excel или обрабатывать главного окна. К примеру эти маркеры полезны при создании и отображение настраиваемых диалоговых окон Windows.
  
Существует две функции XLL-только для интерфейса API для C, которые предоставляют доступ к эти маркеры: функция [xlGetInst](xlgetinst.md) и [xlGetHwnd](xlgethwnd.md) работать соответственно. В Win32 все дескрипторы, 32-разрядных целых чисел. Тем не менее когда был разработан **XLOPER** , Windows не 16-разрядной системе. Таким образом структура, допускается только для дескрипторов 16-разрядной. В Win32 при вызове с **Excel4** или **Excel4v**функции **xlGetInst** и **xlGetHwnd** возвратить только низкой полный дескриптор 32-разрядная версия. 
  
В Excel 2007 и более поздних версий при вызове этих функций с помощью [Excel12](excel4-excel12.md) или [Excel12v](excel4v-excel12v.md), возвращенные **XLOPER12** содержит маркер 32-разрядная. 
  
Получение маркера полного экземпляра прост в любой версии Excel, во время его передачи для обратного вызова Windows **DllMain**, который вызывается при загрузке DLL. Запишите этот экземпляр обработчика в глобальную переменную никогда не требуется ли вызовите функцию **xlGetInst** . 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Получение дескриптора главного Excel в Excel 2003 и более ранних версий

Для получения основной дескриптор Excel в Excel 2003 и более ранних версий 32-разрядная версия, необходимо сначала вызовите функцию **xlGetHwnd** для получения низкой word фактический маркер. Затем необходимо выполнять итерацию список окон верхнего уровня, поиск совпадения с возвращенные низкой word. В следующем коде показывается способ. 
  
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

## <a name="see-also"></a>См. также



[Отображение диалоговых окон из библиотеки DLL или XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[���������� XLL-������� ��� Excel 2013](developing-excel-xlls.md)

