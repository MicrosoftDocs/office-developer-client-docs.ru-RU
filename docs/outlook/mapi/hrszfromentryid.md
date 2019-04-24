---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346419"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="47ac7-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="47ac7-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="47ac7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47ac7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47ac7-105">Кодирует идентификатор записи в строку ASCII.</span><span class="sxs-lookup"><span data-stu-id="47ac7-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47ac7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="47ac7-106">Header file:</span></span>  <br/> |<span data-ttu-id="47ac7-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="47ac7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="47ac7-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="47ac7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="47ac7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="47ac7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="47ac7-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="47ac7-110">Called by:</span></span>  <br/> |<span data-ttu-id="47ac7-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="47ac7-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="47ac7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="47ac7-112">Parameters</span></span>

 <span data-ttu-id="47ac7-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="47ac7-113">_cb_</span></span>
  
> <span data-ttu-id="47ac7-114">возврата Размер (в байтах) идентификатора записи, на который указывает параметр _пентри_ .</span><span class="sxs-lookup"><span data-stu-id="47ac7-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="47ac7-115">_пентри_</span><span class="sxs-lookup"><span data-stu-id="47ac7-115">_pentry_</span></span>
  
> <span data-ttu-id="47ac7-116">возврата Указатель на структуру [EntryID](entryid.md) , содержащую идентификатор записи, который необходимо закодировать.</span><span class="sxs-lookup"><span data-stu-id="47ac7-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="47ac7-117">_ПСЗ_</span><span class="sxs-lookup"><span data-stu-id="47ac7-117">_psz_</span></span>
  
> <span data-ttu-id="47ac7-118">вышли Указатель на возвращаемую строку ASCII.</span><span class="sxs-lookup"><span data-stu-id="47ac7-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47ac7-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47ac7-119">Return value</span></span>

<span data-ttu-id="47ac7-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="47ac7-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47ac7-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="47ac7-121">Remarks</span></span>

<span data-ttu-id="47ac7-122">Функции [хрентридфромсз](hrentryidfromsz.md) и **хрсзфроментрид** обеспечивают преобразование между строковым и двоичным форматами идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="47ac7-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="47ac7-123">С помощью MAPI следует использовать структуры с двоичными данными.</span><span class="sxs-lookup"><span data-stu-id="47ac7-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="47ac7-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="47ac7-124">Notes to callers</span></span>

<span data-ttu-id="47ac7-125">Функция **хрсзфроментрид** выделяет память для строки ASCII с помощью функции [мапиаллокатебуффер](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="47ac7-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

