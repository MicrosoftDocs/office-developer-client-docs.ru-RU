---
title: Имслогонкомпаринтридс
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348729"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="60254-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="60254-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="60254-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60254-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60254-105">Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="60254-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="60254-106">MAPI указывает этот вызов поставщику услуг, только если уникальные идентификаторы (UID) в обоих идентификаторах записей будут обрабатываться этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="60254-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="60254-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="60254-107">Parameters</span></span>

 <span data-ttu-id="60254-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="60254-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="60254-109">возврата Размер (в байтах) идентификатора записи, на который указывает параметр _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="60254-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="60254-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="60254-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="60254-111">возврата Указатель на первый идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="60254-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="60254-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="60254-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="60254-113">возврата Размер (в байтах) идентификатора записи, на который указывает параметр _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="60254-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="60254-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="60254-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="60254-115">возврата Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="60254-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="60254-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="60254-116">_ulFlags_</span></span>
  
> <span data-ttu-id="60254-117">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="60254-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="60254-118">_Лпулресулт_</span><span class="sxs-lookup"><span data-stu-id="60254-118">_lpulResult_</span></span>
  
> <span data-ttu-id="60254-119">вышли Указатель на возвращаемый результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="60254-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="60254-120">ЗНАЧЕНИЕ TRUE, если два идентификатора записи ссылаются на один объект; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="60254-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="60254-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60254-121">Return value</span></span>

<span data-ttu-id="60254-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="60254-122">S_OK</span></span> 
  
> <span data-ttu-id="60254-123">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="60254-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60254-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="60254-124">Remarks</span></span>

<span data-ttu-id="60254-125">Поставщики хранилища сообщений реализуют метод **имслогон:: метод compareentryids** для сравнения двух идентификаторов записей для заданной записи в хранилище сообщений, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="60254-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="60254-126">Если два идентификатора записи ссылаются на один и тот же объект, **метод compareentryids** устанавливает для параметра _лпулресулт_ значение true; Если они ссылаются на различные объекты, **метод compareentryids** устанавливает для _лпулресулт_ значение false.</span><span class="sxs-lookup"><span data-stu-id="60254-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="60254-127">**Метод compareentryids** полезен, так как объект может иметь несколько допустимых идентификаторов записи.</span><span class="sxs-lookup"><span data-stu-id="60254-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="60254-128">Это может произойти, например, после установки новой версии поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="60254-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60254-129">См. также</span><span class="sxs-lookup"><span data-stu-id="60254-129">See also</span></span>



[<span data-ttu-id="60254-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="60254-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

