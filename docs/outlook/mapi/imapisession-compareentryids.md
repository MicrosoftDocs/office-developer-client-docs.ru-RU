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
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="f1b1f-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="f1b1f-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="f1b1f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1b1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1b1f-105">Сравнивает два идентификатора записей, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="f1b1f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1b1f-106">Parameters</span></span>

 <span data-ttu-id="f1b1f-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="f1b1f-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="f1b1f-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="f1b1f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="f1b1f-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="f1b1f-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="f1b1f-110">[in] Указатель на идентификатор первой записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="f1b1f-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="f1b1f-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="f1b1f-112">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="f1b1f-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="f1b1f-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="f1b1f-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="f1b1f-114">[in] Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="f1b1f-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f1b1f-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f1b1f-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f1b1f-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="f1b1f-117">_lpulResult_</span></span>
  
> <span data-ttu-id="f1b1f-118">[out] Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="f1b1f-119">TRUE, если два идентификатора записей ссылаются на один и тот же объект; в противном случае false.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f1b1f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1b1f-120">Return value</span></span>

<span data-ttu-id="f1b1f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1b1f-121">S_OK</span></span> 
  
> <span data-ttu-id="f1b1f-122">Сравнение было успешным.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-122">The comparison was successful.</span></span>
    
<span data-ttu-id="f1b1f-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f1b1f-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="f1b1f-124">Один или оба идентификатора записей, указанных в качестве параметров, не ссылаются на объекты, возможно, из-за того, что эти объекты в настоящее время не работают и недоступны.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1b1f-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1b1f-125">Remarks</span></span>

<span data-ttu-id="f1b1f-126">Метод **IMAPISession::CompareEntryIDs** сравнивает два идентификатора записей, принадлежащих одному поставщику услуг, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="f1b1f-127">MAPI извлекает часть [MAPIUID](mapiuid.md) из идентификаторов записей, чтобы определить поставщика услуг, ответственного за объекты, а затем вызывает метод **CompareEntryIDs** объекта входа для выполнения сравнения.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f1b1f-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f1b1f-128">Notes to callers</span></span>

<span data-ttu-id="f1b1f-129">Метод **CompareEntryIDs полезен,** так как объект может иметь несколько допустимого идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="f1b1f-130">Это может произойти, например, после установки новой версии поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="f1b1f-131">Если **CompareEntryIDs** возвращает ошибку, не принимайте никаких действий на основе результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="f1b1f-132">Вместо этого вы можете использовать наиболее емкий подход.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="f1b1f-133">**CompareEntryIDs** может привести к сбой, если, например, один или оба идентификатора записи содержат **недопустимый MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f1b1f-134">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f1b1f-134">MFCMAPI reference</span></span>

<span data-ttu-id="f1b1f-135">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f1b1f-136">**Файл**</span><span class="sxs-lookup"><span data-stu-id="f1b1f-136">**File**</span></span>|<span data-ttu-id="f1b1f-137">**Функция**</span><span class="sxs-lookup"><span data-stu-id="f1b1f-137">**Function**</span></span>|<span data-ttu-id="f1b1f-138">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f1b1f-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f1b1f-139">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="f1b1f-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="f1b1f-140">CbaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="f1b1f-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="f1b1f-141">MFCMAPI использует метод **IMAPISession::CompareEntryIDs** для сравнения двух входных данных, которые вводит пользователь.</span><span class="sxs-lookup"><span data-stu-id="f1b1f-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1b1f-142">См. также</span><span class="sxs-lookup"><span data-stu-id="f1b1f-142">See also</span></span>



[<span data-ttu-id="f1b1f-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="f1b1f-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="f1b1f-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1b1f-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="f1b1f-145">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f1b1f-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

