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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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
  
> Битоваяmas флагов, которая управляет типом строк. Можно использовать следующий флаг:
    
MAPI_UNICODE 
  
> Строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 **hDevmode**
  
> Обработка режима принтера.
    
 **hDevnames**
  
> Обработать путь принтера.
    
 **ulFirstPageNumber**
  
> Номер страницы первой страницы для печати.
    
 **ulFPrintAttachments**
  
> Флаг, который указывает, есть ли вложения для печати. Если для печати есть вложения, для члена **ulFPrintAttachments** устанавливается 1. Если вложений для печати нет, для него устанавливается 0. 
    
## <a name="remarks"></a>Примечания

Структура **FORMPRINTSETUP** используется для описания сведений о настройке печати для объекта формы. Реализации [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) заполняют структуру **FORMPRINTSETUP** и возвращают ее в содержимом выходного параметра  _lppFormPrintSetup_ **getPrintSetup**.
  
Если флаг MAPI_UNICODE передается в  _параметре ulFlags_ **getPrintSetup,** строки, на которые ссылается **hDevmode** и **hDevnames,** должны иметь формат Юникод. В противном случае строки должны быть в формате ANSI. 
  
Средства просмотра форм, реализующие **IMAPIViewContext,** должны выделять структуру **FORMPRINTSETUP** с помощью функции mapI allocator [MAPIAllocateBuffer,](mapiallocatebuffer.md)но выделять отдельные **члены, hDevMode** и **hDevNames** с функцией Windows [GlobalAlloc.](https://go.microsoft.com/fwlink/?LinkId=132110) Выпуск памяти обрабатывается аналогично. Члены **hDevMode** и **hDevNames** должны быть освобождены с помощью функции Windows [GlobalFree,](https://go.microsoft.com/fwlink/?LinkId=132108) тогда как структура **FORMPRINTSETUP** должна быть освобождена с помощью функции [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>См. также



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[Структуры MAPI](mapi-structures.md)

