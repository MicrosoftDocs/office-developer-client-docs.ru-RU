---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327288"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает сведения о настройке печати для объекта формы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulFlags;
  HDEVMODE hDevMode;
  HDEVNAMES hDevNames;
  ULONG ulFirstPageNumber;
  ULONG ulFPrintAttachments;
} FORMPRINTSETUP, FAR * LPFORMPRINTSETUP;

```

## <a name="members"></a>Элементы

 **ulFlags**
  
> Bitmask флагов, которые контролируют тип строк. Можно использовать следующий флаг:
    
MAPI_UNICODE 
  
> Строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
 **hDevmode**
  
> Перенаправляйся в режим принтера.
    
 **hDevnames**
  
> Переправляйся к пути принтера.
    
 **ulFirstPageNumber**
  
> Номер страницы первой страницы, которая будет напечатана.
    
 **ulFPrintAttachments**
  
> Флаг, который указывает, есть ли вложения для печати. Если для печати есть вложения, то для **члена ulFPrintAttachments** установлено 1. Если нет вложений для печати, она установлена до 0. 
    
## <a name="remarks"></a>Примечания

Структура **FORMPRINTSETUP** используется для описания сведений о настройке печати для объекта формы. Реализация [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) заполняет структуру **FORMPRINTSETUP** и возвращает ее в содержимое выпуска  _lppFormPrintSetup_ **параметра GetPrintSetup**.
  
Если флаг MAPI_UNICODE в параметре  _ulFlags_ **GetPrintSetup,** строки, на которые ссылается **участники hDevmode** и **hDevnames,** должны быть в формате Unicode. В противном случае строки должны быть в формате ANSI. 
  
Зрители форм, реализующие **IMAPIViewContext,** должны выделить структуру **FORMPRINTSETUP** с помощью функции распределения [MAPI MAPIAllocateBuffer,](mapiallocatebuffer.md)но выделить отдельных **участников, hDevMode** и **hDevNames** с функцией Windows [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110). Выпуск памяти обрабатывается аналогичным образом. Члены **hDevMode** и **hDevNames** должны быть освобождены с помощью функции Windows [GlobalFree,](https://go.microsoft.com/fwlink/?LinkId=132108) в то время как структура **FORMPRINTSETUP** должна быть освобождена с помощью функции [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>См. также



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[Структуры MAPI](mapi-structures.md)

