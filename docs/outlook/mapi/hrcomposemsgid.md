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
# <a name="hrcomposemsgid"></a><span data-ttu-id="d79d4-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="d79d4-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="d79d4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d79d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d79d4-105">Создает строку ASCII, представляющую составной идентификатор записи для объекта, обычно это сообщение в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="d79d4-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d79d4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d79d4-106">Header file:</span></span>  <br/> |<span data-ttu-id="d79d4-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="d79d4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d79d4-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d79d4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d79d4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d79d4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d79d4-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d79d4-110">Called by:</span></span>  <br/> |<span data-ttu-id="d79d4-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="d79d4-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d79d4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d79d4-112">Parameters</span></span>

 <span data-ttu-id="d79d4-113">_псессион_</span><span class="sxs-lookup"><span data-stu-id="d79d4-113">_psession_</span></span>
  
> <span data-ttu-id="d79d4-114">возврата Указатель на сеанс, используемый клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="d79d4-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="d79d4-115">_Кбсторерекордкэй_</span><span class="sxs-lookup"><span data-stu-id="d79d4-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="d79d4-116">возврата Размер (в байтах) ключа записи хранилища сообщений, содержащего сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="d79d4-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="d79d4-117">Если в параметре _кбсторерекордкэй_ передается нулевое значение, параметр _псзмсгид_ указывает на копию идентификатора записи, преобразованного в текст.</span><span class="sxs-lookup"><span data-stu-id="d79d4-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="d79d4-118">_Псторерекордкэй_</span><span class="sxs-lookup"><span data-stu-id="d79d4-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="d79d4-119">возврата Указатель на ключ записи хранилища сообщений, содержащего сообщение или другой объект.</span><span class="sxs-lookup"><span data-stu-id="d79d4-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="d79d4-120">_Кбмсжеид_</span><span class="sxs-lookup"><span data-stu-id="d79d4-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="d79d4-121">возврата Размер (в байтах) идентификатора записи сообщения или другого объекта.</span><span class="sxs-lookup"><span data-stu-id="d79d4-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="d79d4-122">_Пмсжеид_</span><span class="sxs-lookup"><span data-stu-id="d79d4-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="d79d4-123">возврата Указатель на идентификатор записи объекта.</span><span class="sxs-lookup"><span data-stu-id="d79d4-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="d79d4-124">_Псзмсгид_</span><span class="sxs-lookup"><span data-stu-id="d79d4-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="d79d4-125">вышли Указатель на возвращаемую строку ASCII.</span><span class="sxs-lookup"><span data-stu-id="d79d4-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="d79d4-126">Если значение параметра _кбсторерекордкэй_ больше нуля, параметр _псзмсгид_ указывает на идентификатор составной записи, преобразованный в текст.</span><span class="sxs-lookup"><span data-stu-id="d79d4-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="d79d4-127">Если _кбсторерекордкэй_ имеет нулевое значение, _псзмсгид_ указывает на несоставной идентификатор операции, преобразованный в текст.</span><span class="sxs-lookup"><span data-stu-id="d79d4-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d79d4-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d79d4-128">Return value</span></span>

<span data-ttu-id="d79d4-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="d79d4-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d79d4-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="d79d4-130">Remarks</span></span>

<span data-ttu-id="d79d4-131">Если сообщение или другой объект, для которого создается создаваемый идентификатор составного элемента, находится в хранилище сообщений, строка идентификатора создается из идентификатора записи объекта и ключа записи в хранилище.</span><span class="sxs-lookup"><span data-stu-id="d79d4-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="d79d4-132">Если объект не находится в хранилище, то есть, если количество байт для ключа записи хранилища, переданное в параметре _кбсторерекордкэй_ , равно нулю, то идентификатор записи объекта просто копируется и преобразуется в строку.</span><span class="sxs-lookup"><span data-stu-id="d79d4-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="d79d4-133">Вызов функции **хркомпосемсгид** эквивалентен вызову функции [хркомпосиид](hrcomposeeid.md) , а затем функции [хрсзфроментрид](hrszfromentryid.md) .</span><span class="sxs-lookup"><span data-stu-id="d79d4-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="d79d4-134">**Хркомпосемсгид** позволяет клиентским приложениям работать с объектами в нескольких хранилищах с помощью составных идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="d79d4-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="d79d4-135">Приложение может вызвать функцию [хрдекомпосемсгид](hrdecomposemsgid.md) , чтобы разделить идентификатор составной записи на исходные составляющие.</span><span class="sxs-lookup"><span data-stu-id="d79d4-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

