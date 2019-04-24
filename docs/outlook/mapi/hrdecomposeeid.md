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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348071"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="6198f-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="6198f-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="6198f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6198f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6198f-105">Отделяет составной идентификатор записи объекта, обычно это сообщение в хранилище сообщений, в идентификатор записи этого объекта в хранилище и идентификатор записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="6198f-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6198f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6198f-106">Header file:</span></span>  <br/> |<span data-ttu-id="6198f-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="6198f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6198f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="6198f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6198f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6198f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6198f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="6198f-110">Called by:</span></span>  <br/> |<span data-ttu-id="6198f-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="6198f-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="6198f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6198f-112">Parameters</span></span>

 <span data-ttu-id="6198f-113">_псессион_</span><span class="sxs-lookup"><span data-stu-id="6198f-113">_psession_</span></span>
  
> <span data-ttu-id="6198f-114">возврата Указатель на сеанс, используемый клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="6198f-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="6198f-115">_Кбеид_</span><span class="sxs-lookup"><span data-stu-id="6198f-115">_cbEID_</span></span>
  
> <span data-ttu-id="6198f-116">возврата Размер (в байтах) составного идентификатора операции, который должен быть отделен.</span><span class="sxs-lookup"><span data-stu-id="6198f-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="6198f-117">_Пеид_</span><span class="sxs-lookup"><span data-stu-id="6198f-117">_pEID_</span></span>
  
> <span data-ttu-id="6198f-118">возврата Указатель на идентификатор составной записи, который необходимо отделить.</span><span class="sxs-lookup"><span data-stu-id="6198f-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="6198f-119">_Пкбсториид_</span><span class="sxs-lookup"><span data-stu-id="6198f-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="6198f-120">вышли Указатель на возвращенный размер (в байтах) идентификатора записи для хранилища сообщений, содержащего объект.</span><span class="sxs-lookup"><span data-stu-id="6198f-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="6198f-121">Если параметр _пеид_ указывает на несоставный идентификатор записи, параметр _пкбсториид_ указывает на нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6198f-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="6198f-122">_Ппсториид_</span><span class="sxs-lookup"><span data-stu-id="6198f-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="6198f-123">вышли Указатель на указатель возвращаемого идентификатора записи хранилища сообщений, содержащего объект.</span><span class="sxs-lookup"><span data-stu-id="6198f-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="6198f-124">Если параметр _пеид_ указывает на несоставный идентификатор записи, в параметре _ППСТОРИИД_ возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="6198f-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="6198f-125">_Пкбмсжеид_</span><span class="sxs-lookup"><span data-stu-id="6198f-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="6198f-126">вышли Указатель на возвращенный размер (в байтах) идентификатора записи объекта.</span><span class="sxs-lookup"><span data-stu-id="6198f-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="6198f-127">Если параметр _пеид_ указывает на несоставный идентификатор записи, параметр _пкбмсжеид_ равен значению параметра _кбеид_ .</span><span class="sxs-lookup"><span data-stu-id="6198f-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="6198f-128">_Ппмсжеид_</span><span class="sxs-lookup"><span data-stu-id="6198f-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="6198f-129">вышли Указатель на указатель на возвращенный идентификатор записи объекта.</span><span class="sxs-lookup"><span data-stu-id="6198f-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="6198f-130">Если параметр _пеид_ указывает на несоставной идентификатор записи, _ппмсжеид_ указывает на указатель на копию несоставного идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="6198f-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6198f-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6198f-131">Return value</span></span>

<span data-ttu-id="6198f-132">Нет.</span><span class="sxs-lookup"><span data-stu-id="6198f-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6198f-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="6198f-133">Remarks</span></span>

<span data-ttu-id="6198f-134">Если идентификатор, указанный в параметре _пеид_ , является составным, он делится на идентификатор записи объекта в его банке сообщений и идентификатор записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="6198f-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="6198f-135">Строки несоставных идентификаторов записей просто копируются.</span><span class="sxs-lookup"><span data-stu-id="6198f-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="6198f-136">Составной идентификатор, который должен быть отделен, обычно создается функцией [хркомпосиид](hrcomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="6198f-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6198f-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6198f-137">Notes to callers</span></span>

<span data-ttu-id="6198f-138">При успешном завершении этой функции будет выпущена память, содержащая параметр _пеид_ .</span><span class="sxs-lookup"><span data-stu-id="6198f-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="6198f-139">Вызываемая реализация отвечает за освобождение памяти для выходных параметров.</span><span class="sxs-lookup"><span data-stu-id="6198f-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

