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
ms.openlocfilehash: e66d48b6caefe0fee67f41ea829db3201751cf27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808668"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="46132-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="46132-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="46132-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46132-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46132-105">Разделяет составные запись идентификатор объекта, обычно сообщения в банке сообщений в идентификатор записи этого объекта в хранилище и идентификатор записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="46132-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46132-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="46132-106">Header file:</span></span>  <br/> |<span data-ttu-id="46132-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="46132-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="46132-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="46132-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="46132-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="46132-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="46132-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="46132-110">Called by:</span></span>  <br/> |<span data-ttu-id="46132-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="46132-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="46132-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="46132-112">Parameters</span></span>

 <span data-ttu-id="46132-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="46132-113">_psession_</span></span>
  
> <span data-ttu-id="46132-114">[in] Указатель на сеанс используется клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="46132-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="46132-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="46132-115">_cbEID_</span></span>
  
> <span data-ttu-id="46132-116">[in] Размер, в байтах, составные запись идентификатора отделить.</span><span class="sxs-lookup"><span data-stu-id="46132-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="46132-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="46132-117">_pEID_</span></span>
  
> <span data-ttu-id="46132-118">[in] Указатель на идентификатор составные записи отделить.</span><span class="sxs-lookup"><span data-stu-id="46132-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="46132-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="46132-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="46132-120">[out] Указатель на возвращаемый размер, в байтах, идентификатор записи хранилища сообщение, содержащее объект.</span><span class="sxs-lookup"><span data-stu-id="46132-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="46132-121">Если параметр _pEID_ указывает идентификатор noncompound записи, параметр _pcbStoreEID_ указывает нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="46132-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="46132-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="46132-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="46132-123">[out] Указатель на указатель на идентификатор возвращенного элемента хранилища сообщение, содержащее объект.</span><span class="sxs-lookup"><span data-stu-id="46132-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="46132-124">Если параметр _pEID_ указывает идентификатор noncompound записи, с помощью параметра _ppStoreEID_ возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="46132-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="46132-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="46132-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="46132-126">[out] Указатель на возвращаемый размер, в байтах, запись идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="46132-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="46132-127">Если параметр _pEID_ указывает идентификатор noncompound записи, параметр _pcbMsgEID_ равно значению параметра _cbEID_ .</span><span class="sxs-lookup"><span data-stu-id="46132-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="46132-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="46132-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="46132-129">[out] Указатель на указатель возвращенного элемента идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="46132-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="46132-130">Если параметр _pEID_ указывает идентификатор noncompound записи, _ppMsgEID_ указывает указатель на копию идентификатор noncompound записи.</span><span class="sxs-lookup"><span data-stu-id="46132-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="46132-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46132-131">Return value</span></span>

<span data-ttu-id="46132-132">Нет.</span><span class="sxs-lookup"><span data-stu-id="46132-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46132-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="46132-133">Remarks</span></span>

<span data-ttu-id="46132-134">Если идентификатор, указанный в параметре _pEID_ составные, она разбивается на идентификатор записи объекта в его хранилища сообщений и идентификатор записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="46132-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="46132-135">Строки идентификатора noncompound записи, просто копируются.</span><span class="sxs-lookup"><span data-stu-id="46132-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="46132-136">Составные идентификатор отделить обычно является одним создан с помощью функции [HrComposeEID](hrcomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="46132-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="46132-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="46132-137">Notes to callers</span></span>

<span data-ttu-id="46132-138">Объем памяти, в котором размещается параметр _pEID_ высвобождается при успешном выполнении этой функции.</span><span class="sxs-lookup"><span data-stu-id="46132-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="46132-139">Вызывающий реализации несет ответственность за освобождение памяти для выходных параметров.</span><span class="sxs-lookup"><span data-stu-id="46132-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

