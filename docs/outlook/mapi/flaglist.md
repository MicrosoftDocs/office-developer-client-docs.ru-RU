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
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336941"
---
# <a name="flaglist"></a><span data-ttu-id="c982d-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="c982d-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="c982d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c982d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c982d-105">Содержит список флагов, используемых для указания состояния записей адресов в процессе разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="c982d-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c982d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c982d-106">Header file:</span></span>  <br/> |<span data-ttu-id="c982d-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c982d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="c982d-108">Members</span><span class="sxs-lookup"><span data-stu-id="c982d-108">Members</span></span>

 <span data-ttu-id="c982d-109">**Кфлагс**</span><span class="sxs-lookup"><span data-stu-id="c982d-109">**cFlags**</span></span>
  
> <span data-ttu-id="c982d-110">Количество флагов, определенных MAPI, в списке.</span><span class="sxs-lookup"><span data-stu-id="c982d-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="c982d-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c982d-111">**ulFlags**</span></span>
  
> <span data-ttu-id="c982d-112">Массив флагов, который предоставляет состояние операции разрешения имен для получателя.</span><span class="sxs-lookup"><span data-stu-id="c982d-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="c982d-113">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c982d-113">The following flags can be set:</span></span>
    
<span data-ttu-id="c982d-114">МАПИ_АМБИГУАУС</span><span class="sxs-lookup"><span data-stu-id="c982d-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="c982d-115">Получатель разрешен, но не является уникальным идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="c982d-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="c982d-116">Другие контейнеры адресных книг не должны пытаться разрешить этого получателя.</span><span class="sxs-lookup"><span data-stu-id="c982d-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="c982d-117">МАПИ_РЕСОЛВЕД</span><span class="sxs-lookup"><span data-stu-id="c982d-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="c982d-118">Получатель был сопоставлен с уникальным идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="c982d-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="c982d-119">Другие контейнеры адресных книг не должны пытаться разрешить этого получателя.</span><span class="sxs-lookup"><span data-stu-id="c982d-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="c982d-120">МАПИ_УНРЕСОЛВЕД</span><span class="sxs-lookup"><span data-stu-id="c982d-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="c982d-121">Запись не была устранена.</span><span class="sxs-lookup"><span data-stu-id="c982d-121">The entry has not been resolved.</span></span> <span data-ttu-id="c982d-122">Другие контейнеры адресных книг должны попытаться разрешить этого получателя.</span><span class="sxs-lookup"><span data-stu-id="c982d-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c982d-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c982d-123">Remarks</span></span>

<span data-ttu-id="c982d-124">Структура **флаглист** используется в качестве параметра для [Иабконтаинер:: ResolveNames](iabcontainer-resolvenames.md).</span><span class="sxs-lookup"><span data-stu-id="c982d-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="c982d-125">Каждый из разрешенных получателей включается в структуру [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="c982d-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="c982d-126">Так как контейнер адресной книги пытается разрешить каждого получателя, он устанавливает соответствующий флаг в соответствующей записи структуры **флаглист** .</span><span class="sxs-lookup"><span data-stu-id="c982d-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="c982d-127">Все записи в структуре **флаглист** находятся в том же порядке, что и записи в структуре **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="c982d-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="c982d-128">Это позволяет легко сопоставить параметр флага с получателем.</span><span class="sxs-lookup"><span data-stu-id="c982d-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c982d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c982d-129">See also</span></span>



[<span data-ttu-id="c982d-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="c982d-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="c982d-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="c982d-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="c982d-132">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="c982d-132">MAPI Structures</span></span>](mapi-structures.md)

