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
# <a name="hrentryidfromsz"></a><span data-ttu-id="ebe15-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="ebe15-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="ebe15-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebe15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebe15-105">Воссоздает идентификатор записи из коди-кодии ASCII.</span><span class="sxs-lookup"><span data-stu-id="ebe15-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ebe15-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ebe15-106">Header file:</span></span>  <br/> |<span data-ttu-id="ebe15-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ebe15-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ebe15-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ebe15-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ebe15-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ebe15-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ebe15-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ebe15-110">Called by:</span></span>  <br/> |<span data-ttu-id="ebe15-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="ebe15-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="ebe15-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="ebe15-112">Parameters</span></span>

 <span data-ttu-id="ebe15-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="ebe15-113">_sz_</span></span>
  
> <span data-ttu-id="ebe15-114">[in] Указатель на строку ASCII, из которой создается идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="ebe15-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="ebe15-115">_pcb_</span><span class="sxs-lookup"><span data-stu-id="ebe15-115">_pcb_</span></span>
  
> <span data-ttu-id="ebe15-116">[вышел] Указатель на размер в bytes идентификатора записи, указываемого параметром _ppentry._</span><span class="sxs-lookup"><span data-stu-id="ebe15-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="ebe15-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="ebe15-117">_ppentry_</span></span>
  
> <span data-ttu-id="ebe15-118">[вышел] Указатель на указатель на возвращаемую [структуру ENTRYID,](entryid.md) содержаную новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="ebe15-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ebe15-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebe15-119">Return value</span></span>

<span data-ttu-id="ebe15-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebe15-120">S_OK</span></span>
  
> <span data-ttu-id="ebe15-121">Отдых был успешным.</span><span class="sxs-lookup"><span data-stu-id="ebe15-121">The recreation was successful.</span></span>
    
<span data-ttu-id="ebe15-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ebe15-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="ebe15-123">ID записи был недействительным.</span><span class="sxs-lookup"><span data-stu-id="ebe15-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ebe15-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="ebe15-124">Remarks</span></span>

<span data-ttu-id="ebe15-125">Функции **HrEntryIDFromSz** и [HrSzFromEntryID](hrszfromentryid.md) обеспечивают преобразование между строками и двоичными форматами идентификаторов записи.</span><span class="sxs-lookup"><span data-stu-id="ebe15-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ebe15-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ebe15-126">Notes to callers</span></span>

<span data-ttu-id="ebe15-127">Функция **HrEntryIDFromSz** выделяет память для строки ASCII с помощью [функции MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="ebe15-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

