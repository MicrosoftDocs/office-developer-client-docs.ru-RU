---
title: Откладывание ошибки MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93ae6d54-41cd-433c-8124-eb07d71baa57
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3d2a46be04f235ba55aa5f2feef222ea7372b211
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569864"
---
# <a name="deferring-mapi-errors"></a><span data-ttu-id="bf7a4-103">Откладывание ошибки MAPI</span><span class="sxs-lookup"><span data-stu-id="bf7a4-103">Deferring MAPI Errors</span></span>

  
  
<span data-ttu-id="bf7a4-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf7a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf7a4-105">Некоторые методы интерфейса принятие флаг MAPI_DEFERRED_ERRORS в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-105">Some interface methods accept the MAPI_DEFERRED_ERRORS flag as an input parameter.</span></span> <span data-ttu-id="bf7a4-106">Если этот флаг, метод не имеет сразу же возвращает значение; Это позволяет вызывающему объекту определить результат вызова позднее.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-106">When this flag is set, the method does not have to return immediately with a value; it can let the caller know the result of the call at some later time.</span></span>
  
<span data-ttu-id="bf7a4-107">Откладывание ошибок помогает поставщиков услуг в их реализации сложных методы внесения обработки быстрее.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-107">Deferring errors helps service providers in their implementation of complex methods, making processing faster.</span></span> <span data-ttu-id="bf7a4-108">Вместо обработки большого числа запросов и возвращает значение для каждого из них, откладывая ошибки позволяет вызовы поставляется в рамках поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-108">Rather than handling many requests and returning a value for each, deferring errors allows the calls to be bundled within the service provider.</span></span> <span data-ttu-id="bf7a4-109">Обработка большого количества запросов за один раз уменьшение сетевого трафика, тем самым повышение производительности.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-109">Processing many requests at once cuts down on network traffic, thereby improving performance.</span></span> <span data-ttu-id="bf7a4-110">Откладывание ошибки особенно полезен в звонков для удаления или копии свойства, которые могут быть очень длительных операций.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-110">Deferring errors is especially useful in calls to delete or copy properties, which can be very time-consuming operations.</span></span> 
  
<span data-ttu-id="bf7a4-111">Если клиент вызывает без параметру MAPI_DEFERRED_ERRORS флаг, который может обрабатывать только отложенная, поставщиков услуг либо можно отложить ошибки вне зависимости от или вернуть MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-111">When a client makes a call without setting the MAPI_DEFERRED_ERRORS flag that can only be handled in a deferred manner, service providers can either defer the errors regardless or return MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="bf7a4-112">Большинство клиентов следует обратиться ошибки как предпочтительными стратегии для восстановления после сбоя вызова.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-112">Most clients should defer errors as a preferable strategy to failing the call.</span></span> 
  
<span data-ttu-id="bf7a4-113">Установка MAPI_DEFERRED_ERRORS флаг изменяет обработка реализации, в том, что возвращенные данные могут доставляться в любое время, а не в запланированного времени ошибок клиента.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-113">Setting the MAPI_DEFERRED_ERRORS flag changes a client's error handling implementation in that the returned information can be delivered at any time rather than at a planned time.</span></span> <span data-ttu-id="bf7a4-114">Это и возможно наличие ошибки, должно быть возвращено, если это слишком позднего никаких действий о нем или после данные о исходный запрос больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-114">It is possible for an error to be returned when it is too late to do anything about it or after data about the original request is no longer available.</span></span> <span data-ttu-id="bf7a4-115">К примеру клиент вызывает **IMsgStore::OpenEntry** , чтобы открыть удаленной папке с набором MAPI_DEFERRED_ERRORS, клиент не будет сведений проблемы до **IMAPIProp::GetProps** вызов извлечение из свойства папки.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-115">For example, if a client calls **IMsgStore::OpenEntry** to open a deleted folder with MAPI_DEFERRED_ERRORS set, the client will not know of the problem until an **IMAPIProp::GetProps** call is made to retrieve one of the folder's properties.</span></span> <span data-ttu-id="bf7a4-116">**GetProps** будет возвращать MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-116">**GetProps** will then return MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf7a4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="bf7a4-117">See also</span></span>



[<span data-ttu-id="bf7a4-118">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="bf7a4-118">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="bf7a4-119">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="bf7a4-119">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)

