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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: a9aa6deeca930da82db61ba517796bfbc0676467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808654"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="fe387-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="fe387-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="fe387-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe387-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe387-105">Создает идентификатор составные запись для объекта, обычно сообщения в банке сообщений.</span><span class="sxs-lookup"><span data-stu-id="fe387-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe387-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="fe387-106">Header file:</span></span>  <br/> |<span data-ttu-id="fe387-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fe387-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fe387-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="fe387-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fe387-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fe387-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fe387-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="fe387-110">Called by:</span></span>  <br/> |<span data-ttu-id="fe387-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="fe387-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="fe387-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="fe387-112">Parameters</span></span>

 <span data-ttu-id="fe387-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="fe387-113">_psession_</span></span>
  
> <span data-ttu-id="fe387-114">[in] Указатель на сеанс используется клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="fe387-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="fe387-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="fe387-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="fe387-116">[in] Размер, в байтах, ключ записи хранилища сообщений, удерживая сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="fe387-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="fe387-117">Если нулевой передается в параметре _cbStoreRecordKey_ , параметр _ppEID_ указывает на копию идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="fe387-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="fe387-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="fe387-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="fe387-119">[in] Указатель на ключ записи хранилища сообщений, который содержит сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="fe387-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="fe387-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="fe387-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="fe387-121">[in] Размер, в байтах, идентификатор записи сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="fe387-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="fe387-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="fe387-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="fe387-123">[in] Указатель на запись идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="fe387-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="fe387-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="fe387-124">_pcbEID_</span></span>
  
> <span data-ttu-id="fe387-125">[out] Указатель на размер, в байтах, возвращенный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="fe387-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="fe387-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="fe387-126">_ppEID_</span></span>
  
> <span data-ttu-id="fe387-127">[out] Указатель на указатель на идентификатор, возвращенного элемента.</span><span class="sxs-lookup"><span data-stu-id="fe387-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="fe387-128">Если значение параметра _cbStoreRecordKey_ больше нуля, параметр _ppEID_ указывает указатель на идентификатор составные записи, которая создается.</span><span class="sxs-lookup"><span data-stu-id="fe387-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="fe387-129">Если _cbStoreRecordKey_ равно нулю, _ppEID_ указывает указатель на копию идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="fe387-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fe387-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe387-130">Return value</span></span>

<span data-ttu-id="fe387-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="fe387-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe387-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe387-132">Remarks</span></span>

<span data-ttu-id="fe387-133">Если сообщение или другой объект, для которого создается идентификатор составные записи находится в хранилище сообщений, идентификатор создается идентификатор объекта записи и хранения записи ключа.</span><span class="sxs-lookup"><span data-stu-id="fe387-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="fe387-134">Если объект не в хранилище, то есть, если количество байтов для ключа записи хранилища, переданные в _cbStoreRecordKey_ равно нулю, идентификатор объекта записи просто скопирован.</span><span class="sxs-lookup"><span data-stu-id="fe387-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="fe387-135">Функция **HrComposeEID** позволяет приложениям для работы с объектами в нескольких хранилищ посредством использования идентификаторы составные записей.</span><span class="sxs-lookup"><span data-stu-id="fe387-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="fe387-136">Приложение может вызвать функцию [HrDecomposeEID](hrdecomposeeid.md) для разделения идентификатор составные записи в его исходное деловых партнеров.</span><span class="sxs-lookup"><span data-stu-id="fe387-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe387-137">См. также</span><span class="sxs-lookup"><span data-stu-id="fe387-137">See also</span></span>



[<span data-ttu-id="fe387-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="fe387-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="fe387-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="fe387-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

