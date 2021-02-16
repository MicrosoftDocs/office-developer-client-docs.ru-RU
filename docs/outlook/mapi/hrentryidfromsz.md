---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437730"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="e7385-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="e7385-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="e7385-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7385-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7385-105">Повторное повторное определение идентификатора записи из его кодировки ASCII.</span><span class="sxs-lookup"><span data-stu-id="e7385-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7385-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e7385-106">Header file:</span></span>  <br/> |<span data-ttu-id="e7385-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e7385-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e7385-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e7385-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7385-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e7385-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e7385-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e7385-110">Called by:</span></span>  <br/> |<span data-ttu-id="e7385-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="e7385-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="e7385-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7385-112">Parameters</span></span>

 <span data-ttu-id="e7385-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="e7385-113">_sz_</span></span>
  
> <span data-ttu-id="e7385-114">[in] Указатель на строку ASCII, из которой создается идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="e7385-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="e7385-115">_pcb_</span><span class="sxs-lookup"><span data-stu-id="e7385-115">_pcb_</span></span>
  
> <span data-ttu-id="e7385-116">[out] Указатель на размер идентификатора записи,на который указывает параметр ppentry (в _bytes)._</span><span class="sxs-lookup"><span data-stu-id="e7385-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="e7385-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="e7385-117">_ppentry_</span></span>
  
> <span data-ttu-id="e7385-118">[out] Указатель на указатель на возвращенную структуру [ENTRYID,](entryid.md) которая содержит новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="e7385-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e7385-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7385-119">Return value</span></span>

<span data-ttu-id="e7385-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7385-120">S_OK</span></span>
  
> <span data-ttu-id="e7385-121">Воссоздание было успешным.</span><span class="sxs-lookup"><span data-stu-id="e7385-121">The recreation was successful.</span></span>
    
<span data-ttu-id="e7385-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e7385-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="e7385-123">Недопустимый ИД записи.</span><span class="sxs-lookup"><span data-stu-id="e7385-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7385-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="e7385-124">Remarks</span></span>

<span data-ttu-id="e7385-125">Функции **HrEntryIDFromSz** и [HrSzFromEntryID](hrszfromentryid.md) обеспечивают преобразование между строками и двоичными форматами идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="e7385-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e7385-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e7385-126">Notes to callers</span></span>

<span data-ttu-id="e7385-127">Функция **HrEntryIDFromSz** выделяет память для строки ASCII с помощью функции [MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="e7385-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

