---
title: Стратегии обработки ошибок
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9e76ae3f292d8348b9dc64cb54bffae96b96e871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424149"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="ce09a-103">Стратегии обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="ce09a-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="ce09a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce09a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce09a-105">Так как методы интерфейса являются виртуальными, невозможно знать, как вызывающий, полный набор значений, которые можно возвратить из любого из одного вызова.</span><span class="sxs-lookup"><span data-stu-id="ce09a-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="ce09a-106">Одна реализация метода может вернуть пять значений; другой может вернуть восемь.</span><span class="sxs-lookup"><span data-stu-id="ce09a-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="ce09a-107">В справочных записях в документации по MAPI перечислено несколько значений, которые можно возвратить для каждого метода; Это значения, которые клиент или поставщик услуг может проверить и обработать, так как у них есть особые значения.</span><span class="sxs-lookup"><span data-stu-id="ce09a-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="ce09a-108">Другие значения могут быть возвращены, но так как они не являются значимыми, Специальный код для их обработки не требуется.</span><span class="sxs-lookup"><span data-stu-id="ce09a-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="ce09a-109">Простая проверка на успешность или сбой является достаточной.</span><span class="sxs-lookup"><span data-stu-id="ce09a-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="ce09a-110">Некоторые из методов интерфейса возвращают предупреждения.</span><span class="sxs-lookup"><span data-stu-id="ce09a-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="ce09a-111">Если метод, который вызывает клиент или поставщик услуг, может возвращать предупреждение, используйте макрос **HR_FAILED** , чтобы проверить возвращаемое значение, а не проверку на ноль или ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ce09a-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="ce09a-112">Предупреждения, хотя ненулевые, отличаются от кодов ошибок тем, что для них не задана Высокая скорость.</span><span class="sxs-lookup"><span data-stu-id="ce09a-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="ce09a-113">Если ваш клиент или поставщик услуг не используют макросы, то, скорее всего, предупреждение об ошибке может быть ошибочным.</span><span class="sxs-lookup"><span data-stu-id="ce09a-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="ce09a-114">Хотя большинство методов и функций интерфейса возвращают значения HRESULT, некоторые функции возвращают неподписанные длинные значения.</span><span class="sxs-lookup"><span data-stu-id="ce09a-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="ce09a-115">Кроме того, некоторые методы, используемые в среде MAPI, поступают из COM и возвращают значения ошибок COM, а не значения ошибок MAPI.</span><span class="sxs-lookup"><span data-stu-id="ce09a-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="ce09a-116">При совершении вызовов учитывайте следующие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="ce09a-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="ce09a-117">Никогда не полагайтесь на и не используйте значения возврата от **IUnknown:: AddRef** или **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="ce09a-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="ce09a-118">Эти возвращаемые значения предназначены только для диагностики.</span><span class="sxs-lookup"><span data-stu-id="ce09a-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="ce09a-119">**IUnknown:: QueryInterface** всегда возвращает общие ошибки COM, в которых FACILITY_NULL или FACILITY_RPC, а не ошибки MAPI.</span><span class="sxs-lookup"><span data-stu-id="ce09a-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="ce09a-120">Все остальные методы интерфейса возвращают ошибки интерфейса MAPI с помощью FACILITY_ITF, а также FACILITY_RPC или FACILITY_NULL ошибок.</span><span class="sxs-lookup"><span data-stu-id="ce09a-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="ce09a-121">При вызове неподдерживаемого метода MAPI может возвращаться одна из четырех возможных ошибок:</span><span class="sxs-lookup"><span data-stu-id="ce09a-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="ce09a-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ce09a-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="ce09a-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ce09a-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="ce09a-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ce09a-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="ce09a-125">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="ce09a-125">MAPI_E_VERSION.</span></span> 
  

