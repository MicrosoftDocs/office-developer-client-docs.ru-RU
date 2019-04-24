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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347812"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="654c7-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="654c7-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="654c7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="654c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="654c7-105">Повторно создает идентификатор записи из кодировки ASCII.</span><span class="sxs-lookup"><span data-stu-id="654c7-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="654c7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="654c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="654c7-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="654c7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="654c7-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="654c7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="654c7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="654c7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="654c7-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="654c7-110">Called by:</span></span>  <br/> |<span data-ttu-id="654c7-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="654c7-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="654c7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="654c7-112">Parameters</span></span>

 <span data-ttu-id="654c7-113">_СЗ_</span><span class="sxs-lookup"><span data-stu-id="654c7-113">_sz_</span></span>
  
> <span data-ttu-id="654c7-114">возврата Указатель на строку ASCII, из которой создается идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="654c7-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="654c7-115">_ПКБ_</span><span class="sxs-lookup"><span data-stu-id="654c7-115">_pcb_</span></span>
  
> <span data-ttu-id="654c7-116">вышли Указатель на размер (в байтах) идентификатора записи, на который указывает параметр _ппентри_ .</span><span class="sxs-lookup"><span data-stu-id="654c7-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="654c7-117">_ппентри_</span><span class="sxs-lookup"><span data-stu-id="654c7-117">_ppentry_</span></span>
  
> <span data-ttu-id="654c7-118">вышли Указатель на указатель на возвращенную структуру [EntryID](entryid.md) , содержащую новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="654c7-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="654c7-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="654c7-119">Return value</span></span>

<span data-ttu-id="654c7-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="654c7-120">S_OK</span></span>
  
> <span data-ttu-id="654c7-121">Отдых успешно создан.</span><span class="sxs-lookup"><span data-stu-id="654c7-121">The recreation was successful.</span></span>
    
<span data-ttu-id="654c7-122">МАПИ_Е_ИНВАЛИД_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="654c7-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="654c7-123">Недопустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="654c7-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="654c7-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="654c7-124">Remarks</span></span>

<span data-ttu-id="654c7-125">Функции **хрентридфромсз** и [хрсзфроментрид](hrszfromentryid.md) обеспечивают преобразование между строковым и двоичным форматами идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="654c7-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="654c7-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="654c7-126">Notes to callers</span></span>

<span data-ttu-id="654c7-127">Функция **хрентридфромсз** выделяет память для строки ASCII с помощью функции [мапиаллокатебуффер](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="654c7-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

