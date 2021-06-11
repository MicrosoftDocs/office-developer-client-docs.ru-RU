---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436113"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="d3912-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="d3912-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="d3912-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3912-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3912-105">Отделяет идентификатор сложной записи объекта, обычно сообщения в хранилище сообщений, в идентификатор входа этого объекта в магазине и идентификатор входа в хранилище.</span><span class="sxs-lookup"><span data-stu-id="d3912-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d3912-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d3912-106">Header file:</span></span>  <br/> |<span data-ttu-id="d3912-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d3912-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d3912-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d3912-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d3912-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d3912-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d3912-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d3912-110">Called by:</span></span>  <br/> |<span data-ttu-id="d3912-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="d3912-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="d3912-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d3912-112">Parameters</span></span>

 <span data-ttu-id="d3912-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="d3912-113">_psession_</span></span>
  
> <span data-ttu-id="d3912-114">[in] Указатель на сеанс, который используется клиентом приложения.</span><span class="sxs-lookup"><span data-stu-id="d3912-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="d3912-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="d3912-115">_cbEID_</span></span>
  
> <span data-ttu-id="d3912-116">[in] Размер в bytes идентификатора сложной записи, который необходимо разделить.</span><span class="sxs-lookup"><span data-stu-id="d3912-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="d3912-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="d3912-117">_pEID_</span></span>
  
> <span data-ttu-id="d3912-118">[in] Указатель на идентификатор сложной записи, который необходимо разделить.</span><span class="sxs-lookup"><span data-stu-id="d3912-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="d3912-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="d3912-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="d3912-120">[вышел] Указатель на возвращенный размер, в bytes, идентификатор входа в хранилище сообщений, который содержит объект.</span><span class="sxs-lookup"><span data-stu-id="d3912-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="d3912-121">Если параметр  _pEID_ указывает на идентификатор некомпонентной записи, то параметр  _pcbStoreEID_ указывает на значение нуля.</span><span class="sxs-lookup"><span data-stu-id="d3912-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="d3912-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="d3912-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="d3912-123">[вышел] Указатель на указатель на возвращенный идентификатор входа в хранилище сообщений, содержащий объект.</span><span class="sxs-lookup"><span data-stu-id="d3912-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="d3912-124">Если параметр _pEID_ указывает на идентификатор некомпонентной записи, NULL возвращается в _параметре ppStoreEID._</span><span class="sxs-lookup"><span data-stu-id="d3912-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="d3912-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="d3912-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="d3912-126">[вышел] Указатель на возвращенный размер в bytes идентификатора входа объекта.</span><span class="sxs-lookup"><span data-stu-id="d3912-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="d3912-127">Если параметр _pEID_ указывает на идентификатор некомпонентной записи, то параметр _pcbMsgEID_ равен значению _параметра cbEID._</span><span class="sxs-lookup"><span data-stu-id="d3912-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="d3912-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="d3912-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="d3912-129">[вышел] Указатель на указатель на возвращенный идентификатор входа объекта.</span><span class="sxs-lookup"><span data-stu-id="d3912-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="d3912-130">Если параметр  _pEID_ указывает на идентификатор некомпонентной записи,  _ppMsgEID_ указывает на указатель на копию идентификатора некомпонентной записи.</span><span class="sxs-lookup"><span data-stu-id="d3912-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d3912-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3912-131">Return value</span></span>

<span data-ttu-id="d3912-132">Нет.</span><span class="sxs-lookup"><span data-stu-id="d3912-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d3912-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3912-133">Remarks</span></span>

<span data-ttu-id="d3912-134">Если идентификатор, указанный параметром  _pEID,_ является составным, он делится на идентификатор входа объекта в хранилище сообщений и идентификатор входа магазина.</span><span class="sxs-lookup"><span data-stu-id="d3912-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="d3912-135">Строки идентификатора некомпонентной записи просто копируется.</span><span class="sxs-lookup"><span data-stu-id="d3912-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="d3912-136">Идентификатор соединения, который необходимо разделить, обычно создается функцией [HrComposeEID.](hrcomposeeid.md)</span><span class="sxs-lookup"><span data-stu-id="d3912-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d3912-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d3912-137">Notes to callers</span></span>

<span data-ttu-id="d3912-138">Память, которая содержит параметр  _pEID,_ будет выпущена после успешного завершения этой функции.</span><span class="sxs-lookup"><span data-stu-id="d3912-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="d3912-139">Реализация вызовов отвечает за то, чтобы освободить память для параметров вывода.</span><span class="sxs-lookup"><span data-stu-id="d3912-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

