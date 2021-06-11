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
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="0ddcf-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="0ddcf-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="0ddcf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ddcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ddcf-105">Сравнивает два идентификатора входа в хранилище сообщений, чтобы определить, относятся ли они к одному объекту магазина.</span><span class="sxs-lookup"><span data-stu-id="0ddcf-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0ddcf-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0ddcf-106">Parameters</span></span>

 <span data-ttu-id="0ddcf-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="0ddcf-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="0ddcf-108">[in] Размер в bytes идентификатора записи, на который указывает параметр _lpEntryID1._ </span><span class="sxs-lookup"><span data-stu-id="0ddcf-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="0ddcf-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="0ddcf-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="0ddcf-110">[in] Указатель на первый идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="0ddcf-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="0ddcf-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="0ddcf-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="0ddcf-112">[in] Размер в bytes идентификатора записи, на который указывает параметр _lpEntryID2._ </span><span class="sxs-lookup"><span data-stu-id="0ddcf-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="0ddcf-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="0ddcf-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="0ddcf-114">[in] Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="0ddcf-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="0ddcf-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0ddcf-115">_ulFlags_</span></span>
  
> <span data-ttu-id="0ddcf-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="0ddcf-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0ddcf-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="0ddcf-117">_lpulResult_</span></span>
  
> <span data-ttu-id="0ddcf-118">[вышел] Указатель на возвращенный результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="0ddcf-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="0ddcf-119">TRUE, если два идентификатора записи относятся к одному объекту; в противном случае FALSE.</span><span class="sxs-lookup"><span data-stu-id="0ddcf-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0ddcf-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ddcf-120">Return value</span></span>

<span data-ttu-id="0ddcf-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ddcf-121">S_OK</span></span> 
  
> <span data-ttu-id="0ddcf-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0ddcf-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ddcf-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="0ddcf-123">Remarks</span></span>

<span data-ttu-id="0ddcf-124">MAPI вызывает **метод IMSProvider::CompareStoreIDs** при обработке вызова метода [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md)</span><span class="sxs-lookup"><span data-stu-id="0ddcf-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="0ddcf-125">В данный момент для определения того, какой раздел профиля связан с открываемой хранилищем сообщений, **вызвано compareStoreIDs.**</span><span class="sxs-lookup"><span data-stu-id="0ddcf-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="0ddcf-126">Вызов **CompareStoreIDs можно** сделать, если для конкретного поставщика магазинов не открыты магазины сообщений.</span><span class="sxs-lookup"><span data-stu-id="0ddcf-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="0ddcf-127">Кроме того, MAPI также вызывает **CompareStoreIDs** при обработке вызова поставщика магазина в [метод IMAPISupport::OpenProfileSection.](imapisupport-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="0ddcf-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="0ddcf-128">Идентификаторы записей, сравниваемые **с CompareStoreID,** являются как для библиотеки динамических ссылок текущего поставщика хранения (DLL), так и для идентификаторов входа в хранилище.</span><span class="sxs-lookup"><span data-stu-id="0ddcf-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="0ddcf-129">Дополнительные сведения о идентификаторах входа в магазин для упаковки см. в [книге IMAPISupport::WrapStoreEntryID.](imapisupport-wrapstoreentryid.md)</span><span class="sxs-lookup"><span data-stu-id="0ddcf-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="0ddcf-130">Сравнение идентификаторов записей полезно, так как объект может иметь несколько допустимых идентификаторов записи.</span><span class="sxs-lookup"><span data-stu-id="0ddcf-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="0ddcf-131">Это может произойти, например, после установки новой версии поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="0ddcf-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0ddcf-132">См. также</span><span class="sxs-lookup"><span data-stu-id="0ddcf-132">See also</span></span>



[<span data-ttu-id="0ddcf-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="0ddcf-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="0ddcf-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="0ddcf-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="0ddcf-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="0ddcf-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="0ddcf-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ddcf-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

