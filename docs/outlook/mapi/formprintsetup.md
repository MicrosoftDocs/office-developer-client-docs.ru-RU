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
# <a name="formprintsetup"></a><span data-ttu-id="86657-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="86657-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="86657-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86657-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86657-105">Описывает сведения о настройке печати для объекта Form.</span><span class="sxs-lookup"><span data-stu-id="86657-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86657-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="86657-106">Header file:</span></span>  <br/> |<span data-ttu-id="86657-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="86657-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="86657-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="86657-108">Members</span></span>

 <span data-ttu-id="86657-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="86657-109">**ulFlags**</span></span>
  
> <span data-ttu-id="86657-110">Битовая маска флагов, определяющих тип строк.</span><span class="sxs-lookup"><span data-stu-id="86657-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="86657-111">Можно использовать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="86657-111">The following flag can be used:</span></span>
    
<span data-ttu-id="86657-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="86657-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="86657-113">Строки представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="86657-113">The strings are in Unicode format.</span></span> <span data-ttu-id="86657-114">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="86657-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="86657-115">**хдевмоде**</span><span class="sxs-lookup"><span data-stu-id="86657-115">**hDevmode**</span></span>
  
> <span data-ttu-id="86657-116">Режим обработки принтера.</span><span class="sxs-lookup"><span data-stu-id="86657-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="86657-117">**хдевнамес**</span><span class="sxs-lookup"><span data-stu-id="86657-117">**hDevnames**</span></span>
  
> <span data-ttu-id="86657-118">Ссылка на путь к принтеру.</span><span class="sxs-lookup"><span data-stu-id="86657-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="86657-119">**улфирстпаженумбер**</span><span class="sxs-lookup"><span data-stu-id="86657-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="86657-120">Номер первой страницы, которую необходимо напечатать.</span><span class="sxs-lookup"><span data-stu-id="86657-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="86657-121">**улфпринтаттачментс**</span><span class="sxs-lookup"><span data-stu-id="86657-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="86657-122">Флаг, указывающий на наличие вложений для печати.</span><span class="sxs-lookup"><span data-stu-id="86657-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="86657-123">При наличии вложений для печати для элемента **улфпринтаттачментс** устанавливается значение 1.</span><span class="sxs-lookup"><span data-stu-id="86657-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="86657-124">Если для печати нет вложений, для него задается значение 0.</span><span class="sxs-lookup"><span data-stu-id="86657-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="86657-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="86657-125">Remarks</span></span>

<span data-ttu-id="86657-126">Структура **формпринтсетуп** используется для описания сведений о настройке печати для объекта Form.</span><span class="sxs-lookup"><span data-stu-id="86657-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="86657-127">Реализации [имапивиевконтекст:: жетпринтсетуп](imapiviewcontext-getprintsetup.md) заполните структуру **формпринтсетуп** и верните ее в содержимое выходного параметра _лппформпринтсетуп_ объекта **жетпринтсетуп**.</span><span class="sxs-lookup"><span data-stu-id="86657-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="86657-128">Если флаг MAPI_UNICODE передается в параметре _ulFlags_ объекта **жетпринтсетуп**, то строки, на которые ссылаются элементы **хдевмоде** и **хдевнамес** , должны быть в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="86657-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="86657-129">В противном случае строки должны быть в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="86657-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="86657-130">Средства просмотра форм, реализующие **имапивиевконтекст** , должны выделить структуру **формпринтсетуп** с помощью функции распределителя MAPI [мапиаллокатебуффер](mapiallocatebuffer.md), но выделить отдельные элементы, **Хдевмоде** и **хдевнамес**, с помощью функции Windows [глобалаллок](https://go.microsoft.com/fwlink/?LinkId=132110).</span><span class="sxs-lookup"><span data-stu-id="86657-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="86657-131">Аналогичный выпуск памяти обрабатывается аналогично.</span><span class="sxs-lookup"><span data-stu-id="86657-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="86657-132">Члены **хдевмоде** и **хдевнамес** должны быть освобождены с помощью функции Windows [Глобалфри](https://go.microsoft.com/fwlink/?LinkId=132108) , тогда как структура **формпринтсетуп** должна быть освобождена с помощью функции [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="86657-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86657-133">См. также</span><span class="sxs-lookup"><span data-stu-id="86657-133">See also</span></span>



[<span data-ttu-id="86657-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="86657-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="86657-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="86657-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="86657-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="86657-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="86657-137">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="86657-137">MAPI Structures</span></span>](mapi-structures.md)

