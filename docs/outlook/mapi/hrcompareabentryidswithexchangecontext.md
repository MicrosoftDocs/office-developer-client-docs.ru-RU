---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436435"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="c168b-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="c168b-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="c168b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c168b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c168b-105">Сравнивает два входа **в адресную** книгу безопасно в Exchange профиле.</span><span class="sxs-lookup"><span data-stu-id="c168b-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="c168b-106">Эта функция является функцией замены [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="c168b-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c168b-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c168b-107">Header file:</span></span>  <br/> |<span data-ttu-id="c168b-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="c168b-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="c168b-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c168b-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="c168b-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="c168b-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="c168b-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c168b-111">Called by:</span></span>  <br/> |<span data-ttu-id="c168b-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c168b-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="c168b-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="c168b-113">Parameters</span></span>

 <span data-ttu-id="c168b-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="c168b-114">_pmsess_</span></span>
  
> <span data-ttu-id="c168b-115">[in] Журнал на **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="c168b-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="c168b-116">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="c168b-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c168b-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="c168b-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="c168b-118">[in] Указатель на **emsmdbUID,** который идентифицирует службу Exchange, которая содержит поставщик адресных книг Exchange, который эта функция должна использовать для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="c168b-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="c168b-119">Если идентификатор входной записи не является идентификатором Exchange поставщика адресных книг, этот параметр игнорируется, и вызов функции ведет себя так же, как [iAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="c168b-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="c168b-120">Если этот параметр является NULL или нулевой MAPIUID, эта функция ведет себя как [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="c168b-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="c168b-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="c168b-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="c168b-122">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="c168b-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="c168b-123">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="c168b-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c168b-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="c168b-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="c168b-125">[in] Количество byte первого идентификатора записи, указанного параметром _lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="c168b-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="c168b-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="c168b-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="c168b-127">[in] Указатель на первый идентификатор записи, который представляет запись адресной книги для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c168b-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="c168b-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="c168b-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="c168b-129">[in] Количество byte второго идентификатора записи, указанного параметром _lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="c168b-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="c168b-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="c168b-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="c168b-131">[in] Указатель на второй идентификатор записи, используемый в сравнении, который представляет запись адресной книги для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c168b-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="c168b-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c168b-132">_ulFlags_</span></span>
  
> <span data-ttu-id="c168b-133">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="c168b-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c168b-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="c168b-134">_lpulResult_</span></span>
  
> <span data-ttu-id="c168b-135">[вышел] Указатель на расположение, содержа которое содержит результаты сравнения.</span><span class="sxs-lookup"><span data-stu-id="c168b-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

