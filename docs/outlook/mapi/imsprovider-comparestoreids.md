---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431710"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="d4eea-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="d4eea-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="d4eea-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4eea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4eea-105">Сравнивает два идентификатора записей в хранилище сообщений, чтобы определить, относятся ли они к одному объекту store.</span><span class="sxs-lookup"><span data-stu-id="d4eea-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
```cpp
HRESULT CompareStoreIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="d4eea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4eea-106">Parameters</span></span>

 <span data-ttu-id="d4eea-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="d4eea-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="d4eea-108">[in] Размер идентификатора записи в вайтах, на который указывает  параметр _lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="d4eea-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="d4eea-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="d4eea-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="d4eea-110">[in] Указатель на идентификатор первой записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="d4eea-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="d4eea-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="d4eea-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="d4eea-112">[in] Размер идентификатора записи в вайтах, на который указывает  параметр _lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="d4eea-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="d4eea-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="d4eea-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="d4eea-114">[in] Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="d4eea-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="d4eea-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d4eea-115">_ulFlags_</span></span>
  
> <span data-ttu-id="d4eea-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="d4eea-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d4eea-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="d4eea-117">_lpulResult_</span></span>
  
> <span data-ttu-id="d4eea-118">[out] Указатель на возвращенный результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="d4eea-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="d4eea-119">TRUE, если два идентификатора записей ссылаются на один и тот же объект; в противном случае false.</span><span class="sxs-lookup"><span data-stu-id="d4eea-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d4eea-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4eea-120">Return value</span></span>

<span data-ttu-id="d4eea-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="d4eea-121">S_OK</span></span> 
  
> <span data-ttu-id="d4eea-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d4eea-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d4eea-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="d4eea-123">Remarks</span></span>

<span data-ttu-id="d4eea-124">MAPI вызывает метод **IMSProvider::CompareStoreIDs** при обработке вызова метода [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md)</span><span class="sxs-lookup"><span data-stu-id="d4eea-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="d4eea-125">В этот момент с помощью **compareStoreIDs** определяется, какой раздел профиля (если он имеется) связан с открываемого хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="d4eea-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="d4eea-126">Вызов **CompareStoreIDs** можно сделать, если для определенного поставщика хранилища не открыты хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d4eea-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="d4eea-127">Кроме того, MAPI также вызывает **CompareStoreIDs** при обработке вызова поставщика магазина к методу [IMAPISupport::OpenProfileSection.](imapisupport-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="d4eea-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="d4eea-128">Идентификаторы записей, сравниваемые **compareStoreIDs,** являются как для библиотеки динамической ссылки текущего поставщика (DLL) текущего поставщика, так и для неподтверченных идентификаторов записей в хранилище.</span><span class="sxs-lookup"><span data-stu-id="d4eea-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="d4eea-129">Дополнительные сведения об переносе идентификаторов записей в хранилище см. в документе [IMAPISupport::WrapStoreEntryID.](imapisupport-wrapstoreentryid.md)</span><span class="sxs-lookup"><span data-stu-id="d4eea-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="d4eea-130">Сравнение идентификаторов записей полезно, так как объект может иметь несколько допустимых идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="d4eea-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="d4eea-131">Это может произойти, например, после установки новой версии поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="d4eea-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4eea-132">См. также</span><span class="sxs-lookup"><span data-stu-id="d4eea-132">See also</span></span>



[<span data-ttu-id="d4eea-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="d4eea-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="d4eea-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="d4eea-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="d4eea-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="d4eea-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="d4eea-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4eea-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

