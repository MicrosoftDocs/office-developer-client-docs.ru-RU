---
title: Имаписуппорткомпаринтридс
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
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331572"
---
# <a name="imapisupportcompareentryids"></a><span data-ttu-id="0b1c8-103">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="0b1c8-103">IMAPISupport::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="0b1c8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b1c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b1c8-105">Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="0b1c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b1c8-106">Parameters</span></span>

 <span data-ttu-id="0b1c8-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="0b1c8-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="0b1c8-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="0b1c8-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="0b1c8-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="0b1c8-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="0b1c8-110">возврата Указатель на первый идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="0b1c8-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="0b1c8-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="0b1c8-112">возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="0b1c8-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="0b1c8-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="0b1c8-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="0b1c8-114">возврата Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="0b1c8-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0b1c8-115">_ulFlags_</span></span>
  
> <span data-ttu-id="0b1c8-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0b1c8-117">_Лпулресулт_</span><span class="sxs-lookup"><span data-stu-id="0b1c8-117">_lpulResult_</span></span>
  
> <span data-ttu-id="0b1c8-118">вышли Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="0b1c8-119">ЗНАЧЕНИЕ TRUE, если два идентификатора записи ссылаются на один объект; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0b1c8-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b1c8-120">Return value</span></span>

<span data-ttu-id="0b1c8-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b1c8-121">S_OK</span></span> 
  
> <span data-ttu-id="0b1c8-122">Сравнение выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-122">The comparison was successful.</span></span>
    
<span data-ttu-id="0b1c8-123">МАПИ_Е_УНКНОВН_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="0b1c8-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="0b1c8-124">Один или оба идентификатора записи, указанные в качестве параметров, не ссылаются на допустимые объекты, возможно потому, что они неоткрыты и недоступны.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-124">One or both of the entry identifiers specified as parameters do not refer to valid objects, possibly because they are currently unopened and unavailable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b1c8-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b1c8-125">Remarks</span></span>

<span data-ttu-id="0b1c8-126">Метод **имаписуппорт:: метод compareentryids** реализован для адресных книг и объектов поддержки поставщиков хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-126">The **IMAPISupport::CompareEntryIDs** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="0b1c8-127">**Метод compareentryids** сравнивает два идентификатора записи, которые принадлежат одному поставщику услуг, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-127">**CompareEntryIDs** compares two entry identifiers that belong to a single service provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="0b1c8-128">MAPI извлекает часть [мапиуид](mapiuid.md) из идентификаторов записей, чтобы определить поставщика услуг, ответственного за объекты.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-128">MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects.</span></span> <span data-ttu-id="0b1c8-129">Затем MAPI вызывает метод **метод compareentryids** своего объекта logon для выполнения сравнения.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-129">MAPI then calls its logon object's **CompareEntryIDs** method to perform the comparison.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0b1c8-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="0b1c8-130">Notes to callers</span></span>

 <span data-ttu-id="0b1c8-131">**Метод compareentryids** полезен, так как объект может иметь несколько допустимых идентификаторов записи.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-131">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="0b1c8-132">Такая ситуация может возникать, например, после установки новой версии поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-132">This situation can occur, for example, after a new version of a service provider is installed.</span></span> 
  
<span data-ttu-id="0b1c8-133">Если **метод compareentryids** возвращает ошибку, не следует предпринимать никаких действий в зависимости от результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-133">If **CompareEntryIDs** returns an error, do not take any action based on the result of the comparison.</span></span> <span data-ttu-id="0b1c8-134">Вместо этого рекомендуется использовать максимально консервативный подход.</span><span class="sxs-lookup"><span data-stu-id="0b1c8-134">Instead, take the most conservative approach possible.</span></span> <span data-ttu-id="0b1c8-135">**Метод compareentryids** может не работать, если, например, один или оба идентификатора записи содержат недопустимую структуру **мапиуид** .</span><span class="sxs-lookup"><span data-stu-id="0b1c8-135">**CompareEntryIDs** might fail if, for example, one or both of the entry identifiers contain an invalid **MAPIUID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b1c8-136">См. также</span><span class="sxs-lookup"><span data-stu-id="0b1c8-136">See also</span></span>



[<span data-ttu-id="0b1c8-137">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0b1c8-137">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="0b1c8-138">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b1c8-138">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

