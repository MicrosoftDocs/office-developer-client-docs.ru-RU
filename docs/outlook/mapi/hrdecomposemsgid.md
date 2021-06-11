---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404437"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="5031d-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="5031d-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="5031d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5031d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5031d-105">Отделяет представление ASCII сложного идентификатора входа объекта, обычно сообщения в хранилище сообщений, в идентификатор входа этого объекта в магазине и идентификатор входа в хранилище.</span><span class="sxs-lookup"><span data-stu-id="5031d-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5031d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5031d-106">Header file:</span></span>  <br/> |<span data-ttu-id="5031d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5031d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5031d-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="5031d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5031d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5031d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5031d-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="5031d-110">Called by:</span></span>  <br/> |<span data-ttu-id="5031d-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="5031d-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="5031d-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="5031d-112">Parameters</span></span>

 <span data-ttu-id="5031d-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="5031d-113">_psession_</span></span>
  
> <span data-ttu-id="5031d-114">[in] Указатель на сеанс, который используется клиентом приложения.</span><span class="sxs-lookup"><span data-stu-id="5031d-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="5031d-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="5031d-115">_szMsgID_</span></span>
  
> <span data-ttu-id="5031d-116">[in] Строка, представляющая идентификатор входа объекта.</span><span class="sxs-lookup"><span data-stu-id="5031d-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="5031d-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="5031d-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="5031d-118">[вышел] Указатель на возвращенный размер, в bytes, идентификатор входа в хранилище сообщений, который содержит объект.</span><span class="sxs-lookup"><span data-stu-id="5031d-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="5031d-119">Если параметр  _szMsgID указывает_ на строку идентификатора некомпонентной записи, то параметр  _pcbStoreEID_ указывает на ноль.</span><span class="sxs-lookup"><span data-stu-id="5031d-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="5031d-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="5031d-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="5031d-121">[вышел] Указатель на указатель на возвращенный идентификатор входа в хранилище сообщений, содержащий объект.</span><span class="sxs-lookup"><span data-stu-id="5031d-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="5031d-122">Если _параметр szMsgID_ указывает на идентификатор некомпонентной записи, NULL возвращается в _параметре ppStoreEID._</span><span class="sxs-lookup"><span data-stu-id="5031d-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="5031d-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="5031d-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="5031d-124">[вышел] Указатель на возвращенный размер в bytes идентификатора входа объекта в его хранилище.</span><span class="sxs-lookup"><span data-stu-id="5031d-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="5031d-125">Если параметр _szMsgID_ указывает на строку идентификатора некомпонентной записи, то параметр _pcbMsgEID_ равен значению параметра _cbEID._</span><span class="sxs-lookup"><span data-stu-id="5031d-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="5031d-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="5031d-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="5031d-127">[вышел] Указатель на указатель на строку идентификатора возвращаемого входа объекта в магазине.</span><span class="sxs-lookup"><span data-stu-id="5031d-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="5031d-128">Если параметр  _szMsgID_ указывает на идентификатор некомпонентной записи,  _ppMsgEID_ указывает на указатель на преобразованную копию идентификатора некомпонентной записи.</span><span class="sxs-lookup"><span data-stu-id="5031d-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5031d-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5031d-129">Return value</span></span>

<span data-ttu-id="5031d-130">Нет.</span><span class="sxs-lookup"><span data-stu-id="5031d-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5031d-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="5031d-131">Remarks</span></span>

<span data-ttu-id="5031d-132">Если идентификатор, указанный  _параметром szMsgID,_ является составным, он преобразуется из ASCII и делится на идентификатор входа объекта в хранилище сообщений и идентификатор входа магазина.</span><span class="sxs-lookup"><span data-stu-id="5031d-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="5031d-133">Строки идентификатора некомпонентной записи просто преобразуются и копируется.</span><span class="sxs-lookup"><span data-stu-id="5031d-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="5031d-134">Выделенная строка идентификатора соединения обычно создается функцией [HrComposeMsgID.](hrcomposemsgid.md)</span><span class="sxs-lookup"><span data-stu-id="5031d-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="5031d-135">Вызов **функции HrDecomposeMsgID** эквивалентен вызову функции [HrEntryIDFromSz,](hrentryidfromsz.md) а затем [функции HrDecomposeEID.](hrdecomposeeid.md)</span><span class="sxs-lookup"><span data-stu-id="5031d-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

