---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d6f983e49132e7ab6ea402a8e32bb5ec56d1efba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564852"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="75ee7-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="75ee7-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="75ee7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75ee7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75ee7-105">Сравнение двух идентификаторы записей, относящихся к конкретной адресной книге, чтобы определить, является ли они ссылаются на один и тот же объект адресной книги.</span><span class="sxs-lookup"><span data-stu-id="75ee7-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="75ee7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75ee7-106">Parameters</span></span>

 <span data-ttu-id="75ee7-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="75ee7-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="75ee7-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="75ee7-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="75ee7-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="75ee7-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="75ee7-110">[in] Указатель на первый идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="75ee7-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="75ee7-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="75ee7-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="75ee7-112">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="75ee7-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="75ee7-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="75ee7-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="75ee7-114">[in] Указатель на второй идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="75ee7-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="75ee7-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="75ee7-115">_ulFlags_</span></span>
  
> <span data-ttu-id="75ee7-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="75ee7-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="75ee7-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="75ee7-117">_lpulResult_</span></span>
  
> <span data-ttu-id="75ee7-118">[out] Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="75ee7-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="75ee7-119">Содержимое _lpulResult_ присвоено значение TRUE, если идентификаторы двух записей ссылаются на тот же объект; в противном случае содержимое присвоено значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="75ee7-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="75ee7-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="75ee7-120">Return value</span></span>

<span data-ttu-id="75ee7-121">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="75ee7-121">S_OK</span></span> 
  
> <span data-ttu-id="75ee7-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="75ee7-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="75ee7-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="75ee7-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="75ee7-124">Одно или оба идентификаторы записей, переданными параметрами _lpEntryID1_ или _lpEntryID2_ не распознается любой поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="75ee7-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="75ee7-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="75ee7-125">Remarks</span></span>

<span data-ttu-id="75ee7-126">Клиентские приложения и службы поставщиков вызовите метод **CompareEntryIDs** для сравнения двух идентификаторов запись, к которой принадлежит поставщик единого адресной книги для определения, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="75ee7-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="75ee7-127">**CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="75ee7-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="75ee7-128">Это может произойти, например, после установки новой версии поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="75ee7-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="75ee7-129">MAPI передает этот вызов для доступа к адресной книге, который несет ответственность за идентификаторы записей определение нужного поставщика, сопоставляя структуры [MAPIUID](mapiuid.md) в идентификаторы записей со структурой **MAPIUID** , зарегистрированные, Поставщик.</span><span class="sxs-lookup"><span data-stu-id="75ee7-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="75ee7-130">Если идентификаторы двух записей ссылаются на тот же объект, **CompareEntryIDs** задает содержимое параметр _lpulResult_ имеет значение TRUE; Если они ссылаются на разных объектов, **CompareEntryIDs** задает содержимое значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="75ee7-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="75ee7-131">В любом случае **CompareEntryIDs** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="75ee7-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="75ee7-132">Если **CompareEntryIDs** возвращает ошибку, которая может возникнуть, если доступа к адресной книге зарегистрировала структура **MAPIUID** , соответствует одному в идентификаторы записей, клиентов и поставщиков не должен выполнять каких-либо действий на основе результатов из сравнение.</span><span class="sxs-lookup"><span data-stu-id="75ee7-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="75ee7-133">Вместо этого они должен выполнять самый высокий подход к действие, выполняемое.</span><span class="sxs-lookup"><span data-stu-id="75ee7-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="75ee7-134">См. также</span><span class="sxs-lookup"><span data-stu-id="75ee7-134">See also</span></span>



[<span data-ttu-id="75ee7-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="75ee7-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

