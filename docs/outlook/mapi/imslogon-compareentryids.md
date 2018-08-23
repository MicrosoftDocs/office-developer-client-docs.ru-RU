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
ms.openlocfilehash: c5b2d7db745cc270c0be7ee2184e86c6a4f97aad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594301"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="8149a-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="8149a-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="8149a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8149a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8149a-105">Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="8149a-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="8149a-106">MAPI ссылается этот вызов к поставщику услуг только в том случае, если уникальных идентификаторов (UID) в обоих идентификаторы записей для сравнения обрабатываются этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="8149a-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="8149a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8149a-107">Parameters</span></span>

 <span data-ttu-id="8149a-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="8149a-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="8149a-109">[in] Указывает размер в байтах, идентификатор записи с помощью параметра _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="8149a-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="8149a-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="8149a-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="8149a-111">[in] Указатель на первый идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8149a-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="8149a-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="8149a-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="8149a-113">[in] Указывает размер в байтах, идентификатор записи с помощью параметра _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="8149a-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="8149a-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="8149a-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="8149a-115">[in] Указатель на второй идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8149a-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="8149a-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8149a-116">_ulFlags_</span></span>
  
> <span data-ttu-id="8149a-117">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="8149a-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8149a-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="8149a-118">_lpulResult_</span></span>
  
> <span data-ttu-id="8149a-119">[out] Указатель на возвращаемый результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="8149a-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="8149a-120">Значение TRUE, если идентификаторы двух записей ссылаются на тот же объект; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="8149a-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8149a-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="8149a-121">Return value</span></span>

<span data-ttu-id="8149a-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="8149a-122">S_OK</span></span> 
  
> <span data-ttu-id="8149a-123">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="8149a-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8149a-124">���������</span><span class="sxs-lookup"><span data-stu-id="8149a-124">Remarks</span></span>

<span data-ttu-id="8149a-125">Поставщики хранилища сообщений реализуйте метод **IMSLogon::CompareEntryIDs** для сравнения двух идентификаторов запись соответствующей записи в хранилище сообщений, чтобы определить, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="8149a-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="8149a-126">Если идентификаторы двух записей ссылаются на тот же объект, **CompareEntryIDs** параметру _lpulResult_ присваивается значение TRUE; Если они ссылаются на разных объектов, **CompareEntryIDs** задает _lpulResult_ значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="8149a-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="8149a-127">**CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="8149a-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="8149a-128">Это может произойти, например, после установки новой версии поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8149a-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8149a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="8149a-129">See also</span></span>



[<span data-ttu-id="8149a-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8149a-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

