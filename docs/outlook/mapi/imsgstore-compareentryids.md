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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: a1c5cdc67bc64f20dd8ba0a5e8682c5e2f97294f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809374"
---
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="8e79c-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="8e79c-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="8e79c-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e79c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e79c-105">Сравнение двух идентификаторы записей для определения, является ли они ссылаются на той же операции в банке сообщений.</span><span class="sxs-lookup"><span data-stu-id="8e79c-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="8e79c-106">MAPI передает этот вызов к поставщику услуг только в том случае, если уникальных идентификаторов (UID) в обоих идентификаторы записей для сравнения обрабатываются этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="8e79c-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="8e79c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8e79c-107">Parameters</span></span>

 <span data-ttu-id="8e79c-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="8e79c-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="8e79c-109">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="8e79c-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="8e79c-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="8e79c-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="8e79c-111">[in] Указатель на первый идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8e79c-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="8e79c-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="8e79c-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="8e79c-113">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="8e79c-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="8e79c-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="8e79c-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="8e79c-115">[in] Указатель на второй идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8e79c-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="8e79c-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e79c-116">_ulFlags_</span></span>
  
> <span data-ttu-id="8e79c-117">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="8e79c-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8e79c-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="8e79c-118">_lpulResult_</span></span>
  
> <span data-ttu-id="8e79c-119">[out] Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="8e79c-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="8e79c-120">Значение TRUE, если идентификаторы двух записей ссылаются на тот же объект; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="8e79c-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8e79c-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="8e79c-121">Return value</span></span>

<span data-ttu-id="8e79c-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="8e79c-122">S_OK</span></span> 
  
> <span data-ttu-id="8e79c-123">Сравнение успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="8e79c-123">The comparison was successful.</span></span>
    
<span data-ttu-id="8e79c-124">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8e79c-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="8e79c-125">Одна или обе идентификаторы записей, указанный в качестве параметров относится к объектам, возможно из-за соответствующими объектами неоткрытый и недоступен в представление.</span><span class="sxs-lookup"><span data-stu-id="8e79c-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e79c-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="8e79c-126">Remarks</span></span>

<span data-ttu-id="8e79c-127">Метод **IMsgStore::CompareEntryIDs** сравнивает два идентификаторы записей, относящихся к хранилище сообщений, чтобы определить, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="8e79c-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8e79c-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8e79c-128">Notes to callers</span></span>

 <span data-ttu-id="8e79c-129">**CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей (например, после установки новой версии поставщика хранилища сообщений).</span><span class="sxs-lookup"><span data-stu-id="8e79c-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="8e79c-130">Если **CompareEntryIDs** возвращает ошибку, не имеет каких-либо действий на основании результатов сравнения.</span><span class="sxs-lookup"><span data-stu-id="8e79c-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="8e79c-131">Вместо этого можно использовать самый высокий подход невозможно.</span><span class="sxs-lookup"><span data-stu-id="8e79c-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="8e79c-132">**CompareEntryIDs** может оказаться неудачным, если, например один или оба идентификаторы записей содержит недопустимый **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="8e79c-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8e79c-133">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="8e79c-133">MFCMAPI reference</span></span>

<span data-ttu-id="8e79c-134">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="8e79c-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8e79c-135">**����**</span><span class="sxs-lookup"><span data-stu-id="8e79c-135">**File**</span></span>|<span data-ttu-id="8e79c-136">**�������**</span><span class="sxs-lookup"><span data-stu-id="8e79c-136">**Function**</span></span>|<span data-ttu-id="8e79c-137">**�����������**</span><span class="sxs-lookup"><span data-stu-id="8e79c-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8e79c-138">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="8e79c-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="8e79c-139">CBaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="8e79c-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="8e79c-140">Mfcmapi (en) использует метод **IMsgStore::CompareEntryIDs** для сравнения запись идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="8e79c-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e79c-141">См. также</span><span class="sxs-lookup"><span data-stu-id="8e79c-141">See also</span></span>



[<span data-ttu-id="8e79c-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8e79c-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8e79c-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8e79c-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="8e79c-144">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="8e79c-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

