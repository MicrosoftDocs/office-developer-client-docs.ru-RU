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
# <a name="hrdecomposemsgid"></a><span data-ttu-id="a206b-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="a206b-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="a206b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a206b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a206b-105">Отделяет представление ASCII составного идентификатора записи объекта ( обычно сообщения в хранилище сообщений) в идентификатор записи этого объекта в хранилище и идентификатор записи в хранилище.</span><span class="sxs-lookup"><span data-stu-id="a206b-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a206b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a206b-106">Header file:</span></span>  <br/> |<span data-ttu-id="a206b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a206b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a206b-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a206b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a206b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a206b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a206b-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a206b-110">Called by:</span></span>  <br/> |<span data-ttu-id="a206b-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="a206b-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a206b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a206b-112">Parameters</span></span>

 <span data-ttu-id="a206b-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="a206b-113">_psession_</span></span>
  
> <span data-ttu-id="a206b-114">[in] Указатель на сеанс, который использует клиентский приложение.</span><span class="sxs-lookup"><span data-stu-id="a206b-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="a206b-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="a206b-115">_szMsgID_</span></span>
  
> <span data-ttu-id="a206b-116">[in] Строка, представляющая идентификатор записи объекта.</span><span class="sxs-lookup"><span data-stu-id="a206b-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="a206b-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="a206b-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="a206b-118">[out] Указатель на возвращенный размер (в bytes) идентификатора записи в хранилище сообщений, которое содержит объект.</span><span class="sxs-lookup"><span data-stu-id="a206b-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="a206b-119">Если параметр  _szMsgID_ указывает на несочетаемую строку идентификатора записи, параметр  _pcbStoreEID_ указывает на ноль.</span><span class="sxs-lookup"><span data-stu-id="a206b-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="a206b-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="a206b-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="a206b-121">[out] Указатель на указатель на возвращенный идентификатор записи в хранилище сообщений, содержаном объект.</span><span class="sxs-lookup"><span data-stu-id="a206b-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="a206b-122">Если параметр  _szMsgID_ указывает на несовершенный идентификатор записи, в параметре  _ppStoreEID_ возвращается NULL.</span><span class="sxs-lookup"><span data-stu-id="a206b-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="a206b-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="a206b-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="a206b-124">[out] Указатель на возвращенный размер (в bytes) идентификатора записи объекта в его хранилище.</span><span class="sxs-lookup"><span data-stu-id="a206b-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="a206b-125">Если параметр _szMsgID_ указывает на несочетаемую строку идентификатора записи, то параметр _pcbMsgEID_ равен значению параметра _cbEID._</span><span class="sxs-lookup"><span data-stu-id="a206b-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="a206b-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="a206b-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="a206b-127">[out] Указатель на указатель на возвращенную строку идентификатора записи объекта в его хранилище.</span><span class="sxs-lookup"><span data-stu-id="a206b-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="a206b-128">Если параметр  _szMsgID_ указывает на несовершенный идентификатор записи,  _ppMsgEID_ указывает на указатель на преобразованную копию несовершенного идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="a206b-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a206b-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a206b-129">Return value</span></span>

<span data-ttu-id="a206b-130">Нет.</span><span class="sxs-lookup"><span data-stu-id="a206b-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a206b-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="a206b-131">Remarks</span></span>

<span data-ttu-id="a206b-132">Если идентификатор, указанный параметром  _szMsgID,_ является составным, он преобразуется из ASCII и делится на идентификатор записи объекта в хранилище сообщений и идентификатор записи в хранилище.</span><span class="sxs-lookup"><span data-stu-id="a206b-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="a206b-133">Строки идентификатора несочетаемой записи просто преобразуются и копируется.</span><span class="sxs-lookup"><span data-stu-id="a206b-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="a206b-134">Составная строка идентификатора, которая должна быть разделена, обычно создается функцией [HrComposeMsgID.](hrcomposemsgid.md)</span><span class="sxs-lookup"><span data-stu-id="a206b-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="a206b-135">Вызов **функции HrDecomposeMsgID эквивалентен** вызову функции [HrEntryIDFromSz,](hrentryidfromsz.md) а затем [— функции HrDecomposeEID.](hrdecomposeeid.md)</span><span class="sxs-lookup"><span data-stu-id="a206b-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

