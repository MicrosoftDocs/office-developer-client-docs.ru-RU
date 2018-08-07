---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c939189c2c8f7d3147c3146f55deac0e032ce9df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809113"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="efbf8-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="efbf8-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="efbf8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="efbf8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="efbf8-105">Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="efbf8-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="efbf8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efbf8-106">Parameters</span></span>

 <span data-ttu-id="efbf8-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="efbf8-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="efbf8-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="efbf8-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="efbf8-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="efbf8-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="efbf8-110">[in] Указатель на первый идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="efbf8-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="efbf8-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="efbf8-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="efbf8-112">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="efbf8-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="efbf8-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="efbf8-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="efbf8-114">[in] Указатель на второй идентификатор записи для сравнения.</span><span class="sxs-lookup"><span data-stu-id="efbf8-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="efbf8-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="efbf8-115">_ulFlags_</span></span>
  
> <span data-ttu-id="efbf8-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="efbf8-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="efbf8-117">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="efbf8-117">_lpulResult_</span></span>
  
> <span data-ttu-id="efbf8-118">[out] Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="efbf8-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="efbf8-119">Значение TRUE, если идентификаторы двух записей ссылаются на тот же объект; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="efbf8-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="efbf8-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="efbf8-120">Return value</span></span>

<span data-ttu-id="efbf8-121">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="efbf8-121">S_OK</span></span> 
  
> <span data-ttu-id="efbf8-122">Сравнение успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="efbf8-122">The comparison was successful.</span></span>
    
<span data-ttu-id="efbf8-123">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="efbf8-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="efbf8-124">Одно или оба идентификаторы записей, указанный в качестве параметров ссылается на допустимый объекты возможно так как они в настоящее время неоткрытый и недоступен.</span><span class="sxs-lookup"><span data-stu-id="efbf8-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="efbf8-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="efbf8-125">Remarks</span></span>

<span data-ttu-id="efbf8-126">Метод **IMAPISupport::CompareEntryIDs** реализуется для адресной книги и сообщения хранилища поставщика объекты поддержки.</span><span class="sxs-lookup"><span data-stu-id="efbf8-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="efbf8-127">**CompareEntryIDs** сравниваются два идентификаторы записей, относящихся к отдельный поставщик услуг для определения, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="efbf8-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="efbf8-128">MAPI выделяет [MAPIUID](mapiuid.md) из идентификаторы записей для определения поставщика услуг, ответственных за объекты.</span><span class="sxs-lookup"><span data-stu-id="efbf8-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="efbf8-129">MAPI вызывает метод **CompareEntryIDs** возвращается объект входа в систему для выполнения сравнения.</span><span class="sxs-lookup"><span data-stu-id="efbf8-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="efbf8-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="efbf8-130">Notes to callers</span></span>

 <span data-ttu-id="efbf8-131">**CompareEntryIDs** полезен, так как объект может иметь несколько идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="efbf8-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="efbf8-132">Это может произойти, например, после установки новой версии поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="efbf8-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="efbf8-133">Если **CompareEntryIDs** возвращает ошибку, не имеет каких-либо действий на основании результатов сравнения.</span><span class="sxs-lookup"><span data-stu-id="efbf8-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="efbf8-134">Вместо этого можно использовать самый высокий подход невозможно.</span><span class="sxs-lookup"><span data-stu-id="efbf8-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="efbf8-135">**CompareEntryIDs** может оказаться неудачным, если, например один или оба идентификаторы записей содержит недопустимый структуры **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="efbf8-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efbf8-136">См. также</span><span class="sxs-lookup"><span data-stu-id="efbf8-136">See also</span></span>



[<span data-ttu-id="efbf8-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="efbf8-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="efbf8-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="efbf8-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

