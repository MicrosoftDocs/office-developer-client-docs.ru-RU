---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410135"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="11265-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="11265-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="11265-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11265-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11265-105">Сравнивает два идентификатора записей, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="11265-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="11265-106">MAPI обращается к поставщику услуг только в том случае, если уникальные идентификаторы (UID) в обоих идентификаторах записей, которые необходимо сравнить, обрабатываются этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="11265-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="11265-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="11265-107">Parameters</span></span>

 <span data-ttu-id="11265-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="11265-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="11265-109">[in] Размер идентификатора записи в вайтах, на который указывает  параметр _lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="11265-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="11265-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="11265-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="11265-111">[in] Указатель на идентификатор первой записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="11265-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="11265-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="11265-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="11265-113">[in] Размер идентификатора записи в вайтах, на который указывает  параметр _lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="11265-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="11265-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="11265-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="11265-115">[in] Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="11265-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="11265-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="11265-116">_ulFlags_</span></span>
  
> <span data-ttu-id="11265-117">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="11265-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="11265-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="11265-118">_lpulResult_</span></span>
  
> <span data-ttu-id="11265-119">[out] Указатель на возвращенный результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="11265-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="11265-120">TRUE, если два идентификатора записей ссылаются на один и тот же объект; в противном случае false.</span><span class="sxs-lookup"><span data-stu-id="11265-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11265-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11265-121">Return value</span></span>

<span data-ttu-id="11265-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="11265-122">S_OK</span></span> 
  
> <span data-ttu-id="11265-123">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="11265-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11265-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="11265-124">Remarks</span></span>

<span data-ttu-id="11265-125">Поставщики store сообщений реализуют метод **IMSLogon::CompareEntryIDs** для сравнения двух идентификаторов записей для заданной записи в хранилище сообщений, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="11265-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="11265-126">Если два идентификатора записей ссылаются на один и тот же объект, **CompareEntryIDs** задает для параметра  _lpulResult_ true; Если они ссылаются на разные объекты, **CompareEntryIDs** устанавливает  _для lpulResult_ false.</span><span class="sxs-lookup"><span data-stu-id="11265-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="11265-127">**CompareEntryIDs полезен,** так как объект может иметь несколько допустимых идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="11265-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="11265-128">Это может произойти, например, после установки новой версии поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="11265-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11265-129">См. также</span><span class="sxs-lookup"><span data-stu-id="11265-129">See also</span></span>



[<span data-ttu-id="11265-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11265-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

