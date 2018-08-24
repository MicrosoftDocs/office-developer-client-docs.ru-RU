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
ms.openlocfilehash: 83194b47faf7892d5da568a354921511eb097210
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582954"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывается настройка печати сведения для объекта формы. 
  
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

## <a name="members"></a>Members

 **ulFlags**
  
> Битовая маска флаги, определяющее тип строки. Можно использовать следующий флаг:
    
MAPI_UNICODE 
  
> Они в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 **hDevmode**
  
> Обработка режима принтера.
    
 **hDevnames**
  
> Обработка путь к принтеру.
    
 **ulFirstPageNumber**
  
> Номер первой страницы для печати.
    
 **ulFPrintAttachments**
  
> Флаг, указывающий, есть ли вложения для печати. При наличии вложений для печати, член **ulFPrintAttachments** установлено значение 1. Если нет вложений для печати, он имеет значение 0. 
    
## <a name="remarks"></a>Замечания

Структура **FORMPRINTSETUP** используется для описания сведения об установке печати для объекта формы. Реализации [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) заполните поля в структуре **FORMPRINTSETUP** и вернуть его в содержимое выходной параметр _lppFormPrintSetup_ из **GetPrintSetup**.
  
Если флаг MAPI_UNICODE передается в параметре _ulFlags_ **GetPrintSetup**, строки, указанные в элементы **hDevmode** и **hDevnames** должен быть в формате Юникод. В противном случае строки должны быть в формате ANSI. 
  
Реализация **IMAPIViewContext** средства просмотра формы необходимо выделить структура **FORMPRINTSETUP** , с помощью функции распределителя MAPI [MAPIAllocateBuffer](mapiallocatebuffer.md), но выделить отдельные элементы, **hDevMode** и **hDevNames** с помощью функции Windows [GlobalAlloc](http://go.microsoft.com/fwlink/?LinkId=132110). Подобным образом распределяется выпуске памяти. Члены **hDevMode** и **hDevNames** освобождения с помощью функции Windows [GlobalFree](http://go.microsoft.com/fwlink/?LinkId=132108) , тогда как структура **FORMPRINTSETUP** освобождения с помощью функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>См. также



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[Структуры MAPI](mapi-structures.md)

