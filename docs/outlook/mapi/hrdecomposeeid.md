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
# <a name="hrdecomposeeid"></a><span data-ttu-id="8ab47-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="8ab47-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="8ab47-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ab47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ab47-105">Отделяет составной идентификатор записи объекта, обычно это сообщение в хранилище сообщений, в идентификатор записи этого объекта в хранилище и идентификатор записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="8ab47-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ab47-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8ab47-106">Header file:</span></span>  <br/> |<span data-ttu-id="8ab47-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="8ab47-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8ab47-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8ab47-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8ab47-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8ab47-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8ab47-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8ab47-110">Called by:</span></span>  <br/> |<span data-ttu-id="8ab47-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="8ab47-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="8ab47-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ab47-112">Parameters</span></span>

 <span data-ttu-id="8ab47-113">_псессион_</span><span class="sxs-lookup"><span data-stu-id="8ab47-113">_psession_</span></span>
  
> <span data-ttu-id="8ab47-114">возврата Указатель на сеанс, используемый клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="8ab47-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="8ab47-115">_кбеид_</span><span class="sxs-lookup"><span data-stu-id="8ab47-115">_cbEID_</span></span>
  
> <span data-ttu-id="8ab47-116">возврата Размер (в байтах) составного идентификатора операции, который должен быть отделен.</span><span class="sxs-lookup"><span data-stu-id="8ab47-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="8ab47-117">_пеид_</span><span class="sxs-lookup"><span data-stu-id="8ab47-117">_pEID_</span></span>
  
> <span data-ttu-id="8ab47-118">возврата Указатель на идентификатор составной записи, который необходимо отделить.</span><span class="sxs-lookup"><span data-stu-id="8ab47-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="8ab47-119">_пкбсториид_</span><span class="sxs-lookup"><span data-stu-id="8ab47-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="8ab47-120">вышли Указатель на возвращенный размер (в байтах) идентификатора записи для хранилища сообщений, содержащего объект.</span><span class="sxs-lookup"><span data-stu-id="8ab47-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="8ab47-121">Если параметр _пеид_ указывает на несоставный идентификатор записи, параметр _пкбсториид_ указывает на нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8ab47-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="8ab47-122">_ппсториид_</span><span class="sxs-lookup"><span data-stu-id="8ab47-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="8ab47-123">вышли Указатель на указатель возвращаемого идентификатора записи хранилища сообщений, содержащего объект.</span><span class="sxs-lookup"><span data-stu-id="8ab47-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="8ab47-124">Если параметр _пеид_ указывает на несоставный идентификатор записи, в параметре _ппсториид_ возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="8ab47-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="8ab47-125">_пкбмсжеид_</span><span class="sxs-lookup"><span data-stu-id="8ab47-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="8ab47-126">вышли Указатель на возвращенный размер (в байтах) идентификатора записи объекта.</span><span class="sxs-lookup"><span data-stu-id="8ab47-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="8ab47-127">Если параметр _пеид_ указывает на несоставный идентификатор записи, параметр _пкбмсжеид_ равен значению параметра _кбеид_ .</span><span class="sxs-lookup"><span data-stu-id="8ab47-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="8ab47-128">_ппмсжеид_</span><span class="sxs-lookup"><span data-stu-id="8ab47-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="8ab47-129">вышли Указатель на указатель на возвращенный идентификатор записи объекта.</span><span class="sxs-lookup"><span data-stu-id="8ab47-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="8ab47-130">Если параметр _пеид_ указывает на несоставной идентификатор записи, _ппмсжеид_ указывает на указатель на копию несоставного идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="8ab47-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8ab47-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ab47-131">Return value</span></span>

<span data-ttu-id="8ab47-132">Нет.</span><span class="sxs-lookup"><span data-stu-id="8ab47-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ab47-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ab47-133">Remarks</span></span>

<span data-ttu-id="8ab47-134">Если идентификатор, указанный в параметре _пеид_ , является составным, он делится на идентификатор записи объекта в его банке сообщений и идентификатор записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="8ab47-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="8ab47-135">Строки несоставных идентификаторов записей просто копируются.</span><span class="sxs-lookup"><span data-stu-id="8ab47-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="8ab47-136">Составной идентификатор, который должен быть отделен, обычно создается функцией [хркомпосиид](hrcomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="8ab47-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8ab47-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8ab47-137">Notes to callers</span></span>

<span data-ttu-id="8ab47-138">При успешном завершении этой функции будет выпущена память, содержащая параметр _пеид_ .</span><span class="sxs-lookup"><span data-stu-id="8ab47-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="8ab47-139">Вызываемая реализация отвечает за освобождение памяти для выходных параметров.</span><span class="sxs-lookup"><span data-stu-id="8ab47-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

