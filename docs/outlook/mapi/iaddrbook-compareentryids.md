---
title: Иаддрбуккомпаринтридс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424261"
---
# <a name="iaddrbookcompareentryids"></a><span data-ttu-id="c9396-103">IAddrBook::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="c9396-103">IAddrBook::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="c9396-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9396-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9396-105">Сравнивает два идентификатора записи, которые относятся к определенному поставщику адресных книг, чтобы определить, ссылаются ли они на один и тот же объект адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9396-105">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="c9396-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9396-106">Parameters</span></span>

 <span data-ttu-id="c9396-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="c9396-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="c9396-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="c9396-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="c9396-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="c9396-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="c9396-110">возврата Указатель на первый идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="c9396-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="c9396-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="c9396-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="c9396-112">возврата Число байтов в идентификаторе записи, на которое указывает параметр _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="c9396-112">[in] The byte count in the entry identifier pointed to by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="c9396-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="c9396-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="c9396-114">возврата Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="c9396-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="c9396-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9396-115">_ulFlags_</span></span>
  
> <span data-ttu-id="c9396-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="c9396-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c9396-117">_Лпулресулт_</span><span class="sxs-lookup"><span data-stu-id="c9396-117">_lpulResult_</span></span>
  
> <span data-ttu-id="c9396-118">вышли Указатель на результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="c9396-118">[out] A pointer to the result of the comparison.</span></span> <span data-ttu-id="c9396-119">Для содержимого _лпулресулт_ заДАЕТСЯ значение true, если два идентификатора записи ссылаются на один и тот же объект; в противном случае для содержимого задается значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="c9396-119">The contents of  _lpulResult_ are set to TRUE if the two entry identifiers refer to the same object; otherwise, the contents are set to FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c9396-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9396-120">Return value</span></span>

<span data-ttu-id="c9396-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9396-121">S_OK</span></span> 
  
> <span data-ttu-id="c9396-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="c9396-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c9396-123">МАПИ_Е_УНКНОВН_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="c9396-123">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="c9396-124">Один или оба идентификатора записи, переданные с параметрами _lpEntryID1_ или _lpEntryID2_ , не распознаются ни одним поставщиком адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c9396-124">One or both of the entry identifiers passed in with the  _lpEntryID1_ or  _lpEntryID2_ parameters are not recognized by any address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c9396-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9396-125">Remarks</span></span>

<span data-ttu-id="c9396-126">Клиентские приложения и поставщики услуг вызывают метод **метод compareentryids** , чтобы сравнить два идентификатора записи, принадлежащие одному поставщику адресных книг, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="c9396-126">Client applications and service providers call the **CompareEntryIDs** method to compare two entry identifiers that belongs to a single address book provider to determine whether they refer to the same object.</span></span> <span data-ttu-id="c9396-127">**Метод compareentryids** полезен, так как объект может иметь несколько допустимых идентификаторов записи.</span><span class="sxs-lookup"><span data-stu-id="c9396-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="c9396-128">Такая ситуация может возникать, например, после установки новой версии поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="c9396-128">This situation can occur, for example, after a new version of an address book provider is installed.</span></span> 
  
<span data-ttu-id="c9396-129">MAPI передает этот вызов поставщику адресной книги, который отвечает за идентификаторы записей, определяя соответствующий поставщик, сопоставляя структуру [мапиуид](mapiuid.md) в идентификаторах записей с помощью структуры **мапиуид** , зарегистрированной поставщики.</span><span class="sxs-lookup"><span data-stu-id="c9396-129">MAPI passes this call to the address book provider that is responsible for the entry identifiers, determining the appropriate provider by matching the [MAPIUID](mapiuid.md) structure in the entry identifiers with the **MAPIUID** structure registered by the provider.</span></span> 
  
<span data-ttu-id="c9396-130">Если два идентификатора записи ссылаются на один и тот же объект, **метод compareentryids** задает для параметра _лпулресулт_ значение true; Если они ссылаются на различные объекты, **метод compareentryids** задает для содержимого значение false.</span><span class="sxs-lookup"><span data-stu-id="c9396-130">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the contents of the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets the contents to FALSE.</span></span> <span data-ttu-id="c9396-131">В обоих случаях **метод compareentryids** ВОЗВРАЩАЕТ значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="c9396-131">In either case, **CompareEntryIDs** returns S_OK.</span></span> <span data-ttu-id="c9396-132">Если **метод compareentryids** возвращает ошибку, которая может возникнуть, если у поставщика адресных книг не зарегистрирована структура **мапиуид** , соответствующая одной из идентификаторов записей, клиенты и поставщики не должны предпринимать никаких действий в зависимости от результата Сравнение.</span><span class="sxs-lookup"><span data-stu-id="c9396-132">If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison.</span></span> <span data-ttu-id="c9396-133">Вместо этого они должны принимать наиболее консервативный подход к выполняемому действию.</span><span class="sxs-lookup"><span data-stu-id="c9396-133">They should instead take the most conservative approach to the action being performed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9396-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c9396-134">See also</span></span>



[<span data-ttu-id="c9396-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c9396-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

