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
ms.openlocfilehash: ff46c58fbb352d56ae3df09d6949cdd5f614673f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808485"
---
# <a name="formprintsetup"></a><span data-ttu-id="7efdb-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="7efdb-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="7efdb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7efdb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7efdb-105">Описывается настройка печати сведения для объекта формы.</span><span class="sxs-lookup"><span data-stu-id="7efdb-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7efdb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7efdb-106">Header file:</span></span>  <br/> |<span data-ttu-id="7efdb-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="7efdb-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="7efdb-108">Members</span><span class="sxs-lookup"><span data-stu-id="7efdb-108">Members</span></span>

 <span data-ttu-id="7efdb-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="7efdb-109">**ulFlags**</span></span>
  
> <span data-ttu-id="7efdb-110">Битовая маска флаги, определяющее тип строки.</span><span class="sxs-lookup"><span data-stu-id="7efdb-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="7efdb-111">Можно использовать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="7efdb-111">The following flag can be used:</span></span>
    
<span data-ttu-id="7efdb-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7efdb-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7efdb-113">Они в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="7efdb-113">The strings are in Unicode format.</span></span> <span data-ttu-id="7efdb-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="7efdb-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7efdb-115">**hDevmode**</span><span class="sxs-lookup"><span data-stu-id="7efdb-115">**hDevmode**</span></span>
  
> <span data-ttu-id="7efdb-116">Обработка режима принтера.</span><span class="sxs-lookup"><span data-stu-id="7efdb-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="7efdb-117">**hDevnames**</span><span class="sxs-lookup"><span data-stu-id="7efdb-117">**hDevnames**</span></span>
  
> <span data-ttu-id="7efdb-118">Обработка путь к принтеру.</span><span class="sxs-lookup"><span data-stu-id="7efdb-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="7efdb-119">**ulFirstPageNumber**</span><span class="sxs-lookup"><span data-stu-id="7efdb-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="7efdb-120">Номер первой страницы для печати.</span><span class="sxs-lookup"><span data-stu-id="7efdb-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="7efdb-121">**ulFPrintAttachments**</span><span class="sxs-lookup"><span data-stu-id="7efdb-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="7efdb-122">Флаг, указывающий, есть ли вложения для печати.</span><span class="sxs-lookup"><span data-stu-id="7efdb-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="7efdb-123">При наличии вложений для печати, член **ulFPrintAttachments** установлено значение 1.</span><span class="sxs-lookup"><span data-stu-id="7efdb-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="7efdb-124">Если нет вложений для печати, он имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="7efdb-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7efdb-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="7efdb-125">Remarks</span></span>

<span data-ttu-id="7efdb-126">Структура **FORMPRINTSETUP** используется для описания сведения об установке печати для объекта формы.</span><span class="sxs-lookup"><span data-stu-id="7efdb-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="7efdb-127">Реализации [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) заполните поля в структуре **FORMPRINTSETUP** и вернуть его в содержимое выходной параметр _lppFormPrintSetup_ из **GetPrintSetup**.</span><span class="sxs-lookup"><span data-stu-id="7efdb-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="7efdb-128">Если флаг MAPI_UNICODE передается в параметре _ulFlags_ **GetPrintSetup**, строки, указанные в элементы **hDevmode** и **hDevnames** должен быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="7efdb-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="7efdb-129">В противном случае строки должны быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="7efdb-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="7efdb-130">Реализация **IMAPIViewContext** средства просмотра формы необходимо выделить структура **FORMPRINTSETUP** , с помощью функции распределителя MAPI [MAPIAllocateBuffer](mapiallocatebuffer.md), но выделить отдельные элементы, **hDevMode** и **hDevNames** с помощью функции Windows [GlobalAlloc](http://go.microsoft.com/fwlink/?LinkId=132110).</span><span class="sxs-lookup"><span data-stu-id="7efdb-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](http://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="7efdb-131">Подобным образом распределяется выпуске памяти.</span><span class="sxs-lookup"><span data-stu-id="7efdb-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="7efdb-132">Члены **hDevMode** и **hDevNames** освобождения с помощью функции Windows [GlobalFree](http://go.microsoft.com/fwlink/?LinkId=132108) , тогда как структура **FORMPRINTSETUP** освобождения с помощью функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7efdb-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](http://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7efdb-133">См. также</span><span class="sxs-lookup"><span data-stu-id="7efdb-133">See also</span></span>



[<span data-ttu-id="7efdb-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="7efdb-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="7efdb-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7efdb-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7efdb-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="7efdb-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="7efdb-137">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="7efdb-137">MAPI Structures</span></span>](mapi-structures.md)

