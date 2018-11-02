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
ms.openlocfilehash: 745c1b10cbbb24389cace7911d7c5fd37fe09472
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586853"
---
# <a name="imapisessioncompareentryids"></a><span data-ttu-id="a40d3-103">IMAPISession::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a40d3-103">IMAPISession::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="a40d3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a40d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a40d3-105">Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="a40d3-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="a40d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a40d3-106">Parameters</span></span>

 <span data-ttu-id="a40d3-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="a40d3-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="a40d3-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="a40d3-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="a40d3-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="a40d3-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="a40d3-110">[in] Указатель на первый идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="a40d3-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="a40d3-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="a40d3-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="a40d3-112">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="a40d3-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="a40d3-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="a40d3-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="a40d3-114">[in] Указатель на второй идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="a40d3-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="a40d3-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a40d3-115">_ulFlags_</span></span>
  
> <span data-ttu-id="a40d3-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="a40d3-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a40d3-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="a40d3-117">_lpulResult_</span></span>
  
> <span data-ttu-id="a40d3-118">[out] Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="a40d3-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="a40d3-119">Значение TRUE, если идентификаторы двух записей ссылаются на тот же объект; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="a40d3-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a40d3-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a40d3-120">Return value</span></span>

<span data-ttu-id="a40d3-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="a40d3-121">S_OK</span></span> 
  
> <span data-ttu-id="a40d3-122">Сравнение успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="a40d3-122">The comparison was successful.</span></span>
    
<span data-ttu-id="a40d3-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a40d3-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="a40d3-124">Одно или оба идентификаторы записей, указанный в качестве параметров относится к объектам, возможно из-за этих объектов в настоящее время неоткрытый и недоступен.</span><span class="sxs-lookup"><span data-stu-id="a40d3-124">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because these objects are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a40d3-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="a40d3-125">Remarks</span></span>

<span data-ttu-id="a40d3-126">Метод **IMAPISession::CompareEntryIDs** сравнивает два идентификаторы записей, относящихся к отдельный поставщик услуг для определения, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="a40d3-126">The **IMAPISession::CompareEntryIDs** method compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="a40d3-127">MAPI выделяет [MAPIUID](mapiuid.md) из идентификаторы записей для определения поставщика услуг, ответственных за объекты и затем вызывает метод **CompareEntryIDs** возвращается объект входа в систему для выполнения сравнения.</span><span class="sxs-lookup"><span data-stu-id="a40d3-127">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a40d3-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a40d3-128">Notes to callers</span></span>

<span data-ttu-id="a40d3-129">Метод **CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="a40d3-129">The **CompareEntryIDs** method is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="a40d3-130">Это может произойти, например, после установки новой версии поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="a40d3-130">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="a40d3-131">Если **CompareEntryIDs** возвращает ошибку, не имеет каких-либо действий на основании результатов сравнения.</span><span class="sxs-lookup"><span data-stu-id="a40d3-131">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="a40d3-132">Вместо этого можно использовать самый высокий подход невозможно.</span><span class="sxs-lookup"><span data-stu-id="a40d3-132">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="a40d3-133">**CompareEntryIDs** может оказаться неудачным, если, например один или оба идентификаторы записей содержит недопустимый **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="a40d3-133">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a40d3-134">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a40d3-134">MFCMAPI reference</span></span>

<span data-ttu-id="a40d3-135">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a40d3-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a40d3-136">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a40d3-136">**File**</span></span>|<span data-ttu-id="a40d3-137">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a40d3-137">**Function**</span></span>|<span data-ttu-id="a40d3-138">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a40d3-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a40d3-139">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="a40d3-139">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="a40d3-140">CbaseDialog::OnCompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a40d3-140">CbaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="a40d3-141">Mfcmapi (en) использует метод **IMAPISession::CompareEntryIDs** для сравнения двух идентификаторы, которые пользователь вводит.</span><span class="sxs-lookup"><span data-stu-id="a40d3-141">MFCMAPI uses the **IMAPISession::CompareEntryIDs** method to compare two entry IDs that a user enters.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a40d3-142">См. также</span><span class="sxs-lookup"><span data-stu-id="a40d3-142">See also</span></span>



[<span data-ttu-id="a40d3-143">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a40d3-143">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a40d3-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a40d3-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="a40d3-145">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a40d3-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

