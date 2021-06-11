---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424254"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="2d885-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="2d885-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="2d885-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d885-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d885-105">Сравнивает два идентификатора записи, чтобы определить, относятся ли они к одной и той же записи в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="2d885-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="2d885-106">MAPI передает этот вызов поставщику услуг только в том случае, если уникальные идентификаторы (UID) в обоих идентификаторах записи, которые необходимо сравнить, обрабатываются этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="2d885-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2d885-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="2d885-107">Parameters</span></span>

 <span data-ttu-id="2d885-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2d885-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="2d885-109">[in] Количество byte в идентификаторе записи, на который указывает  параметр _lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="2d885-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="2d885-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="2d885-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="2d885-111">[in] Указатель на первый идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="2d885-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2d885-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2d885-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="2d885-113">[in] Количество byte в идентификаторе входа, на который указывает параметр  _lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="2d885-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="2d885-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="2d885-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="2d885-115">[in] Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="2d885-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="2d885-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2d885-116">_ulFlags_</span></span>
  
> <span data-ttu-id="2d885-117">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="2d885-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2d885-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="2d885-118">_lpulResult_</span></span>
  
> <span data-ttu-id="2d885-119">[вышел] Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="2d885-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="2d885-120">TRUE, если два идентификатора записи относятся к одному объекту; в противном случае FALSE.</span><span class="sxs-lookup"><span data-stu-id="2d885-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2d885-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d885-121">Return value</span></span>

<span data-ttu-id="2d885-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d885-122">S_OK</span></span> 
  
> <span data-ttu-id="2d885-123">Сравнение было успешным.</span><span class="sxs-lookup"><span data-stu-id="2d885-123">The comparison was successful.</span></span>
    
<span data-ttu-id="2d885-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2d885-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="2d885-125">Один или оба идентификатора записи, указанные в качестве параметров, не относятся к объектам, возможно, из-за того, что соответствующие объекты в настоящее время не были отперты и недоступны.</span><span class="sxs-lookup"><span data-stu-id="2d885-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d885-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="2d885-126">Remarks</span></span>

<span data-ttu-id="2d885-127">Метод **IMsgStore::CompareEntryIDs** сравнивает два идентификатора записей, принадлежащих магазину сообщений, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="2d885-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2d885-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2d885-128">Notes to callers</span></span>

 <span data-ttu-id="2d885-129">**CompareEntryIDs** полезен, так как объект может иметь несколько допустимого идентификатора входа (например, после установки новой версии поставщика магазина сообщений).</span><span class="sxs-lookup"><span data-stu-id="2d885-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="2d885-130">Если **compareEntryIDs** возвращает ошибку, не принимайте никаких действий в зависимости от результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="2d885-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="2d885-131">Вместо этого примите наиболее консервативный подход.</span><span class="sxs-lookup"><span data-stu-id="2d885-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="2d885-132">**CompareEntryIDs может** привести к сбой, если, например, один или оба идентификатора записи содержат **недопустимый MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="2d885-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2d885-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2d885-133">MFCMAPI reference</span></span>

<span data-ttu-id="2d885-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="2d885-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2d885-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="2d885-135">**File**</span></span>|<span data-ttu-id="2d885-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="2d885-136">**Function**</span></span>|<span data-ttu-id="2d885-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="2d885-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2d885-138">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="2d885-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="2d885-139">CBaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="2d885-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="2d885-140">MFCMAPI использует **метод IMsgStore::CompareEntryIDs** для сравнения ID-записей.</span><span class="sxs-lookup"><span data-stu-id="2d885-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d885-141">См. также</span><span class="sxs-lookup"><span data-stu-id="2d885-141">See also</span></span>



[<span data-ttu-id="2d885-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="2d885-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="2d885-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2d885-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="2d885-144">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="2d885-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

