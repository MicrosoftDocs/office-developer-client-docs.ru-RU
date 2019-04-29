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
# <a name="hrcomposeeid"></a><span data-ttu-id="e4beb-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="e4beb-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="e4beb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4beb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4beb-105">Создает составной идентификатор для объекта, обычно является сообщением в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="e4beb-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4beb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e4beb-106">Header file:</span></span>  <br/> |<span data-ttu-id="e4beb-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="e4beb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e4beb-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e4beb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e4beb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e4beb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e4beb-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e4beb-110">Called by:</span></span>  <br/> |<span data-ttu-id="e4beb-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="e4beb-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="e4beb-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4beb-112">Parameters</span></span>

 <span data-ttu-id="e4beb-113">_псессион_</span><span class="sxs-lookup"><span data-stu-id="e4beb-113">_psession_</span></span>
  
> <span data-ttu-id="e4beb-114">возврата Указатель на сеанс, используемый клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="e4beb-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="e4beb-115">_Кбсторерекордкэй_</span><span class="sxs-lookup"><span data-stu-id="e4beb-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="e4beb-116">возврата Размер (в байтах) ключа записи хранилища сообщений, содержащего сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="e4beb-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="e4beb-117">Если в параметре _кбсторерекордкэй_ передается нулевое значение, параметр _ппеид_ указывает на копию идентификатора записи объекта.</span><span class="sxs-lookup"><span data-stu-id="e4beb-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="e4beb-118">_Псторерекордкэй_</span><span class="sxs-lookup"><span data-stu-id="e4beb-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="e4beb-119">возврата Указатель на ключ записи хранилища сообщений, содержащего сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="e4beb-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="e4beb-120">_Кбмсжеид_</span><span class="sxs-lookup"><span data-stu-id="e4beb-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="e4beb-121">возврата Размер (в байтах) идентификатора записи сообщения или другого объекта.</span><span class="sxs-lookup"><span data-stu-id="e4beb-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="e4beb-122">_Пмсжеид_</span><span class="sxs-lookup"><span data-stu-id="e4beb-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="e4beb-123">возврата Указатель на идентификатор записи объекта.</span><span class="sxs-lookup"><span data-stu-id="e4beb-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="e4beb-124">_Пкбеид_</span><span class="sxs-lookup"><span data-stu-id="e4beb-124">_pcbEID_</span></span>
  
> <span data-ttu-id="e4beb-125">вышли Указатель на размер возвращенного идентификатора (в байтах).</span><span class="sxs-lookup"><span data-stu-id="e4beb-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="e4beb-126">_Ппеид_</span><span class="sxs-lookup"><span data-stu-id="e4beb-126">_ppEID_</span></span>
  
> <span data-ttu-id="e4beb-127">вышли Указатель на указатель на возвращенный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="e4beb-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="e4beb-128">Если значение параметра _кбсторерекордкэй_ больше нуля, параметр _ппеид_ указывает на указатель на созданный идентификатор составной записи.</span><span class="sxs-lookup"><span data-stu-id="e4beb-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="e4beb-129">Если _кбсторерекордкэй_ имеет значение 0, _ппеид_ указывает на указатель на копию идентификатора записи объекта.</span><span class="sxs-lookup"><span data-stu-id="e4beb-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e4beb-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4beb-130">Return value</span></span>

<span data-ttu-id="e4beb-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="e4beb-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e4beb-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="e4beb-132">Remarks</span></span>

<span data-ttu-id="e4beb-133">Если сообщение или другой объект, для которого создается создаваемый идентификатор составного элемента, находится в хранилище сообщений, идентификатор создается из идентификатора записи объекта и ключа записи в хранилище.</span><span class="sxs-lookup"><span data-stu-id="e4beb-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="e4beb-134">Если объект не находится в хранилище, то есть, если количество байт для ключа записи хранилища, переданное в _кбсторерекордкэй_ , равно нулю, то идентификатор записи объекта просто копируется.</span><span class="sxs-lookup"><span data-stu-id="e4beb-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="e4beb-135">Функция **хркомпосиид** позволяет приложениям работать с объектами в нескольких хранилищах с помощью составных идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="e4beb-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="e4beb-136">Приложение может вызвать функцию [хрдекомпосиид](hrdecomposeeid.md) , чтобы разделить идентификатор составной записи на исходные составляющие.</span><span class="sxs-lookup"><span data-stu-id="e4beb-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4beb-137">См. также</span><span class="sxs-lookup"><span data-stu-id="e4beb-137">See also</span></span>



[<span data-ttu-id="e4beb-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="e4beb-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="e4beb-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="e4beb-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

