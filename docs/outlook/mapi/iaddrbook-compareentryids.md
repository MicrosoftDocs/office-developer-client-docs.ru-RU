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
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424261"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="22058-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="22058-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="22058-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22058-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22058-105">Сравнивает два идентификатора записей, принадлежащих конкретному поставщику адресной книги, чтобы определить, относятся ли они к одному объекту адресной книги.</span><span class="sxs-lookup"><span data-stu-id="22058-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="22058-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22058-106">Parameters</span></span>

 <span data-ttu-id="22058-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="22058-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="22058-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="22058-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="22058-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="22058-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="22058-110">[in] Указатель на идентификатор первой записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="22058-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="22058-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="22058-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="22058-112">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="22058-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="22058-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="22058-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="22058-114">[in] Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="22058-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="22058-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="22058-115">_ulFlags_</span></span>
  
> <span data-ttu-id="22058-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="22058-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="22058-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="22058-117">_lpulResult_</span></span>
  
> <span data-ttu-id="22058-118">[out] Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="22058-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="22058-119">Для содержимого  _lpulResult устанавливается_ true, если два идентификатора записи ссылаются на один и тот же объект; в противном случае для содержимого установлено false.</span><span class="sxs-lookup"><span data-stu-id="22058-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="22058-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22058-120">Return value</span></span>

<span data-ttu-id="22058-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="22058-121">S_OK</span></span> 
  
> <span data-ttu-id="22058-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="22058-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="22058-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="22058-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="22058-124">Один или оба идентификатора записей, переданных с помощью  _параметров lpEntryID1_ или  _lpEntryID2,_ не распознаются ни одним поставщиком адресной книги.</span><span class="sxs-lookup"><span data-stu-id="22058-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="22058-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="22058-125">Remarks</span></span>

<span data-ttu-id="22058-126">Клиентские приложения и поставщики услуг вызывают метод **CompareEntryIDs** для сравнения двух идентификаторов записей, принадлежащих одному поставщику адресной книги, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="22058-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="22058-127">**CompareEntryIDs полезен,** так как объект может иметь несколько допустимых идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="22058-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="22058-128">Это может произойти, например, после установки новой версии поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="22058-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="22058-129">MAPI передает этот вызов поставщику адресной книги, который отвечает за идентификаторы записей, определяя соответствующего поставщика путем совпадения структуры [MAPIUID](mapiuid.md) в идентификаторах записей со структурой **MAPIUID,** зарегистрированной поставщиком.</span><span class="sxs-lookup"><span data-stu-id="22058-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="22058-130">Если два идентификатора записей ссылаются на один и тот же объект, **CompareEntryIDs** задает для содержимого параметра  _lpulResult_ параметр TRUE; Если они ссылаются на разные объекты, **CompareEntryIDs** задает для содержимого false.</span><span class="sxs-lookup"><span data-stu-id="22058-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="22058-131">В любом случае **compareEntryIDs** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="22058-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="22058-132">Если **compareEntryIDs** возвращает ошибку, которая может возникнуть, если ни один поставщик адресной книги не зарегистрировал структуру **MAPIUID,** которая соответствует структуре в идентификаторах записей, клиенты и поставщики не должны принимать никаких действий на основе результатов сравнения.</span><span class="sxs-lookup"><span data-stu-id="22058-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="22058-133">Вместо этого они должны использовать наиболее емкий подход к выполняемому действию.</span><span class="sxs-lookup"><span data-stu-id="22058-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22058-134">См. также</span><span class="sxs-lookup"><span data-stu-id="22058-134">See also</span></span>



[<span data-ttu-id="22058-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="22058-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

