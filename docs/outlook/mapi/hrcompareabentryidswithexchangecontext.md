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
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="c9942-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="c9942-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="c9942-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9942-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9942-105">Безопасно сравнивает две адресные книги **идентификаторами EntryID** в нескольких профилях Exchange.</span><span class="sxs-lookup"><span data-stu-id="c9942-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="c9942-106">Эта функция является функцией замены для [IAddrBook:: метод compareentryids](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="c9942-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9942-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c9942-107">Header file:</span></span>  <br/> |<span data-ttu-id="c9942-108">абхелп. h</span><span class="sxs-lookup"><span data-stu-id="c9942-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="c9942-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c9942-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="c9942-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="c9942-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="c9942-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c9942-111">Called by:</span></span>  <br/> |<span data-ttu-id="c9942-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c9942-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="c9942-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9942-113">Parameters</span></span>

 <span data-ttu-id="c9942-114">_пмсесс_</span><span class="sxs-lookup"><span data-stu-id="c9942-114">_pmsess_</span></span>
  
> <span data-ttu-id="c9942-115">возврата Вошедший в систему **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="c9942-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="c9942-116">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="c9942-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c9942-117">_Пемсмдбуид_</span><span class="sxs-lookup"><span data-stu-id="c9942-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="c9942-118">возврата Указатель на **емсмдбуид** , определяющий службу Exchange, которая содержит поставщика адресных книг Exchange, которую эта функция должна использовать для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="c9942-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="c9942-119">Если входящий идентификатор записи не является идентификатором записи поставщика адресных книг Exchange, этот параметр игнорируется, а вызов функции работает так же, как [IAddrBook::D етаилс](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="c9942-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="c9942-120">Если этот параметр имеет значение NULL или нулевой МАПИУИД, эта функция ведет себя так же, как [IAddrBook::D етаилс](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="c9942-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="c9942-121">_Паддрбук_</span><span class="sxs-lookup"><span data-stu-id="c9942-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="c9942-122">возврата Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="c9942-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="c9942-123">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="c9942-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c9942-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="c9942-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="c9942-125">возврата Число байтов первого идентификатора записи, заданного параметром _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="c9942-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="c9942-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="c9942-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="c9942-127">возврата Указатель на первый идентификатор записи, представляющий запись адресной книги для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c9942-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="c9942-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="c9942-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="c9942-129">возврата Число байтов второго идентификатора записи, заданного параметром _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="c9942-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="c9942-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="c9942-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="c9942-131">возврата Указатель на второй идентификатор записи, используемый в сравнении, представляющем запись адресной книги для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c9942-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="c9942-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9942-132">_ulFlags_</span></span>
  
> <span data-ttu-id="c9942-133">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="c9942-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c9942-134">_Лпулресулт_</span><span class="sxs-lookup"><span data-stu-id="c9942-134">_lpulResult_</span></span>
  
> <span data-ttu-id="c9942-135">вышли Указатель на расположение, в котором содержатся результаты сравнения.</span><span class="sxs-lookup"><span data-stu-id="c9942-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

