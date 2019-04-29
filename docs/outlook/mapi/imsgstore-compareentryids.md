---
title: Имсгсторекомпаринтридс
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
# <a name="imsgstorecompareentryids"></a><span data-ttu-id="233ad-103">IMsgStore::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="233ad-103">IMsgStore::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="233ad-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="233ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="233ad-105">Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на одну и ту же запись в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="233ad-105">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span> <span data-ttu-id="233ad-106">MAPI передает этот вызов поставщику услуг, только если уникальные идентификаторы (UID) в обоих идентификаторах записей будут обрабатываться этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="233ad-106">MAPI passes this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="233ad-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="233ad-107">Parameters</span></span>

 <span data-ttu-id="233ad-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="233ad-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="233ad-109">возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="233ad-109">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="233ad-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="233ad-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="233ad-111">возврата Указатель на первый идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="233ad-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="233ad-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="233ad-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="233ad-113">возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="233ad-113">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="233ad-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="233ad-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="233ad-115">возврата Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="233ad-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="233ad-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="233ad-116">_ulFlags_</span></span>
  
> <span data-ttu-id="233ad-117">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="233ad-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="233ad-118">_Лпулресулт_</span><span class="sxs-lookup"><span data-stu-id="233ad-118">_lpulResult_</span></span>
  
> <span data-ttu-id="233ad-119">вышли Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="233ad-119">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="233ad-120">ЗНАЧЕНИЕ TRUE, если два идентификатора записи ссылаются на один объект; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="233ad-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="233ad-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="233ad-121">Return value</span></span>

<span data-ttu-id="233ad-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="233ad-122">S_OK</span></span> 
  
> <span data-ttu-id="233ad-123">Сравнение выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="233ad-123">The comparison was successful.</span></span>
    
<span data-ttu-id="233ad-124">МАПИ_Е_УНКНОВН_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="233ad-124">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="233ad-125">Один или оба идентификатора записи, указанные в качестве параметров, не ссылаются на объекты, возможно, из-за того, что соответствующие объекты не открыты и недоступны в данный момент.</span><span class="sxs-lookup"><span data-stu-id="233ad-125">One or both of the entry identifiers specified as parameters do not refer to objects, possibly because the corresponding objects are unopened and unavailable at present.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="233ad-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="233ad-126">Remarks</span></span>

<span data-ttu-id="233ad-127">Метод **IMsgStore:: метод compareentryids** сравнивает два идентификатора записи, которые принадлежат хранилищу сообщений, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="233ad-127">The **IMsgStore::CompareEntryIDs** method compares two entry identifiers that belong to the message store to determine whether they refer to the same object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="233ad-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="233ad-128">Notes to callers</span></span>

 <span data-ttu-id="233ad-129">**Метод compareentryids** полезен, так как объект может иметь несколько допустимых идентификаторов записи (например, после установки новой версии поставщика хранилища сообщений).</span><span class="sxs-lookup"><span data-stu-id="233ad-129">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier (for example, after a new version of a message store provider is installed).</span></span> 
  
<span data-ttu-id="233ad-130">Если **метод compareentryids** возвращает ошибку, не следует предпринимать никаких действий в зависимости от результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="233ad-130">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="233ad-131">Вместо этого рекомендуется использовать максимально консервативный подход.</span><span class="sxs-lookup"><span data-stu-id="233ad-131">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="233ad-132">**Метод compareentryids** может не работать, если, например, один или оба идентификатора записи содержат недопустимый **мапиуид**.</span><span class="sxs-lookup"><span data-stu-id="233ad-132">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contains an invalid **MAPIUID**.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="233ad-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="233ad-133">MFCMAPI reference</span></span>

<span data-ttu-id="233ad-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="233ad-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="233ad-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="233ad-135">**File**</span></span>|<span data-ttu-id="233ad-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="233ad-136">**Function**</span></span>|<span data-ttu-id="233ad-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="233ad-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="233ad-138">Баседиалог. cpp</span><span class="sxs-lookup"><span data-stu-id="233ad-138">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="233ad-139">Кбаседиалог:: Онкомпаринтридс</span><span class="sxs-lookup"><span data-stu-id="233ad-139">CBaseDialog::OnCompareEntryIDs</span></span>  <br/> |<span data-ttu-id="233ad-140">MFCMAPI использует метод **IMsgStore:: метод compareentryids** для сравнения идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="233ad-140">MFCMAPI uses the **IMsgStore::CompareEntryIDs** method to compare entry IDs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="233ad-141">См. также</span><span class="sxs-lookup"><span data-stu-id="233ad-141">See also</span></span>



[<span data-ttu-id="233ad-142">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="233ad-142">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="233ad-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="233ad-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="233ad-144">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="233ad-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

