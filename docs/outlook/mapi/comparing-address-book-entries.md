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
ms.openlocfilehash: 808d5f4bfca15cae4ca7aab6758d3b5361813bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808174"
---
# <a name="comparing-address-book-entries"></a><span data-ttu-id="5f4b2-103">Сравнение записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="5f4b2-103">Comparing Address Book Entries</span></span>

  
  
<span data-ttu-id="5f4b2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f4b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f4b2-105">Реализация [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) ваш поставщик сравнивает идентификаторы записей для двух объектов ваш поставщик.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-105">Your provider's [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) implementation compares the entry identifiers for two of your provider's objects.</span></span> <span data-ttu-id="5f4b2-106">MAPI вызывает этот метод после определения, что идентификаторы двух записей содержать ваш поставщик регистрации [MAPIUID](mapiuid.md).</span><span class="sxs-lookup"><span data-stu-id="5f4b2-106">MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md).</span></span> <span data-ttu-id="5f4b2-107">Таким образом метод **CompareEntryIDs** должны проверяет, что идентификаторы записей, переданных параметров _lpEntryID1_ и _lpEntryID2_ принадлежат к поставщику.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-107">Therefore, your **CompareEntryIDs** method need not check that the entry identifiers passed in for the  _lpEntryID1_ and  _lpEntryID2_ parameters belong to your provider.</span></span> 
  
<span data-ttu-id="5f4b2-108">Вызов **IABLogon::CompareEntryIDs** эквивалентен извлечение свойства **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) для каждой из двух объектов и напрямую их сравнения.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-108">Calling **IABLogon::CompareEntryIDs** is equivalent to retrieving the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property for each of the two objects and comparing them directly.</span></span>
  
 <span data-ttu-id="5f4b2-109">**Для реализации CompareEntryIds**</span><span class="sxs-lookup"><span data-stu-id="5f4b2-109">**To implement CompareEntryIds**</span></span>
  
1. <span data-ttu-id="5f4b2-110">Проверка типа идентификаторы записей, переданные в, если ваш поставщик сохраняет их в.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-110">Check the type of the entry identifiers passed in if your provider stores that information.</span></span> <span data-ttu-id="5f4b2-111">Например один идентификатор записи может быть участником обмена сообщениями пользователя в то время как другой может принадлежать в список рассылки.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-111">For example, one entry identifier might belong to a messaging user while the other might belong to a distribution list.</span></span> <span data-ttu-id="5f4b2-112">Несовпадение типов значение содержимого параметра _lpulResult_ значение FALSE и возврата.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-112">If the types do not match, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
2. <span data-ttu-id="5f4b2-113">Сравните размеры идентификаторы двух записей.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-113">Compare the sizes of the two entry identifiers.</span></span> <span data-ttu-id="5f4b2-114">Если они не совпадают, значение содержимого параметра _lpulResult_ значение FALSE и возврат.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-114">If they are not the same, set the contents of the  _lpulResult_ parameter to FALSE and return.</span></span> 
    
3. <span data-ttu-id="5f4b2-115">Убедитесь, что размер идентификаторы записей правильный размер для их типа.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-115">Check that the size of the entry identifiers is the correct size for their type.</span></span> <span data-ttu-id="5f4b2-116">В противном случае задайте содержимое параметра _lpulResult_ значение FALSE и возвращают значение ошибки MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-116">If not, set the contents of the  _lpulResult_ parameter to FALSE and return the error value MAPI_E_UNKNOWN_ENTRYID.</span></span> 
    
4. <span data-ttu-id="5f4b2-117">Проверка же идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-117">Check if the entry identifiers are the same.</span></span> <span data-ttu-id="5f4b2-118">Если они сравнить одинаково, необходимо задайте содержимое параметра _lpulResult_ значение TRUE и возврата.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-118">If they compare equally, set the contents of the  _lpulResult_ parameter to TRUE and return.</span></span> <span data-ttu-id="5f4b2-119">В противном случае следует задайте значение FALSE до возвращения.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-119">Otherwise, set it to FALSE before returning.</span></span> 
    
5. <span data-ttu-id="5f4b2-120">Если ваш поставщик сравнение краткосрочных идентификатор записи с идентификатором долгосрочного, они должны одинаково сравнения.</span><span class="sxs-lookup"><span data-stu-id="5f4b2-120">If your provider is comparing a short-term entry identifier with a long-term identifier, they should compare equally.</span></span>
    

