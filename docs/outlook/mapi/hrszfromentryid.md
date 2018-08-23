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
ms.openlocfilehash: 366208b8288aeb61bf1bb78f2c9f10b400a3dc26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567596"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="dbbe0-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="dbbe0-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="dbbe0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbbe0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbbe0-105">Кодирует идентификатор запись в строку ASCII.</span><span class="sxs-lookup"><span data-stu-id="dbbe0-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbbe0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="dbbe0-106">Header file:</span></span>  <br/> |<span data-ttu-id="dbbe0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dbbe0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dbbe0-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="dbbe0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dbbe0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dbbe0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dbbe0-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="dbbe0-110">Called by:</span></span>  <br/> |<span data-ttu-id="dbbe0-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="dbbe0-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="dbbe0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbbe0-112">Parameters</span></span>

 <span data-ttu-id="dbbe0-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="dbbe0-113">_cb_</span></span>
  
> <span data-ttu-id="dbbe0-114">[in] Размер, в байтах, идентификатор записи, на который указывает параметр _pentry_ .</span><span class="sxs-lookup"><span data-stu-id="dbbe0-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="dbbe0-115">_pentry_</span><span class="sxs-lookup"><span data-stu-id="dbbe0-115">_pentry_</span></span>
  
> <span data-ttu-id="dbbe0-116">[in] Указатель на структуру [ENTRYID](entryid.md) , содержащее идентификатор записи для кодирования.</span><span class="sxs-lookup"><span data-stu-id="dbbe0-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="dbbe0-117">_psz_</span><span class="sxs-lookup"><span data-stu-id="dbbe0-117">_psz_</span></span>
  
> <span data-ttu-id="dbbe0-118">[out] Указатель на Возвращенная строка ASCII.</span><span class="sxs-lookup"><span data-stu-id="dbbe0-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dbbe0-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbbe0-119">Return value</span></span>

<span data-ttu-id="dbbe0-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="dbbe0-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dbbe0-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="dbbe0-121">Remarks</span></span>

<span data-ttu-id="dbbe0-122">Функции [HrEntryIDFromSz](hrentryidfromsz.md) и **HrSzFromEntryID** преобразование между строки и двоичного формата идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="dbbe0-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="dbbe0-123">С помощью интерфейса MAPI следует использовать структуры с двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="dbbe0-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dbbe0-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="dbbe0-124">Notes to callers</span></span>

<span data-ttu-id="dbbe0-125">Функция **HrSzFromEntryID** выделение памяти для строки ASCII, с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="dbbe0-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

