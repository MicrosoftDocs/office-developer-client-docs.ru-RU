---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3bcad4c236f71390f7a048eb66860720e9180e06
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582044"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="4fde2-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="4fde2-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="4fde2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fde2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fde2-105">Создает строку ASCII, представляющий идентификатор составные записи для объекта, обычно сообщения в банке сообщений.</span><span class="sxs-lookup"><span data-stu-id="4fde2-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fde2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4fde2-106">Header file:</span></span>  <br/> |<span data-ttu-id="4fde2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4fde2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4fde2-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="4fde2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4fde2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4fde2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4fde2-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="4fde2-110">Called by:</span></span>  <br/> |<span data-ttu-id="4fde2-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="4fde2-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a><span data-ttu-id="4fde2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fde2-112">Parameters</span></span>

 <span data-ttu-id="4fde2-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="4fde2-113">_psession_</span></span>
  
> <span data-ttu-id="4fde2-114">[in] Указатель на сеанс используется клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="4fde2-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="4fde2-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="4fde2-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="4fde2-116">[in] Размер, в байтах, ключ записи хранилища сообщений, который содержит сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="4fde2-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="4fde2-117">Если нулевой передается в параметре _cbStoreRecordKey_ , указывает параметр _pszMsgID_ на копию идентификатор записи преобразуется в текст.</span><span class="sxs-lookup"><span data-stu-id="4fde2-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="4fde2-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="4fde2-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="4fde2-119">[in] Указатель на ключ записи хранилища сообщений, который содержит сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="4fde2-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="4fde2-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="4fde2-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="4fde2-121">[in] Размер, в байтах, идентификатор записи сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="4fde2-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="4fde2-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="4fde2-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="4fde2-123">[in] Указатель на запись идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="4fde2-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="4fde2-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="4fde2-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="4fde2-125">[out] Указатель на Возвращенная строка ASCII.</span><span class="sxs-lookup"><span data-stu-id="4fde2-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="4fde2-126">Если параметр _cbStoreRecordKey_ больше нуля, указывает параметр _pszMsgID_ на идентификатор составные записи преобразуется в текст.</span><span class="sxs-lookup"><span data-stu-id="4fde2-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="4fde2-127">Если _cbStoreRecordKey_ равно нулю, _pszMsgID_ указывает идентификатор noncompound записи преобразуется в текст.</span><span class="sxs-lookup"><span data-stu-id="4fde2-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4fde2-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fde2-128">Return value</span></span>

<span data-ttu-id="4fde2-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="4fde2-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4fde2-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="4fde2-130">Remarks</span></span>

<span data-ttu-id="4fde2-131">Если сообщение или другой объект, для которого создается идентификатор составные записи находится в хранилище сообщений, строка идентификатора создается идентификатор объекта записи и хранения записи ключа.</span><span class="sxs-lookup"><span data-stu-id="4fde2-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="4fde2-132">Если объект не в хранилище, то есть, если количество байтов для ключа записи хранилища, переданной в параметре _cbStoreRecordKey_ равно нулю, идентификатор объекта записи просто копируется и преобразован в строку.</span><span class="sxs-lookup"><span data-stu-id="4fde2-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="4fde2-133">Вызов функции **HrComposeMsgID** эквивалентен вызову функции [HrComposeEID](hrcomposeeid.md) , а затем функцию [HrSzFromEntryID](hrszfromentryid.md) .</span><span class="sxs-lookup"><span data-stu-id="4fde2-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="4fde2-134">**HrComposeMsgID** позволяет клиентским приложениям для работы с объектами в нескольких хранилищ посредством использования идентификаторы составные записей.</span><span class="sxs-lookup"><span data-stu-id="4fde2-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="4fde2-135">Приложение может вызвать функцию [HrDecomposeMsgID](hrdecomposemsgid.md) для разделения идентификатор составные записи в его исходное деловых партнеров.</span><span class="sxs-lookup"><span data-stu-id="4fde2-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

