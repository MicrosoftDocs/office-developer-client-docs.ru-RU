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
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="0737c-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="0737c-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="0737c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0737c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0737c-105">Сравнивает два идентификатора записей, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="0737c-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="0737c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0737c-106">Parameters</span></span>

 <span data-ttu-id="0737c-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="0737c-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="0737c-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="0737c-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="0737c-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="0737c-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="0737c-110">[in] Указатель на идентификатор первой записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="0737c-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="0737c-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="0737c-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="0737c-112">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="0737c-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="0737c-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="0737c-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="0737c-114">[in] Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="0737c-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="0737c-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0737c-115">_ulFlags_</span></span>
  
> <span data-ttu-id="0737c-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="0737c-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0737c-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="0737c-117">_lpulResult_</span></span>
  
> <span data-ttu-id="0737c-118">[out] Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="0737c-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="0737c-119">TRUE, если два идентификатора записей ссылаются на один и тот же объект; в противном случае false.</span><span class="sxs-lookup"><span data-stu-id="0737c-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0737c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0737c-120">Return value</span></span>

<span data-ttu-id="0737c-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="0737c-121">S_OK</span></span> 
  
> <span data-ttu-id="0737c-122">Сравнение было успешным.</span><span class="sxs-lookup"><span data-stu-id="0737c-122">The comparison was successful.</span></span>
    
<span data-ttu-id="0737c-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0737c-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="0737c-124">Один или оба идентификатора записей, указанных в качестве параметров, не ссылаются на допустимые объекты, возможно, из-за того, что они в настоящее время не работают и недоступны.</span><span class="sxs-lookup"><span data-stu-id="0737c-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0737c-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="0737c-125">Remarks</span></span>

<span data-ttu-id="0737c-126">Метод **IMAPISupport::CompareEntryIDs** реализован для объектов поддержки адресной книги и поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="0737c-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="0737c-127">**CompareEntryIDs** сравнивает два идентификатора записей, принадлежащих одному поставщику услуг, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="0737c-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="0737c-128">MAPI извлекает часть [MAPIUID](mapiuid.md) из идентификаторов записей, чтобы определить поставщика услуг, ответственного за объекты.</span><span class="sxs-lookup"><span data-stu-id="0737c-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="0737c-129">Затем MAPI вызывает метод **CompareEntryIDs** объекта для его логотипа для выполнения сравнения.</span><span class="sxs-lookup"><span data-stu-id="0737c-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0737c-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="0737c-130">Notes to callers</span></span>

 <span data-ttu-id="0737c-131">**CompareEntryIDs полезен,** так как объект может иметь несколько допустимых идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="0737c-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="0737c-132">Это может произойти, например, после установки новой версии поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="0737c-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="0737c-133">Если **CompareEntryIDs** возвращает ошибку, не принимайте никаких действий на основе результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="0737c-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="0737c-134">Вместо этого вы можете использовать наиболее емкий подход.</span><span class="sxs-lookup"><span data-stu-id="0737c-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="0737c-135">**CompareEntryIDs** может привести к сбой, если, например, один или оба идентификатора записи содержат недействительные **структуры MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="0737c-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0737c-136">См. также</span><span class="sxs-lookup"><span data-stu-id="0737c-136">See also</span></span>



[<span data-ttu-id="0737c-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0737c-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="0737c-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0737c-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

