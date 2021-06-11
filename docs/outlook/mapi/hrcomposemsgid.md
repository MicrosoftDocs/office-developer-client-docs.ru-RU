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
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424065"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="a7cde-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="a7cde-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="a7cde-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7cde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7cde-105">Создает строку ASCII, представляющую сложный идентификатор входа для объекта, обычно сообщение в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="a7cde-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7cde-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a7cde-106">Header file:</span></span>  <br/> |<span data-ttu-id="a7cde-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a7cde-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a7cde-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a7cde-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a7cde-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a7cde-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a7cde-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a7cde-110">Called by:</span></span>  <br/> |<span data-ttu-id="a7cde-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="a7cde-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a7cde-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="a7cde-112">Parameters</span></span>

 <span data-ttu-id="a7cde-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="a7cde-113">_psession_</span></span>
  
> <span data-ttu-id="a7cde-114">[in] Указатель на сеанс, который используется клиентом приложения.</span><span class="sxs-lookup"><span data-stu-id="a7cde-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="a7cde-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="a7cde-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="a7cde-116">[in] Размер в bytes ключа записи магазина сообщений, который содержит сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="a7cde-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="a7cde-117">Если в  _параметре cbStoreRecordKey_ передается ноль, параметр  _pszMsgID_ указывает на копию идентификатора записи, преобразованного в текст.</span><span class="sxs-lookup"><span data-stu-id="a7cde-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="a7cde-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="a7cde-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="a7cde-119">[in] Указатель на ключ записи в хранилище сообщений, содержащий сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="a7cde-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="a7cde-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="a7cde-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="a7cde-121">[in] Размер в bytes идентификатора входа сообщения или другого объекта.</span><span class="sxs-lookup"><span data-stu-id="a7cde-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="a7cde-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="a7cde-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="a7cde-123">[in] Указатель на идентификатор входа объекта.</span><span class="sxs-lookup"><span data-stu-id="a7cde-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="a7cde-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="a7cde-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="a7cde-125">[вышел] Указатель на возвращенную строку ASCII.</span><span class="sxs-lookup"><span data-stu-id="a7cde-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="a7cde-126">Если параметр  _cbStoreRecordKey_ больше нуля, параметр  _pszMsgID_ указывает на сложный идентификатор входа, преобразованный в текст.</span><span class="sxs-lookup"><span data-stu-id="a7cde-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="a7cde-127">Если  _значение cbStoreRecordKey_ нулевое,  _pszMsgID_ указывает на идентификатор некомпетентной записи, преобразованный в текст.</span><span class="sxs-lookup"><span data-stu-id="a7cde-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a7cde-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7cde-128">Return value</span></span>

<span data-ttu-id="a7cde-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="a7cde-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7cde-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7cde-130">Remarks</span></span>

<span data-ttu-id="a7cde-131">Если сообщение или другой объект, для которого создается идентификатор сложной записи, находится в хранилище сообщений, строка идентификатора создается из идентификатора входа объекта и ключа записи магазина.</span><span class="sxs-lookup"><span data-stu-id="a7cde-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="a7cde-132">Если объекта нет в магазине, то есть если количество byte для ключа записи магазина, переданного в  _параметре cbStoreRecordKey,_ нулевое, идентификатор входа объекта просто копируется и преобразуется в строку.</span><span class="sxs-lookup"><span data-stu-id="a7cde-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="a7cde-133">Вызов **функции HrComposeMsgID** эквивалентен вызову функции [HrComposeEID,](hrcomposeeid.md) а затем [функции HrSzFromEntryID.](hrszfromentryid.md)</span><span class="sxs-lookup"><span data-stu-id="a7cde-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="a7cde-134">**HrComposeMsgID** позволяет клиентские приложения работать с объектами в нескольких магазинах с помощью идентификаторов сложной записи.</span><span class="sxs-lookup"><span data-stu-id="a7cde-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="a7cde-135">Приложение может вызвать функцию [HrDecomposeMsgID,](hrdecomposemsgid.md) чтобы разделить идентификатор входного соединения на исходные составляющие.</span><span class="sxs-lookup"><span data-stu-id="a7cde-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

