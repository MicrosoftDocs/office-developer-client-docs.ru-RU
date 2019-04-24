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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335534"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="5fa22-103">Сравнение записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="5fa22-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="5fa22-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fa22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fa22-105">Реализация поставщика [иаблогон:: метод compareentryids](iablogon-compareentryids.md) сравнивает идентификаторы записей для двух объектов поставщика.</span><span class="sxs-lookup"><span data-stu-id="5fa22-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="5fa22-106">MAPI вызывает этот метод после определения того, что два идентификатора записи содержат зарегистрированный [мапиуид](mapiuid.md)поставщика.</span><span class="sxs-lookup"><span data-stu-id="5fa22-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="5fa22-107">Таким образом, метод **метод compareentryids** не должен проверять, что идентификаторы записей, переданные для параметров _lpEntryID1_ и _lpEntryID2_ , принадлежат поставщику.</span><span class="sxs-lookup"><span data-stu-id="5fa22-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="5fa22-108">Вызов **иаблогон:: метод compareentryids** эквивалентно извлечению свойства **пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) для каждого из двух объектов и их сравнения напрямую.</span><span class="sxs-lookup"><span data-stu-id="5fa22-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="5fa22-109">**Реализация метод compareentryids**</span><span class="sxs-lookup"><span data-stu-id="5fa22-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="5fa22-110">Проверьте тип идентификаторов записей, которые передаются, если поставщик хранит эти сведения.</span><span class="sxs-lookup"><span data-stu-id="5fa22-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="5fa22-111">Например, один идентификатор записи может относиться к пользователю обмена сообщениями, а другой может относиться к списку рассылки.</span><span class="sxs-lookup"><span data-stu-id="5fa22-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="5fa22-112">Если типы не совпадают, присвойте параметру _лпулресулт_ значение false и ВОЗВРАТИТЕ значение false.</span><span class="sxs-lookup"><span data-stu-id="5fa22-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="5fa22-113">Сравните размеры двух идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="5fa22-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="5fa22-114">Если они не совпадают, присвойте параметру _лпулресулт_ значение false и ВОЗВРАТИТЕ значение false.</span><span class="sxs-lookup"><span data-stu-id="5fa22-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="5fa22-115">Убедитесь, что размер идентификатора записи задан правильно для соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="5fa22-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="5fa22-116">В противном случае присвойте параметру _лпулресулт_ значение false и возвратите значение ошибки мапи_е_ункновн_ентрид.</span><span class="sxs-lookup"><span data-stu-id="5fa22-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="5fa22-117">Проверьте, совпадают ли идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="5fa22-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="5fa22-118">Если они сравниваются одинаково, присвойте параметру _лпулресулт_ значение true и Return.</span><span class="sxs-lookup"><span data-stu-id="5fa22-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="5fa22-119">В противном случае задайте для него значение FALSE перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="5fa22-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="5fa22-120">Если ваш поставщик сравнивает краткосрочный идентификатор записи с долгосрочным идентификатором, он должен сравниваться одинаково.</span><span class="sxs-lookup"><span data-stu-id="5fa22-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

