---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 335fac38ff3f084195a000ad32a27adcb85c1cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564817"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="9770e-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="9770e-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="9770e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9770e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9770e-105">Создает идентификатор составные запись для объекта, обычно сообщения в банке сообщений.</span><span class="sxs-lookup"><span data-stu-id="9770e-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9770e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9770e-106">Header file:</span></span>  <br/> |<span data-ttu-id="9770e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9770e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9770e-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="9770e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9770e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9770e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9770e-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="9770e-110">Called by:</span></span>  <br/> |<span data-ttu-id="9770e-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="9770e-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a><span data-ttu-id="9770e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9770e-112">Parameters</span></span>

 <span data-ttu-id="9770e-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="9770e-113">_psession_</span></span>
  
> <span data-ttu-id="9770e-114">[in] Указатель на сеанс используется клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="9770e-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="9770e-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="9770e-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="9770e-116">[in] Размер, в байтах, ключ записи хранилища сообщений, удерживая сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="9770e-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="9770e-117">Если нулевой передается в параметре _cbStoreRecordKey_ , параметр _ppEID_ указывает на копию идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="9770e-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="9770e-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="9770e-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="9770e-119">[in] Указатель на ключ записи хранилища сообщений, который содержит сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="9770e-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="9770e-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="9770e-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="9770e-121">[in] Размер, в байтах, идентификатор записи сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="9770e-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="9770e-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="9770e-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="9770e-123">[in] Указатель на запись идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="9770e-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="9770e-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="9770e-124">_pcbEID_</span></span>
  
> <span data-ttu-id="9770e-125">[out] Указатель на размер, в байтах, возвращенный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="9770e-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="9770e-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="9770e-126">_ppEID_</span></span>
  
> <span data-ttu-id="9770e-127">[out] Указатель на указатель на идентификатор, возвращенного элемента.</span><span class="sxs-lookup"><span data-stu-id="9770e-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="9770e-128">Если значение параметра _cbStoreRecordKey_ больше нуля, параметр _ppEID_ указывает указатель на идентификатор составные записи, которая создается.</span><span class="sxs-lookup"><span data-stu-id="9770e-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="9770e-129">Если _cbStoreRecordKey_ равно нулю, _ppEID_ указывает указатель на копию идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="9770e-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9770e-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9770e-130">Return value</span></span>

<span data-ttu-id="9770e-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="9770e-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9770e-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="9770e-132">Remarks</span></span>

<span data-ttu-id="9770e-133">Если сообщение или другой объект, для которого создается идентификатор составные записи находится в хранилище сообщений, идентификатор создается идентификатор объекта записи и хранения записи ключа.</span><span class="sxs-lookup"><span data-stu-id="9770e-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="9770e-134">Если объект не в хранилище, то есть, если количество байтов для ключа записи хранилища, переданные в _cbStoreRecordKey_ равно нулю, идентификатор объекта записи просто скопирован.</span><span class="sxs-lookup"><span data-stu-id="9770e-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="9770e-135">Функция **HrComposeEID** позволяет приложениям для работы с объектами в нескольких хранилищ посредством использования идентификаторы составные записей.</span><span class="sxs-lookup"><span data-stu-id="9770e-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="9770e-136">Приложение может вызвать функцию [HrDecomposeEID](hrdecomposeeid.md) для разделения идентификатор составные записи в его исходное деловых партнеров.</span><span class="sxs-lookup"><span data-stu-id="9770e-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9770e-137">См. также</span><span class="sxs-lookup"><span data-stu-id="9770e-137">See also</span></span>



[<span data-ttu-id="9770e-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="9770e-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="9770e-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="9770e-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

