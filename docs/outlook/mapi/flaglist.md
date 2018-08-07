---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2cf5ff69e8453b2da26fd5044823ddf4f99a9f45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808451"
---
# <a name="flaglist"></a><span data-ttu-id="f7587-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="f7587-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="f7587-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7587-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7587-105">Содержит список флагов, используемых для указания состояния записей адресов во время процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="f7587-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7587-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f7587-106">Header file:</span></span>  <br/> |<span data-ttu-id="f7587-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7587-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="f7587-108">Members</span><span class="sxs-lookup"><span data-stu-id="f7587-108">Members</span></span>

 <span data-ttu-id="f7587-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="f7587-109">**cFlags**</span></span>
  
> <span data-ttu-id="f7587-110">Число определенных MAPI флажки в списке.</span><span class="sxs-lookup"><span data-stu-id="f7587-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="f7587-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f7587-111">**ulFlags**</span></span>
  
> <span data-ttu-id="f7587-112">Массив флаги, который предоставляет сведения о состоянии операцию разрешения имени для получателя.</span><span class="sxs-lookup"><span data-stu-id="f7587-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="f7587-113">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="f7587-113">The following flags can be set:</span></span>
    
<span data-ttu-id="f7587-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="f7587-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="f7587-115">Получатель была устранена, но не уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="f7587-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="f7587-116">Другие контейнеры адресной книги не рекомендуется для устранения этой получателя.</span><span class="sxs-lookup"><span data-stu-id="f7587-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="f7587-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="f7587-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="f7587-118">Получатель была устранена в уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="f7587-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="f7587-119">Другие контейнеры адресной книги не рекомендуется для устранения этой получателя.</span><span class="sxs-lookup"><span data-stu-id="f7587-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="f7587-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="f7587-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="f7587-121">Операция не была устранена.</span><span class="sxs-lookup"><span data-stu-id="f7587-121">The entry has not been resolved.</span></span> <span data-ttu-id="f7587-122">Другие контейнеры адресной книги должны пытаться разрешить этому получателю.</span><span class="sxs-lookup"><span data-stu-id="f7587-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7587-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="f7587-123">Remarks</span></span>

<span data-ttu-id="f7587-124">Структура **FLAGLIST** используется в качестве параметра [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span><span class="sxs-lookup"><span data-stu-id="f7587-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="f7587-125">Каждого из получателей будет включен в структуру [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="f7587-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="f7587-126">Как контейнер адресной книги предпринимается попытка разрешить каждого получателя, соответствующей записи в структуре **FLAGLIST** устанавливает соответствующий флаг.</span><span class="sxs-lookup"><span data-stu-id="f7587-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="f7587-127">Все записи в структуре **FLAGLIST** , в том же порядке, как записи в структуре **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="f7587-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="f7587-128">Это позволяет легко связать параметр флага с получателем.</span><span class="sxs-lookup"><span data-stu-id="f7587-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7587-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f7587-129">See also</span></span>



[<span data-ttu-id="f7587-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="f7587-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="f7587-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="f7587-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="f7587-132">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f7587-132">MAPI Structures</span></span>](mapi-structures.md)

