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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412977"
---
# <a name="flaglist"></a><span data-ttu-id="5dc02-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="5dc02-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="5dc02-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dc02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dc02-105">Содержит список флагов, используемых для указать состояние записей адресов во время процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="5dc02-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5dc02-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5dc02-106">Header file:</span></span>  <br/> |<span data-ttu-id="5dc02-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5dc02-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="5dc02-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="5dc02-108">Members</span></span>

 <span data-ttu-id="5dc02-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="5dc02-109">**cFlags**</span></span>
  
> <span data-ttu-id="5dc02-110">Количество флагов, определенных MAPI, в списке.</span><span class="sxs-lookup"><span data-stu-id="5dc02-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="5dc02-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="5dc02-111">**ulFlags**</span></span>
  
> <span data-ttu-id="5dc02-112">Массив флагов, который предоставляет состояние операции разрешения имен для получателя.</span><span class="sxs-lookup"><span data-stu-id="5dc02-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="5dc02-113">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5dc02-113">The following flags can be set:</span></span>
    
<span data-ttu-id="5dc02-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="5dc02-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="5dc02-115">Получатель был разрешен, но не имеет уникального идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="5dc02-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="5dc02-116">Другие контейнеры адресной книги не должны пытаться разрешить этого получателя.</span><span class="sxs-lookup"><span data-stu-id="5dc02-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="5dc02-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="5dc02-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="5dc02-118">Получатель был разрешен в уникальный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="5dc02-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="5dc02-119">Другие контейнеры адресной книги не должны пытаться разрешить этого получателя.</span><span class="sxs-lookup"><span data-stu-id="5dc02-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="5dc02-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="5dc02-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="5dc02-121">Запись не была разрешена.</span><span class="sxs-lookup"><span data-stu-id="5dc02-121">The entry has not been resolved.</span></span> <span data-ttu-id="5dc02-122">Другие контейнеры адресной книги должны попытаться разрешить этого получателя.</span><span class="sxs-lookup"><span data-stu-id="5dc02-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5dc02-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="5dc02-123">Remarks</span></span>

<span data-ttu-id="5dc02-124">Структура **FLAGLIST** используется в качестве параметра [для IABContainer::ResolveNames.](iabcontainer-resolvenames.md)</span><span class="sxs-lookup"><span data-stu-id="5dc02-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="5dc02-125">Каждый из разрешенных получателей включается в структуру [ADRLIST.](adrlist.md)</span><span class="sxs-lookup"><span data-stu-id="5dc02-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="5dc02-126">Когда контейнер адресной книги пытается разрешить каждого получателя, он устанавливает соответствующий флаг в соответствующей записи в **структуре FLAGLIST.**</span><span class="sxs-lookup"><span data-stu-id="5dc02-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="5dc02-127">Все записи в структуре **FLAGLIST** находятся в том же порядке, что и записи в **структуре ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="5dc02-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="5dc02-128">Это упрощает связывать параметр флага с получателем.</span><span class="sxs-lookup"><span data-stu-id="5dc02-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5dc02-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5dc02-129">See also</span></span>



[<span data-ttu-id="5dc02-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="5dc02-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="5dc02-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="5dc02-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="5dc02-132">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5dc02-132">MAPI Structures</span></span>](mapi-structures.md)

