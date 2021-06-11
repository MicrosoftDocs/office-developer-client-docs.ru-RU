---
title: Отсрочка ошибок MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93ae6d54-41cd-433c-8124-eb07d71baa57
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0cf56a92190acfab1a941bc8d3ad0acc1f3e1f89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427341"
---
# <a name="deferring-mapi-errors"></a><span data-ttu-id="5d302-103">Отсрочка ошибок MAPI</span><span class="sxs-lookup"><span data-stu-id="5d302-103">Deferring MAPI Errors</span></span>

  
  
<span data-ttu-id="5d302-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d302-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d302-105">Некоторые методы интерфейса принимают флаг MAPI_DEFERRED_ERRORS в качестве параметра ввода.</span><span class="sxs-lookup"><span data-stu-id="5d302-105">Some interface methods accept the MAPI_DEFERRED_ERRORS flag as an input parameter.</span></span> <span data-ttu-id="5d302-106">Когда этот флаг заданной, метод не должен возвращаться сразу со значением; он может позволить звониву узнать результат вызова в более позднее время.</span><span class="sxs-lookup"><span data-stu-id="5d302-106">When this flag is set, the method does not have to return immediately with a value; it can let the caller know the result of the call at some later time.</span></span>
  
<span data-ttu-id="5d302-107">Отсрочка ошибок помогает поставщикам услуг в их реализации сложных методов, делая обработку быстрее.</span><span class="sxs-lookup"><span data-stu-id="5d302-107">Deferring errors helps service providers in their implementation of complex methods, making processing faster.</span></span> <span data-ttu-id="5d302-108">Вместо обработки многих запросов и возврата значения для каждого из них, перенос ошибок позволяет объединить вызовы в поставщике услуг.</span><span class="sxs-lookup"><span data-stu-id="5d302-108">Rather than handling many requests and returning a value for each, deferring errors allows the calls to be bundled within the service provider.</span></span> <span data-ttu-id="5d302-109">Обработка многих запросов одновременно сокращает сетевой трафик, тем самым повышая производительность.</span><span class="sxs-lookup"><span data-stu-id="5d302-109">Processing many requests at once cuts down on network traffic, thereby improving performance.</span></span> <span data-ttu-id="5d302-110">Отсрочка ошибок особенно полезна при вызовах для удаления или копирования свойств, которые могут быть очень трудоемкими операциями.</span><span class="sxs-lookup"><span data-stu-id="5d302-110">Deferring errors is especially useful in calls to delete or copy properties, which can be very time-consuming operations.</span></span> 
  
<span data-ttu-id="5d302-111">Если клиент совершает вызов без установки флага MAPI_DEFERRED_ERRORS, который может обрабатываться только отложенным способом, поставщики услуг могут отложить ошибки независимо от них или MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="5d302-111">When a client makes a call without setting the MAPI_DEFERRED_ERRORS flag that can only be handled in a deferred manner, service providers can either defer the errors regardless or return MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="5d302-112">Большинству клиентов следует отложить ошибки в качестве предпочтительной стратегии для отказа от вызова.</span><span class="sxs-lookup"><span data-stu-id="5d302-112">Most clients should defer errors as a preferable strategy to failing the call.</span></span> 
  
<span data-ttu-id="5d302-113">Настройка флага MAPI_DEFERRED_ERRORS изменяет реализацию обработки ошибок клиента в том, что возвращаемая информация может быть доставлена в любое время, а не в запланированное время.</span><span class="sxs-lookup"><span data-stu-id="5d302-113">Setting the MAPI_DEFERRED_ERRORS flag changes a client's error handling implementation in that the returned information can be delivered at any time rather than at a planned time.</span></span> <span data-ttu-id="5d302-114">Ошибка может быть возвращена, когда слишком поздно что-либо сделать или после того, как данные о первоначальном запросе перестают быть доступны.</span><span class="sxs-lookup"><span data-stu-id="5d302-114">It is possible for an error to be returned when it is too late to do anything about it or after data about the original request is no longer available.</span></span> <span data-ttu-id="5d302-115">Например, если клиент вызывает **IMsgStore::OpenEntry,** чтобы открыть удаленную папку с набором MAPI_DEFERRED_ERRORS, клиент не узнает о проблеме, пока не будет выполнен вызов **IMAPIProp::GetProps** для получения одного из свойств папки.</span><span class="sxs-lookup"><span data-stu-id="5d302-115">For example, if a client calls **IMsgStore::OpenEntry** to open a deleted folder with MAPI_DEFERRED_ERRORS set, the client will not know of the problem until an **IMAPIProp::GetProps** call is made to retrieve one of the folder's properties.</span></span> <span data-ttu-id="5d302-116">**Затем GetProps** возвращает MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="5d302-116">**GetProps** will then return MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d302-117">См. также</span><span class="sxs-lookup"><span data-stu-id="5d302-117">See also</span></span>



[<span data-ttu-id="5d302-118">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5d302-118">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="5d302-119">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="5d302-119">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)

