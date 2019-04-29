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
# <a name="hrdecomposemsgid"></a><span data-ttu-id="8ad98-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="8ad98-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="8ad98-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ad98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ad98-105">Отделяет представление ASCII для идентификатора составной записи объекта, как правило, к сообщению в хранилище сообщений, к идентификатору записи этого объекта в хранилище и идентификатору записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="8ad98-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ad98-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8ad98-106">Header file:</span></span>  <br/> |<span data-ttu-id="8ad98-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="8ad98-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8ad98-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8ad98-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8ad98-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8ad98-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8ad98-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8ad98-110">Called by:</span></span>  <br/> |<span data-ttu-id="8ad98-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="8ad98-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="8ad98-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ad98-112">Parameters</span></span>

 <span data-ttu-id="8ad98-113">_псессион_</span><span class="sxs-lookup"><span data-stu-id="8ad98-113">_psession_</span></span>
  
> <span data-ttu-id="8ad98-114">возврата Указатель на сеанс, используемый клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="8ad98-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="8ad98-115">_Сзмсгид_</span><span class="sxs-lookup"><span data-stu-id="8ad98-115">_szMsgID_</span></span>
  
> <span data-ttu-id="8ad98-116">возврата Строка, представляющая идентификатор записи объекта.</span><span class="sxs-lookup"><span data-stu-id="8ad98-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="8ad98-117">_Пкбсториид_</span><span class="sxs-lookup"><span data-stu-id="8ad98-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="8ad98-118">вышли Указатель на возвращенный размер (в байтах) идентификатора записи для хранилища сообщений, содержащего объект.</span><span class="sxs-lookup"><span data-stu-id="8ad98-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="8ad98-119">Если параметр _сзмсгид_ указывает на строку несоставного идентификатора записи, параметр _пкбсториид_ указывает на ноль.</span><span class="sxs-lookup"><span data-stu-id="8ad98-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="8ad98-120">_Ппсториид_</span><span class="sxs-lookup"><span data-stu-id="8ad98-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="8ad98-121">вышли Указатель на указатель возвращаемого идентификатора записи хранилища сообщений, содержащего объект.</span><span class="sxs-lookup"><span data-stu-id="8ad98-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="8ad98-122">Если параметр _сзмсгид_ указывает на несоставный идентификатор записи, в параметре _ППСТОРИИД_ возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="8ad98-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="8ad98-123">_Пкбмсжеид_</span><span class="sxs-lookup"><span data-stu-id="8ad98-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="8ad98-124">вышли Указатель на возвращенный размер (в байтах) идентификатора записи объекта в его хранилище.</span><span class="sxs-lookup"><span data-stu-id="8ad98-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="8ad98-125">Если параметр _сзмсгид_ указывает на строку несоставного идентификатора записи, параметр _пкбмсжеид_ равен значению параметра _кбеид_ .</span><span class="sxs-lookup"><span data-stu-id="8ad98-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="8ad98-126">_Ппмсжеид_</span><span class="sxs-lookup"><span data-stu-id="8ad98-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="8ad98-127">вышли Указатель на указатель на возвращаемую строку идентификатора записи объекта в его хранилище.</span><span class="sxs-lookup"><span data-stu-id="8ad98-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="8ad98-128">Если параметр _сзмсгид_ указывает на несоставной идентификатор записи, _ппмсжеид_ указывает на указатель на преобразованную копию несоставного идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="8ad98-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8ad98-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ad98-129">Return value</span></span>

<span data-ttu-id="8ad98-130">Нет.</span><span class="sxs-lookup"><span data-stu-id="8ad98-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ad98-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ad98-131">Remarks</span></span>

<span data-ttu-id="8ad98-132">Если идентификатор, указанный в параметре _сзмсгид_ , является составным, он преобразуется из ASCII и разбивается на идентификатор записи объекта в его банке сообщений и идентификаторе записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="8ad98-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="8ad98-133">Строки несоставных идентификаторов записей просто преобразуются и копируются.</span><span class="sxs-lookup"><span data-stu-id="8ad98-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="8ad98-134">Строка составного идентификатора, которая должна быть разделена, обычно создана с помощью функции [хркомпосемсгид](hrcomposemsgid.md) .</span><span class="sxs-lookup"><span data-stu-id="8ad98-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="8ad98-135">Вызов функции **хрдекомпосемсгид** эквивалентен вызову функции [хрентридфромсз](hrentryidfromsz.md) , а затем функции [хрдекомпосиид](hrdecomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="8ad98-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

