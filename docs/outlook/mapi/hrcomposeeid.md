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
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429049"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="60dd2-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="60dd2-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="60dd2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60dd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60dd2-105">Создает идентификатор сложной записи для объекта, как правило, сообщения в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="60dd2-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60dd2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="60dd2-106">Header file:</span></span>  <br/> |<span data-ttu-id="60dd2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="60dd2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="60dd2-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="60dd2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="60dd2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="60dd2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="60dd2-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="60dd2-110">Called by:</span></span>  <br/> |<span data-ttu-id="60dd2-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="60dd2-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="60dd2-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="60dd2-112">Parameters</span></span>

 <span data-ttu-id="60dd2-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="60dd2-113">_psession_</span></span>
  
> <span data-ttu-id="60dd2-114">[in] Указатель на сеанс, который используется клиентом приложения.</span><span class="sxs-lookup"><span data-stu-id="60dd2-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="60dd2-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="60dd2-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="60dd2-116">[in] Размер в bytes ключа записи в хранилище сообщений с сообщением или другим объектом.</span><span class="sxs-lookup"><span data-stu-id="60dd2-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="60dd2-117">Если в  _параметре cbStoreRecordKey_ передается ноль, параметр  _ppEID_ указывает на копию идентификатора входа объекта.</span><span class="sxs-lookup"><span data-stu-id="60dd2-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="60dd2-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="60dd2-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="60dd2-119">[in] Указатель на ключ записи в хранилище сообщений, содержащий сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="60dd2-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="60dd2-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="60dd2-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="60dd2-121">[in] Размер в bytes идентификатора входа сообщения или другого объекта.</span><span class="sxs-lookup"><span data-stu-id="60dd2-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="60dd2-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="60dd2-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="60dd2-123">[in] Указатель на идентификатор входа объекта.</span><span class="sxs-lookup"><span data-stu-id="60dd2-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="60dd2-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="60dd2-124">_pcbEID_</span></span>
  
> <span data-ttu-id="60dd2-125">[вышел] Указатель на размер в bytes возвращенного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="60dd2-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="60dd2-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="60dd2-126">_ppEID_</span></span>
  
> <span data-ttu-id="60dd2-127">[вышел] Указатель на указатель на возвращенный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="60dd2-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="60dd2-128">Если значение параметра  _cbStoreRecordKey_ больше нуля, параметр  _ppEID_ указывает на указатель на созданный идентификатор входной записи.</span><span class="sxs-lookup"><span data-stu-id="60dd2-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="60dd2-129">Если  _значение cbStoreRecordKey_ нулевое,  _ppEID_ указывает на указатель на копию идентификатора входа объекта.</span><span class="sxs-lookup"><span data-stu-id="60dd2-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="60dd2-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60dd2-130">Return value</span></span>

<span data-ttu-id="60dd2-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="60dd2-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60dd2-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="60dd2-132">Remarks</span></span>

<span data-ttu-id="60dd2-133">Если сообщение или другой объект, для которого создается идентификатор входного соединения, находится в хранилище сообщений, идентификатор создается из идентификатора входа объекта и ключа записи магазина.</span><span class="sxs-lookup"><span data-stu-id="60dd2-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="60dd2-134">Если объект не находится в магазине, то есть если количество byte для ключа записи магазина, переданного  _в cbStoreRecordKey,_ ноль, идентификатор входа объекта просто копируется.</span><span class="sxs-lookup"><span data-stu-id="60dd2-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="60dd2-135">Функция **HrComposeEID** позволяет приложениям работать с объектами в нескольких хранилищах с помощью идентификаторов сложных входов.</span><span class="sxs-lookup"><span data-stu-id="60dd2-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="60dd2-136">Приложение может вызвать функцию [HrDecomposeEID,](hrdecomposeeid.md) чтобы разделить идентификатор входного соединения на исходные составляющие.</span><span class="sxs-lookup"><span data-stu-id="60dd2-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60dd2-137">См. также</span><span class="sxs-lookup"><span data-stu-id="60dd2-137">See also</span></span>



[<span data-ttu-id="60dd2-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="60dd2-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="60dd2-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="60dd2-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

