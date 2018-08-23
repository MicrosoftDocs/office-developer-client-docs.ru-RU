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
ms.openlocfilehash: 57b8438d655b3bc5b708fd7ed6734554a3a23ac4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585992"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="1b6dc-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="1b6dc-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="1b6dc-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b6dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b6dc-105">Сравнение двух сообщений идентификаторы хранилища записей для определения, является ли они ссылаются на тот же объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1b6dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b6dc-106">Parameters</span></span>

 <span data-ttu-id="1b6dc-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1b6dc-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="1b6dc-108">[in] Указывает размер в байтах, идентификатор записи с помощью параметра _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="1b6dc-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="1b6dc-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="1b6dc-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="1b6dc-110">[in] Указатель на первый идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1b6dc-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1b6dc-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="1b6dc-112">[in] Указывает размер в байтах, идентификатор записи с помощью параметра _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="1b6dc-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="1b6dc-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="1b6dc-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="1b6dc-114">[in] Указатель на второй идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="1b6dc-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b6dc-115">_ulFlags_</span></span>
  
> <span data-ttu-id="1b6dc-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1b6dc-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="1b6dc-117">_lpulResult_</span></span>
  
> <span data-ttu-id="1b6dc-118">[out] Указатель на возвращаемый результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="1b6dc-119">Значение TRUE, если идентификаторы двух записей ссылаются на тот же объект; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b6dc-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1b6dc-120">Return value</span></span>

<span data-ttu-id="1b6dc-121">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1b6dc-121">S_OK</span></span> 
  
> <span data-ttu-id="1b6dc-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b6dc-123">���������</span><span class="sxs-lookup"><span data-stu-id="1b6dc-123">Remarks</span></span>

<span data-ttu-id="1b6dc-124">MAPI вызывает метод **IMSProvider::CompareStoreIDs** при обработке вызова метода [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="1b6dc-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="1b6dc-125">На этом этапе вызывает **CompareStoreIDs** для определения, какие раздела профиля при их наличии, связанного с хранилищем сообщений их открытием.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="1b6dc-126">Вызов **CompareStoreIDs** может быть выполнен, когда нет хранилищ сообщений открыты для конкретного хранилища поставщика.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="1b6dc-127">В дополнение к этому MAPI также вызывает **CompareStoreIDs** при обработке вызова поставщика хранилища в метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="1b6dc-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="1b6dc-128">Идентификаторы записей, по сравнению с **CompareStoreIDs** являются оба для текущего хранения поставщика библиотеки динамической компоновки (DLL) и являются оба идентификаторы развернуть хранилища записей.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="1b6dc-129">Дополнительные сведения о перенос идентификаторы хранилища записей можно [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span><span class="sxs-lookup"><span data-stu-id="1b6dc-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="1b6dc-130">Сравнение идентификаторы записей полезен, так как объект может иметь несколько идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="1b6dc-131">Это может произойти, например, после установки новой версии поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b6dc-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b6dc-132">См. также</span><span class="sxs-lookup"><span data-stu-id="1b6dc-132">See also</span></span>



[<span data-ttu-id="1b6dc-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="1b6dc-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="1b6dc-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="1b6dc-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="1b6dc-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="1b6dc-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="1b6dc-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b6dc-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

