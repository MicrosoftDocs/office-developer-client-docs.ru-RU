---
title: Откладывание ошибок MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93ae6d54-41cd-433c-8124-eb07d71baa57
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0cf56a92190acfab1a941bc8d3ad0acc1f3e1f89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338705"
---
# <a name="deferring-mapi-errors"></a><span data-ttu-id="00ec7-103">Откладывание ошибок MAPI</span><span class="sxs-lookup"><span data-stu-id="00ec7-103">Deferring MAPI Errors</span></span>

  
  
<span data-ttu-id="00ec7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00ec7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00ec7-105">Некоторые методы интерфейса принимают флаг МАПИ_ДЕФЕРРЕД_ЕРРОРС в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="00ec7-105">Some interface methods accept the MAPI_DEFERRED_ERRORS flag as an input parameter.</span></span> <span data-ttu-id="00ec7-106">Если этот флаг установлен, методу не требуется сразу же вернуть значение; Вы можете позволить абоненту узнать результат вызова в любое время позже.</span><span class="sxs-lookup"><span data-stu-id="00ec7-106">When this flag is set, the method does not have to return immediately with a value; it can let the caller know the result of the call at some later time.</span></span>
  
<span data-ttu-id="00ec7-107">Откладывание сообщений об ошибках помогает поставщикам услуг в их реализации сложных методов, что ускоряет обработку.</span><span class="sxs-lookup"><span data-stu-id="00ec7-107">Deferring errors helps service providers in their implementation of complex methods, making processing faster.</span></span> <span data-ttu-id="00ec7-108">Вместо того чтобы обрабатывать большое количество запросов и возвращать значение для каждого, откладывание ошибок позволяет объединить вызовы в пределах поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="00ec7-108">Rather than handling many requests and returning a value for each, deferring errors allows the calls to be bundled within the service provider.</span></span> <span data-ttu-id="00ec7-109">Обработка большого количества запросов за один раз приводит к снижению производительности сети, что повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="00ec7-109">Processing many requests at once cuts down on network traffic, thereby improving performance.</span></span> <span data-ttu-id="00ec7-110">Откладывание ошибок особенно полезна при вызовах удаления или копирования свойств, которые могут занимать много времени.</span><span class="sxs-lookup"><span data-stu-id="00ec7-110">Deferring errors is especially useful in calls to delete or copy properties, which can be very time-consuming operations.</span></span> 
  
<span data-ttu-id="00ec7-111">Когда клиент выполняет вызов, не устанавливая флаг МАПИ_ДЕФЕРРЕД_ЕРРОРС, который может обрабатываться по принципу "только отложенно", поставщики услуг могут откладывать ошибки независимо от состояния или возвращать МАПИ_Е_ТУ_КОМПЛЕКС.</span><span class="sxs-lookup"><span data-stu-id="00ec7-111">When a client makes a call without setting the MAPI_DEFERRED_ERRORS flag that can only be handled in a deferred manner, service providers can either defer the errors regardless or return MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="00ec7-112">Большинство клиентов должны откладывать ошибки в качестве предпочтительного способа для отказа в вызове.</span><span class="sxs-lookup"><span data-stu-id="00ec7-112">Most clients should defer errors as a preferable strategy to failing the call.</span></span> 
  
<span data-ttu-id="00ec7-113">Установка флага МАПИ_ДЕФЕРРЕД_ЕРРОРС изменяет реализацию обработки ошибок клиента, в результате чего возвращаемые сведения могут быть доставлены в любое время, а не в запланированное время.</span><span class="sxs-lookup"><span data-stu-id="00ec7-113">Setting the MAPI_DEFERRED_ERRORS flag changes a client's error handling implementation in that the returned information can be delivered at any time rather than at a planned time.</span></span> <span data-ttu-id="00ec7-114">Возникнет ошибка, которая может быть возвращена, когда она слишком поздно для выполнения каких-либо действий или после того, как данные о первоначальном запросе больше не будут доступны.</span><span class="sxs-lookup"><span data-stu-id="00ec7-114">It is possible for an error to be returned when it is too late to do anything about it or after data about the original request is no longer available.</span></span> <span data-ttu-id="00ec7-115">Например, если клиент вызывает **IMsgStore:: OpenEntry** , чтобы открыть удаленную папку с набором мапи_деферред_еррорс, клиент не узнает о проблеме до тех пор, пока не будет выполнен вызов **IMAPIProp::** -Props, чтобы получить одно из свойств папки.</span><span class="sxs-lookup"><span data-stu-id="00ec7-115">For example, if a client calls **IMsgStore::OpenEntry** to open a deleted folder with MAPI_DEFERRED_ERRORS set, the client will not know of the problem until an **IMAPIProp::GetProps** call is made to retrieve one of the folder's properties.</span></span> <span data-ttu-id="00ec7-116">\*\*\*\* После этого свойства PROPS будут возвращать мапи_е_нот_фаунд.</span><span class="sxs-lookup"><span data-stu-id="00ec7-116">**GetProps** will then return MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00ec7-117">См. также</span><span class="sxs-lookup"><span data-stu-id="00ec7-117">See also</span></span>



[<span data-ttu-id="00ec7-118">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="00ec7-118">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="00ec7-119">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="00ec7-119">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)

