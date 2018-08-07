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
ms.openlocfilehash: 730c24a179cc6aaf8dc2068199ffc206d30156b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808652"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="d961f-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d961f-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="d961f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d961f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d961f-105">Сравнивает книги два адреса **entryIDs** безопасно в профиле нескольких Exchange.</span><span class="sxs-lookup"><span data-stu-id="d961f-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="d961f-106">Эта функция — это функция замены для [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="d961f-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d961f-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d961f-107">Header file:</span></span>  <br/> |<span data-ttu-id="d961f-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="d961f-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d961f-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="d961f-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d961f-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d961f-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d961f-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="d961f-111">Called by:</span></span>  <br/> |<span data-ttu-id="d961f-112">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="d961f-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d961f-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="d961f-113">Parameters</span></span>

 <span data-ttu-id="d961f-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="d961f-114">_pmsess_</span></span>
  
> <span data-ttu-id="d961f-115">[in] Система на **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="d961f-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="d961f-116">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="d961f-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d961f-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="d961f-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="d961f-118">[in] Указатель на **emsmdbUID** , который определяет службу Exchange, которая содержит поставщик адресной книги Exchange, который следует использовать эту функцию для отображения сведений на идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d961f-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="d961f-119">Если входящий идентификатор записи не идентификатор записи Exchange поставщик адресной книги, этот параметр игнорируется и вызов функции действует как [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="d961f-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="d961f-120">Если этот параметр имеет значение NULL или ноль MAPIUID, эта функция действует как [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="d961f-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="d961f-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="d961f-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="d961f-122">[in] В адресной книге используется для открытия идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d961f-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="d961f-123">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="d961f-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d961f-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="d961f-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="d961f-125">[in] Количество байтов первой записи идентификатор, указанный в параметре _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="d961f-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="d961f-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="d961f-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="d961f-127">[in] Указатель на первый идентификатор записи, который представляет записи адресной книги для сравнения.</span><span class="sxs-lookup"><span data-stu-id="d961f-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="d961f-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="d961f-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="d961f-129">[in] Количество байтов второй идентификатор записи, указанные с помощью параметра _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="d961f-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="d961f-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="d961f-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="d961f-131">[in] Указатель на втором запись идентификатор, который используется для сравнения, представляющий запись адресной книги для сравнения.</span><span class="sxs-lookup"><span data-stu-id="d961f-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="d961f-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d961f-132">_ulFlags_</span></span>
  
> <span data-ttu-id="d961f-133">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="d961f-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d961f-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="d961f-134">_lpulResult_</span></span>
  
> <span data-ttu-id="d961f-135">[out] Указатель на папку, где содержатся результаты сравнения.</span><span class="sxs-lookup"><span data-stu-id="d961f-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

