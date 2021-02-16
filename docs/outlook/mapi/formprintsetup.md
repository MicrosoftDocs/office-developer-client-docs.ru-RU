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
# <a name="formprintsetup"></a><span data-ttu-id="22a34-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="22a34-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="22a34-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22a34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22a34-105">Описывает сведения о настройке печати для объекта формы.</span><span class="sxs-lookup"><span data-stu-id="22a34-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22a34-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="22a34-106">Header file:</span></span>  <br/> |<span data-ttu-id="22a34-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="22a34-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="22a34-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="22a34-108">Members</span></span>

 <span data-ttu-id="22a34-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="22a34-109">**ulFlags**</span></span>
  
> <span data-ttu-id="22a34-110">Битоваяmas флагов, которая управляет типом строк.</span><span class="sxs-lookup"><span data-stu-id="22a34-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="22a34-111">Можно использовать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="22a34-111">The following flag can be used:</span></span>
    
<span data-ttu-id="22a34-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="22a34-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="22a34-113">Строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="22a34-113">The strings are in Unicode format.</span></span> <span data-ttu-id="22a34-114">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="22a34-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="22a34-115">**hDevmode**</span><span class="sxs-lookup"><span data-stu-id="22a34-115">**hDevmode**</span></span>
  
> <span data-ttu-id="22a34-116">Обработка режима принтера.</span><span class="sxs-lookup"><span data-stu-id="22a34-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="22a34-117">**hDevnames**</span><span class="sxs-lookup"><span data-stu-id="22a34-117">**hDevnames**</span></span>
  
> <span data-ttu-id="22a34-118">Обработать путь принтера.</span><span class="sxs-lookup"><span data-stu-id="22a34-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="22a34-119">**ulFirstPageNumber**</span><span class="sxs-lookup"><span data-stu-id="22a34-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="22a34-120">Номер страницы первой страницы для печати.</span><span class="sxs-lookup"><span data-stu-id="22a34-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="22a34-121">**ulFPrintAttachments**</span><span class="sxs-lookup"><span data-stu-id="22a34-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="22a34-122">Флаг, который указывает, есть ли вложения для печати.</span><span class="sxs-lookup"><span data-stu-id="22a34-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="22a34-123">Если для печати есть вложения, для члена **ulFPrintAttachments** устанавливается 1.</span><span class="sxs-lookup"><span data-stu-id="22a34-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="22a34-124">Если вложений для печати нет, для него устанавливается 0.</span><span class="sxs-lookup"><span data-stu-id="22a34-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="22a34-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="22a34-125">Remarks</span></span>

<span data-ttu-id="22a34-126">Структура **FORMPRINTSETUP** используется для описания сведений о настройке печати для объекта формы.</span><span class="sxs-lookup"><span data-stu-id="22a34-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="22a34-127">Реализации [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) заполняют структуру **FORMPRINTSETUP** и возвращают ее в содержимом выходного параметра  _lppFormPrintSetup_ **getPrintSetup**.</span><span class="sxs-lookup"><span data-stu-id="22a34-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="22a34-128">Если флаг MAPI_UNICODE передается в  _параметре ulFlags_ **getPrintSetup,** строки, на которые ссылается **hDevmode** и **hDevnames,** должны иметь формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="22a34-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="22a34-129">В противном случае строки должны быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="22a34-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="22a34-130">Средства просмотра форм, реализующие **IMAPIViewContext,** должны выделять структуру **FORMPRINTSETUP** с помощью функции mapI allocator [MAPIAllocateBuffer,](mapiallocatebuffer.md)но выделять отдельные **члены, hDevMode** и **hDevNames** с функцией Windows [GlobalAlloc.](https://go.microsoft.com/fwlink/?LinkId=132110)</span><span class="sxs-lookup"><span data-stu-id="22a34-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="22a34-131">Выпуск памяти обрабатывается аналогично.</span><span class="sxs-lookup"><span data-stu-id="22a34-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="22a34-132">Члены **hDevMode** и **hDevNames** должны быть освобождены с помощью функции Windows [GlobalFree,](https://go.microsoft.com/fwlink/?LinkId=132108) тогда как структура **FORMPRINTSETUP** должна быть освобождена с помощью функции [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="22a34-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22a34-133">См. также</span><span class="sxs-lookup"><span data-stu-id="22a34-133">See also</span></span>



[<span data-ttu-id="22a34-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="22a34-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="22a34-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="22a34-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="22a34-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="22a34-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="22a34-137">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="22a34-137">MAPI Structures</span></span>](mapi-structures.md)

