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
ms.openlocfilehash: f7a236c2a7e307d278cac5ef413cbd2f600bf09f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582100"
---
# <a name="flaglist"></a><span data-ttu-id="9404c-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="9404c-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="9404c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9404c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9404c-105">Содержит список флагов, используемых для указания состояния записей адресов во время процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="9404c-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9404c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9404c-106">Header file:</span></span>  <br/> |<span data-ttu-id="9404c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9404c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="9404c-108">Members</span><span class="sxs-lookup"><span data-stu-id="9404c-108">Members</span></span>

 <span data-ttu-id="9404c-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="9404c-109">**cFlags**</span></span>
  
> <span data-ttu-id="9404c-110">Число определенных MAPI флажки в списке.</span><span class="sxs-lookup"><span data-stu-id="9404c-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="9404c-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9404c-111">**ulFlags**</span></span>
  
> <span data-ttu-id="9404c-112">Массив флаги, который предоставляет сведения о состоянии операцию разрешения имени для получателя.</span><span class="sxs-lookup"><span data-stu-id="9404c-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="9404c-113">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="9404c-113">The following flags can be set:</span></span>
    
<span data-ttu-id="9404c-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="9404c-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="9404c-115">Получатель была устранена, но не уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="9404c-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="9404c-116">Другие контейнеры адресной книги не рекомендуется для устранения этой получателя.</span><span class="sxs-lookup"><span data-stu-id="9404c-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="9404c-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="9404c-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="9404c-118">Получатель была устранена в уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="9404c-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="9404c-119">Другие контейнеры адресной книги не рекомендуется для устранения этой получателя.</span><span class="sxs-lookup"><span data-stu-id="9404c-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="9404c-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="9404c-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="9404c-121">Операция не была устранена.</span><span class="sxs-lookup"><span data-stu-id="9404c-121">The entry has not been resolved.</span></span> <span data-ttu-id="9404c-122">Другие контейнеры адресной книги должны пытаться разрешить этому получателю.</span><span class="sxs-lookup"><span data-stu-id="9404c-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9404c-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="9404c-123">Remarks</span></span>

<span data-ttu-id="9404c-124">Структура **FLAGLIST** используется в качестве параметра [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span><span class="sxs-lookup"><span data-stu-id="9404c-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="9404c-125">Каждого из получателей будет включен в структуру [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="9404c-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="9404c-126">Как контейнер адресной книги предпринимается попытка разрешить каждого получателя, соответствующей записи в структуре **FLAGLIST** устанавливает соответствующий флаг.</span><span class="sxs-lookup"><span data-stu-id="9404c-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="9404c-127">Все записи в структуре **FLAGLIST** , в том же порядке, как записи в структуре **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="9404c-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="9404c-128">Это позволяет легко связать параметр флага с получателем.</span><span class="sxs-lookup"><span data-stu-id="9404c-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9404c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="9404c-129">See also</span></span>



[<span data-ttu-id="9404c-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="9404c-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="9404c-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="9404c-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="9404c-132">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="9404c-132">MAPI Structures</span></span>](mapi-structures.md)

