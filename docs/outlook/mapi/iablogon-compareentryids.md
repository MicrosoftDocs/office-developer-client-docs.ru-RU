---
title: иаблогонкомпаринтридс
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
ms.openlocfilehash: 48ddb5a7c4e013c03138b08d9dadcdc0991faeec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438374"
---
# <a name="iablogoncompareentryids"></a><span data-ttu-id="e6250-103">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="e6250-103">IABLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="e6250-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6250-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6250-105">Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="e6250-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="e6250-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6250-106">Parameters</span></span>

 <span data-ttu-id="e6250-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="e6250-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="e6250-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="e6250-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="e6250-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="e6250-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="e6250-110">возврата Указатель на первый идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="e6250-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="e6250-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="e6250-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="e6250-112">возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="e6250-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="e6250-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="e6250-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="e6250-114">возврата Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="e6250-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="e6250-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6250-115">_ulFlags_</span></span>
  
> <span data-ttu-id="e6250-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="e6250-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e6250-117">_лпулрет_</span><span class="sxs-lookup"><span data-stu-id="e6250-117">_lpulRet_</span></span>
  
> <span data-ttu-id="e6250-118">вышли Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="e6250-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="e6250-119">Значение TRUE, чтобы указать, что два идентификатора записи ссылаются на один и тот же объект; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="e6250-119">TRUE to indicate that the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6250-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6250-120">Return value</span></span>

<span data-ttu-id="e6250-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6250-121">S_OK</span></span> 
  
> <span data-ttu-id="e6250-122">Идентификаторы записей были успешно сравнены.</span><span class="sxs-lookup"><span data-stu-id="e6250-122">The entry identifiers were successfully compared.</span></span>
    
<span data-ttu-id="e6250-123">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e6250-123">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="e6250-124">Один или оба идентификатора записи не принадлежат поставщику адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e6250-124">One or both of the entry identifiers do not belong to the address book provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6250-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="e6250-125">Remarks</span></span>

<span data-ttu-id="e6250-126">Поставщики адресных книг реализуют метод **метод compareentryids** для сравнения двух идентификаторов записей, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="e6250-126">Address book providers implement the **CompareEntryIDs** method to compare two entry identifiers to determine whether they refer to the same object.</span></span> 
  
 <span data-ttu-id="e6250-127">**Метод compareentryids** полезен, так как объект может иметь несколько допустимых идентификаторов записей; Такая ситуация может возникнуть, например, при сравнении краткосрочного идентификатора записи с длинным идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="e6250-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier; such a situation can occur, for example, when you compare a short-term entry identifier with a long-term entry identifier.</span></span> 
  
<span data-ttu-id="e6250-128">Дополнительные сведения о создании идентификаторов записей можно узнать в статье [идентификаторы записей MAPI](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="e6250-128">For more information about how to create entry identifiers, see [MAPI Entry Identifiers](mapi-entry-identifiers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e6250-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e6250-129">See also</span></span>



[<span data-ttu-id="e6250-130">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6250-130">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

