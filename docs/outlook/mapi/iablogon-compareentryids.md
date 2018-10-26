---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b161c8c0da78b5ca872b87cad9a297169426d4cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565006"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="5b23d-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="5b23d-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="5b23d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b23d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b23d-105">Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="5b23d-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
);
```

## <a name="parameters"></a><span data-ttu-id="5b23d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b23d-106">Parameters</span></span>

 <span data-ttu-id="5b23d-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="5b23d-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="5b23d-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="5b23d-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="5b23d-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="5b23d-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="5b23d-110">[in] Указатель на первый идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="5b23d-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="5b23d-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="5b23d-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="5b23d-112">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="5b23d-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="5b23d-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="5b23d-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="5b23d-114">[in] Указатель на второй идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="5b23d-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="5b23d-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b23d-115">_ulFlags_</span></span>
  
> <span data-ttu-id="5b23d-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="5b23d-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5b23d-117">_lpulRet_</span><span class="sxs-lookup"><span data-stu-id="5b23d-117">_lpulRet_</span></span>
  
> <span data-ttu-id="5b23d-118">[out] Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="5b23d-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="5b23d-119">Значение TRUE, чтобы указать, что идентификаторы двух записей ссылаются на тот же объект; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="5b23d-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b23d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b23d-120">Return value</span></span>

<span data-ttu-id="5b23d-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b23d-121">S_OK</span></span> 
  
> <span data-ttu-id="5b23d-122">Идентификаторы записей было успешно выполнено.</span><span class="sxs-lookup"><span data-stu-id="5b23d-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="5b23d-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5b23d-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="5b23d-124">Одно или оба идентификаторы записей не принадлежат к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="5b23d-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b23d-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="5b23d-125">Remarks</span></span>

<span data-ttu-id="5b23d-126">Метод **CompareEntryIDs** для сравнения двух идентификаторы записей для определения, является ли они ссылаются на тот же объект, реализуемые поставщиками адресных книг.</span><span class="sxs-lookup"><span data-stu-id="5b23d-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="5b23d-127">**CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей; такой ситуации может произойти, например, при сравнении краткосрочных идентификатор записи с долгосрочного идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="5b23d-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="5b23d-128">Дополнительные сведения о том, как создавать идентификаторы записей можно [Идентификаторы MAPI записей](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="5b23d-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5b23d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5b23d-129">See also</span></span>



[<span data-ttu-id="5b23d-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b23d-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

