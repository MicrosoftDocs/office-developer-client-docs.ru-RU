---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427817"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="9a652-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="9a652-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="9a652-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a652-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a652-105">Сравнивает два идентификатора записи, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="9a652-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="9a652-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9a652-106">Parameters</span></span>

 <span data-ttu-id="9a652-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="9a652-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="9a652-108">[in] Количество byte в идентификаторе входа, на который указывает параметр _lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="9a652-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="9a652-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="9a652-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="9a652-110">[in] Указатель на первый идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="9a652-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="9a652-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="9a652-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="9a652-112">[in] Количество byte в идентификаторе входа, на который указывает параметр _lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="9a652-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="9a652-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="9a652-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="9a652-114">[in] Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="9a652-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="9a652-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9a652-115">_ulFlags_</span></span>
  
> <span data-ttu-id="9a652-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="9a652-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9a652-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="9a652-117">_lpulResult_</span></span>
  
> <span data-ttu-id="9a652-118">[вышел] Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="9a652-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="9a652-119">TRUE, если два идентификатора записи относятся к одному объекту; в противном случае FALSE.</span><span class="sxs-lookup"><span data-stu-id="9a652-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9a652-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a652-120">Return value</span></span>

<span data-ttu-id="9a652-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a652-121">S_OK</span></span> 
  
> <span data-ttu-id="9a652-122">Сравнение было успешным.</span><span class="sxs-lookup"><span data-stu-id="9a652-122">The comparison was successful.</span></span>
    
<span data-ttu-id="9a652-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9a652-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="9a652-124">Один или оба идентификатора записи, указанные в качестве параметров, не относятся к объектам, возможно, из-за того, что эти объекты в настоящее время недоступны.</span><span class="sxs-lookup"><span data-stu-id="9a652-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a652-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a652-125">Remarks</span></span>

<span data-ttu-id="9a652-126">Метод **IMAPISession::CompareEntryIDs** сравнивает два идентификатора записи, принадлежащих одному поставщику услуг, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="9a652-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="9a652-127">MAPI извлекает часть [MAPIUID](mapiuid.md) из идентификаторов записи, чтобы определить поставщика услуг, ответственного за объекты, а затем вызывает метод **compareEntryIDs** объекта с логотипом для выполнения сравнения.</span><span class="sxs-lookup"><span data-stu-id="9a652-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9a652-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9a652-128">Notes to callers</span></span>

<span data-ttu-id="9a652-129">Метод **CompareEntryIDs** полезен, так как объект может иметь несколько допустимого идентификатора входа.</span><span class="sxs-lookup"><span data-stu-id="9a652-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="9a652-130">Такая ситуация может возникнуть, например, после установки новой версии поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="9a652-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="9a652-131">Если **compareEntryIDs** возвращает ошибку, не принимайте никаких действий в зависимости от результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="9a652-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="9a652-132">Вместо этого примите наиболее консервативный подход.</span><span class="sxs-lookup"><span data-stu-id="9a652-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="9a652-133">**CompareEntryID может** привести к сбой, если, например, один или оба идентификатора записи содержат **недопустимый MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="9a652-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9a652-134">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9a652-134">MFCMAPI reference</span></span>

<span data-ttu-id="9a652-135">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9a652-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9a652-136">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9a652-136">**File**</span></span>|<span data-ttu-id="9a652-137">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9a652-137">**Function**</span></span>|<span data-ttu-id="9a652-138">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9a652-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9a652-139">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="9a652-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="9a652-140">CbaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="9a652-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="9a652-141">MFCMAPI использует **метод IMAPISession::CompareEntryIDs** для сравнения двух входных ИД, которые вводит пользователь.</span><span class="sxs-lookup"><span data-stu-id="9a652-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a652-142">См. также</span><span class="sxs-lookup"><span data-stu-id="9a652-142">See also</span></span>



[<span data-ttu-id="9a652-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="9a652-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="9a652-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a652-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="9a652-145">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9a652-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

