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
# <a name="formprintsetup"></a><span data-ttu-id="c7878-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="c7878-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="c7878-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7878-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7878-105">Описывает сведения о настройке печати для объекта формы.</span><span class="sxs-lookup"><span data-stu-id="c7878-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7878-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c7878-106">Header file:</span></span>  <br/> |<span data-ttu-id="c7878-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="c7878-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="c7878-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="c7878-108">Members</span></span>

 <span data-ttu-id="c7878-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c7878-109">**ulFlags**</span></span>
  
> <span data-ttu-id="c7878-110">Bitmask флагов, которые контролируют тип строк.</span><span class="sxs-lookup"><span data-stu-id="c7878-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="c7878-111">Можно использовать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="c7878-111">The following flag can be used:</span></span>
    
<span data-ttu-id="c7878-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c7878-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c7878-113">Строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7878-113">The strings are in Unicode format.</span></span> <span data-ttu-id="c7878-114">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="c7878-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c7878-115">**hDevmode**</span><span class="sxs-lookup"><span data-stu-id="c7878-115">**hDevmode**</span></span>
  
> <span data-ttu-id="c7878-116">Перенаправляйся в режим принтера.</span><span class="sxs-lookup"><span data-stu-id="c7878-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="c7878-117">**hDevnames**</span><span class="sxs-lookup"><span data-stu-id="c7878-117">**hDevnames**</span></span>
  
> <span data-ttu-id="c7878-118">Переправляйся к пути принтера.</span><span class="sxs-lookup"><span data-stu-id="c7878-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="c7878-119">**ulFirstPageNumber**</span><span class="sxs-lookup"><span data-stu-id="c7878-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="c7878-120">Номер страницы первой страницы, которая будет напечатана.</span><span class="sxs-lookup"><span data-stu-id="c7878-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="c7878-121">**ulFPrintAttachments**</span><span class="sxs-lookup"><span data-stu-id="c7878-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="c7878-122">Флаг, который указывает, есть ли вложения для печати.</span><span class="sxs-lookup"><span data-stu-id="c7878-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="c7878-123">Если для печати есть вложения, то для **члена ulFPrintAttachments** установлено 1.</span><span class="sxs-lookup"><span data-stu-id="c7878-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="c7878-124">Если нет вложений для печати, она установлена до 0.</span><span class="sxs-lookup"><span data-stu-id="c7878-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c7878-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7878-125">Remarks</span></span>

<span data-ttu-id="c7878-126">Структура **FORMPRINTSETUP** используется для описания сведений о настройке печати для объекта формы.</span><span class="sxs-lookup"><span data-stu-id="c7878-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="c7878-127">Реализация [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) заполняет структуру **FORMPRINTSETUP** и возвращает ее в содержимое выпуска  _lppFormPrintSetup_ **параметра GetPrintSetup**.</span><span class="sxs-lookup"><span data-stu-id="c7878-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="c7878-128">Если флаг MAPI_UNICODE в параметре  _ulFlags_ **GetPrintSetup,** строки, на которые ссылается **участники hDevmode** и **hDevnames,** должны быть в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7878-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="c7878-129">В противном случае строки должны быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="c7878-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="c7878-130">Зрители форм, реализующие **IMAPIViewContext,** должны выделить структуру **FORMPRINTSETUP** с помощью функции распределения [MAPI MAPIAllocateBuffer,](mapiallocatebuffer.md)но выделить отдельных **участников, hDevMode** и **hDevNames** с функцией Windows [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span><span class="sxs-lookup"><span data-stu-id="c7878-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="c7878-131">Выпуск памяти обрабатывается аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="c7878-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="c7878-132">Члены **hDevMode** и **hDevNames** должны быть освобождены с помощью функции Windows [GlobalFree,](https://go.microsoft.com/fwlink/?LinkId=132108) в то время как структура **FORMPRINTSETUP** должна быть освобождена с помощью функции [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="c7878-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7878-133">См. также</span><span class="sxs-lookup"><span data-stu-id="c7878-133">See also</span></span>



[<span data-ttu-id="c7878-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="c7878-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="c7878-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c7878-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c7878-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c7878-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="c7878-137">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="c7878-137">MAPI Structures</span></span>](mapi-structures.md)

