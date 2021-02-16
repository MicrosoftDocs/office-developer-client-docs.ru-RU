---
title: Сравнение записей адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6ccd7a55c195b45b1fa83db6180efeacd41b968d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415357"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="2232f-103">Сравнение записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="2232f-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="2232f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2232f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2232f-105">Реализация [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) поставщика сравнивает идентификаторы записей для двух объектов поставщика.</span><span class="sxs-lookup"><span data-stu-id="2232f-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="2232f-106">MAPI вызывает этот метод после определения того, что два идентификатора записи содержат зарегистрированный [MAPIUID поставщика.](mapiuid.md)</span><span class="sxs-lookup"><span data-stu-id="2232f-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="2232f-107">Поэтому метод **CompareEntryIDs** не должен проверять, что идентификаторы записей, переданные для  _параметров lpEntryID1_ и  _lpEntryID2,_ принадлежат поставщику.</span><span class="sxs-lookup"><span data-stu-id="2232f-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="2232f-108">Вызов **IABLogon::CompareEntryIDs** эквивалентен тому, как получить свойство **PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)для каждого из двух объектов и сравнить их напрямую.</span><span class="sxs-lookup"><span data-stu-id="2232f-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="2232f-109">**Реализация CompareEntryIds**</span><span class="sxs-lookup"><span data-stu-id="2232f-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="2232f-110">Проверьте тип идентификаторов записей, переданных, если поставщик сохраняет эти сведения.</span><span class="sxs-lookup"><span data-stu-id="2232f-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="2232f-111">Например, один идентификатор записи может принадлежать пользователю системы обмена сообщениями, а другой — списку рассылки.</span><span class="sxs-lookup"><span data-stu-id="2232f-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="2232f-112">Если типы не совпадают, установите для  _параметра lpulResult_ параметр FALSE и вернетесь.</span><span class="sxs-lookup"><span data-stu-id="2232f-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="2232f-113">Сравните размеры двух идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="2232f-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="2232f-114">Если они не одинаковые, установите для  _содержимого параметра lpulResult_ параметр FALSE и вернетесь.</span><span class="sxs-lookup"><span data-stu-id="2232f-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="2232f-115">Убедитесь, что размер идентификаторов записей правильный для их типа.</span><span class="sxs-lookup"><span data-stu-id="2232f-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="2232f-116">Если нет, установите для  _содержимого параметра lpulResult_ значение FALSE и вернетесь значение ошибки MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="2232f-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="2232f-117">Проверьте, одинаковы ли идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="2232f-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="2232f-118">Если они сравнивают одинаково, установите для  _содержимого параметра lpulResult_ параметр TRUE и возврат.</span><span class="sxs-lookup"><span data-stu-id="2232f-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="2232f-119">В противном случае установите для него false перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="2232f-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="2232f-120">Если поставщик сравнивает краткосрочный идентификатор записи с долгосрочным идентификатором, он должен сравниться одинаково.</span><span class="sxs-lookup"><span data-stu-id="2232f-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

