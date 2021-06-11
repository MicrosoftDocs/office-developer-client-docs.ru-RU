---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431045"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="63f65-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="63f65-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="63f65-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63f65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63f65-105">Сравнивает два идентификатора записи, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="63f65-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="63f65-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="63f65-106">Parameters</span></span>

 <span data-ttu-id="63f65-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="63f65-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="63f65-108">[in] Количество byte в идентификаторе входа, на который указывает параметр _lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="63f65-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="63f65-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="63f65-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="63f65-110">[in] Указатель на первый идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="63f65-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="63f65-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="63f65-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="63f65-112">[in] Количество byte в идентификаторе входа, на который указывает параметр _lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="63f65-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="63f65-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="63f65-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="63f65-114">[in] Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="63f65-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="63f65-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63f65-115">_ulFlags_</span></span>
  
> <span data-ttu-id="63f65-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="63f65-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="63f65-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="63f65-117">_lpulResult_</span></span>
  
> <span data-ttu-id="63f65-118">[вышел] Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="63f65-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="63f65-119">TRUE, если два идентификатора записи относятся к одному объекту; в противном случае FALSE.</span><span class="sxs-lookup"><span data-stu-id="63f65-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63f65-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63f65-120">Return value</span></span>

<span data-ttu-id="63f65-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="63f65-121">S_OK</span></span> 
  
> <span data-ttu-id="63f65-122">Сравнение было успешным.</span><span class="sxs-lookup"><span data-stu-id="63f65-122">The comparison was successful.</span></span>
    
<span data-ttu-id="63f65-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="63f65-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="63f65-124">Один или оба идентификатора записи, указанных в качестве параметров, не относятся к допустимым объектам, возможно, потому, что они в настоящее время не были отперты и недоступны.</span><span class="sxs-lookup"><span data-stu-id="63f65-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63f65-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="63f65-125">Remarks</span></span>

<span data-ttu-id="63f65-126">Метод **IMAPISupport::CompareEntryIDs** реализован для объектов поддержки поставщиков адресной книги и магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="63f65-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="63f65-127">**CompareEntryIDs** сравнивает два идентификатора записи, принадлежащих одному поставщику услуг, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="63f65-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="63f65-128">MAPI извлекает часть [MAPIUID](mapiuid.md) из идентификаторов записи, чтобы определить поставщика услуг, ответственного за объекты.</span><span class="sxs-lookup"><span data-stu-id="63f65-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="63f65-129">Затем MAPI вызывает метод **CompareEntryIDs** объекта с логотипом для выполнения сравнения.</span><span class="sxs-lookup"><span data-stu-id="63f65-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="63f65-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="63f65-130">Notes to callers</span></span>

 <span data-ttu-id="63f65-131">**CompareEntryIDs полезен,** так как объект может иметь несколько допустимых идентификаторов записи.</span><span class="sxs-lookup"><span data-stu-id="63f65-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="63f65-132">Такая ситуация может возникнуть, например, после установки новой версии поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="63f65-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="63f65-133">Если **compareEntryIDs** возвращает ошибку, не принимайте никаких действий в зависимости от результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="63f65-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="63f65-134">Вместо этого примите наиболее консервативный подход.</span><span class="sxs-lookup"><span data-stu-id="63f65-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="63f65-135">**CompareEntryIDs может** привести к сбой, если, например, один или оба идентификатора записи содержат недействительные **структуры MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="63f65-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="63f65-136">См. также</span><span class="sxs-lookup"><span data-stu-id="63f65-136">See also</span></span>



[<span data-ttu-id="63f65-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="63f65-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="63f65-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="63f65-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

