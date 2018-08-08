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
ms.openlocfilehash: 2b7ef789c80f85f3539ec3bbd0caf4a8adc50f3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808674"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="7deb0-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="7deb0-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="7deb0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7deb0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7deb0-105">Повторно создает запись идентификатора из кодировки ASCII.</span><span class="sxs-lookup"><span data-stu-id="7deb0-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7deb0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7deb0-106">Header file:</span></span>  <br/> |<span data-ttu-id="7deb0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7deb0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7deb0-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="7deb0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7deb0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7deb0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7deb0-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="7deb0-110">Called by:</span></span>  <br/> |<span data-ttu-id="7deb0-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="7deb0-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="7deb0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7deb0-112">Parameters</span></span>

 <span data-ttu-id="7deb0-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="7deb0-113">_sz_</span></span>
  
> <span data-ttu-id="7deb0-114">[in] Указатель на строку ASCII из которого требуется создать запись идентификатора.</span><span class="sxs-lookup"><span data-stu-id="7deb0-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="7deb0-115">_печатной_</span><span class="sxs-lookup"><span data-stu-id="7deb0-115">_pcb_</span></span>
  
> <span data-ttu-id="7deb0-116">[out] Указатель на размер, в байтах, идентификатор записи, на который указывает параметр _ppentry_ .</span><span class="sxs-lookup"><span data-stu-id="7deb0-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="7deb0-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="7deb0-117">_ppentry_</span></span>
  
> <span data-ttu-id="7deb0-118">[out] Указатель на указатель на структуру возвращенные [ENTRYID](entryid.md) , который содержит новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="7deb0-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7deb0-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7deb0-119">Return value</span></span>

<span data-ttu-id="7deb0-120">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7deb0-120">S_OK</span></span>
  
> <span data-ttu-id="7deb0-121">Повторное создание прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="7deb0-121">The recreation was successful.</span></span>
    
<span data-ttu-id="7deb0-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7deb0-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="7deb0-123">Недопустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="7deb0-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7deb0-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="7deb0-124">Remarks</span></span>

<span data-ttu-id="7deb0-125">Функции **HrEntryIDFromSz** и [HrSzFromEntryID](hrszfromentryid.md) преобразование между строки и двоичного формата идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="7deb0-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7deb0-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7deb0-126">Notes to callers</span></span>

<span data-ttu-id="7deb0-127">Функция **HrEntryIDFromSz** выделение памяти для строки ASCII, с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7deb0-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

