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
ms.openlocfilehash: 3095907498b1ce7ae6b3666e0678dd0c5f76c23e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808657"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="7b627-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="7b627-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="7b627-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b627-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b627-105">Разделяет представления ASCII составные запись идентификатор объекта, обычно сообщения в банке сообщений в идентификатор записи этого объекта в хранилище и идентификатор записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="7b627-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b627-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7b627-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b627-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7b627-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7b627-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="7b627-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b627-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b627-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b627-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="7b627-110">Called by:</span></span>  <br/> |<span data-ttu-id="7b627-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="7b627-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7b627-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b627-112">Parameters</span></span>

 <span data-ttu-id="7b627-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="7b627-113">_psession_</span></span>
  
> <span data-ttu-id="7b627-114">[in] Указатель на сеанс используется клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="7b627-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="7b627-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="7b627-115">_szMsgID_</span></span>
  
> <span data-ttu-id="7b627-116">[in] Строка, представляющая запись идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="7b627-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="7b627-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="7b627-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="7b627-118">[out] Указатель на возвращаемый размер, в байтах, идентификатор записи хранилища сообщение, содержащее объект.</span><span class="sxs-lookup"><span data-stu-id="7b627-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="7b627-119">Если параметр _szMsgID_ указывает идентификатор noncompound записи строка, затем указывает параметр _pcbStoreEID_ присваивается значение 0.</span><span class="sxs-lookup"><span data-stu-id="7b627-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="7b627-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="7b627-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="7b627-121">[out] Указатель на указатель на идентификатор возвращенного элемента хранилища сообщение, содержащее объект.</span><span class="sxs-lookup"><span data-stu-id="7b627-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="7b627-122">Если параметр _szMsgID_ указывает идентификатор noncompound записи, с помощью параметра _ppStoreEID_ возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="7b627-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="7b627-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="7b627-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="7b627-124">[out] Указатель на возвращаемый размер, в байтах, запись идентификатор объекта в его хранилище.</span><span class="sxs-lookup"><span data-stu-id="7b627-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="7b627-125">Если параметр _szMsgID_ указывает строка идентификатора noncompound запись, параметр _pcbMsgEID_ равно значению параметра _cbEID_ .</span><span class="sxs-lookup"><span data-stu-id="7b627-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="7b627-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="7b627-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="7b627-127">[out] Указатель на указатель строки идентификатора возвращенного элемента объекта в его хранилище.</span><span class="sxs-lookup"><span data-stu-id="7b627-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="7b627-128">Если параметр _szMsgID_ указывает идентификатор noncompound записи, _ppMsgEID_ указывает указатель преобразованной копии идентификатор noncompound записи.</span><span class="sxs-lookup"><span data-stu-id="7b627-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7b627-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b627-129">Return value</span></span>

<span data-ttu-id="7b627-130">Нет.</span><span class="sxs-lookup"><span data-stu-id="7b627-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b627-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b627-131">Remarks</span></span>

<span data-ttu-id="7b627-132">Если идентификатор, указанный в параметре _szMsgID_ составные, преобразованных из ASCII и разделены на идентификатор записи объекта в его хранилища сообщений и идентификатор записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="7b627-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="7b627-133">Строки идентификатора noncompound запись просто преобразуются и копируются.</span><span class="sxs-lookup"><span data-stu-id="7b627-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="7b627-134">Составные идентификатор строку, которую нужно разделить — это обычно один создан с помощью функции [HrComposeMsgID](hrcomposemsgid.md) .</span><span class="sxs-lookup"><span data-stu-id="7b627-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="7b627-135">Вызов функции **HrDecomposeMsgID** эквивалентен вызову функции [HrEntryIDFromSz](hrentryidfromsz.md) , а затем функцию [HrDecomposeEID](hrdecomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="7b627-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

