---
title: Обработка ошибок свойств MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1dc676101d4c39544c9dd1fae94000db9963ea02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419081"
---
# <a name="handling-mapi-property-errors"></a><span data-ttu-id="aaf95-103">Обработка ошибок свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="aaf95-103">Handling MAPI property errors</span></span>

<span data-ttu-id="aaf95-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaf95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aaf95-105">Вместо полного сбоя или успешного выполнения следующие **методы IMAPIProp** сообщают о частичном успехе:</span><span class="sxs-lookup"><span data-stu-id="aaf95-105">Instead of complete failure or success, the following **IMAPIProp** methods report partial success:</span></span> 
  
[<span data-ttu-id="aaf95-106">GetProps</span><span class="sxs-lookup"><span data-stu-id="aaf95-106">GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="aaf95-107">SetProps</span><span class="sxs-lookup"><span data-stu-id="aaf95-107">SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="aaf95-108">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="aaf95-108">DeleteProps</span></span>](imapiprop-deleteprops.md)
  
[<span data-ttu-id="aaf95-109">CopyTo</span><span class="sxs-lookup"><span data-stu-id="aaf95-109">CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="aaf95-110">CopyProps</span><span class="sxs-lookup"><span data-stu-id="aaf95-110">CopyProps</span></span>](imapiprop-copyprops.md)
  
<span data-ttu-id="aaf95-111">**GetProps** сообщает о частичном успехе, когда он может получить хотя бы одно из запрашиваемого свойства для объекта.</span><span class="sxs-lookup"><span data-stu-id="aaf95-111">**GetProps** reports partial success when it can retrieve at least one of the requested properties for an object.</span></span> <span data-ttu-id="aaf95-112">**GetProps** указывает на частичный успех, возвращая предупреждение MAPI_W_ERRORS_RETURNED и размещая сведения о недоступных свойствах в массиве значений свойств, указанных параметром **lppPropArray.**</span><span class="sxs-lookup"><span data-stu-id="aaf95-112">**GetProps** indicates partial success by returning the warning MAPI_W_ERRORS_RETURNED and placing information about the unavailable properties in the property value array pointed to by the **lppPropArray** parameter.</span></span> <span data-ttu-id="aaf95-113">Запись недоступного свойства в этом массиве содержит PT_ERROR для типа свойства в члене **ulPropTag** и MAPI_E_NOT_FOUND или другое соответствующее значение ошибки для участника **Value.**</span><span class="sxs-lookup"><span data-stu-id="aaf95-113">An unavailable property's entry in this array contains PT_ERROR for the property type in the **ulPropTag** member and MAPI_E_NOT_FOUND or another appropriate error value for the **Value** member.</span></span> <span data-ttu-id="aaf95-114">Например, если клиент вызывает метод **GetProps** папки для получения трех свойств, а третий недоступен, поставщик магазина сообщений помещает PT_ERROR в третий тип свойства в массиве значений свойств и MAPI_E_NOT_FOUND в третьем значении свойства.</span><span class="sxs-lookup"><span data-stu-id="aaf95-114">For example, if a client calls a folder's **GetProps** method to retrieve three properties and the third is unavailable, the message store provider places PT_ERROR in the third property type in the property value array and MAPI_E_NOT_FOUND in the third property value.</span></span> 
  
<span data-ttu-id="aaf95-115">Другие методы **IMAPIProp** по-разному сообщают о частичном успехе.</span><span class="sxs-lookup"><span data-stu-id="aaf95-115">The other **IMAPIProp** methods report partial success differently.</span></span> <span data-ttu-id="aaf95-116">Эти методы сообщают о частичном успехе, возвращая S_OK и размещая сведения об ошибках в [структуре SPropProblemArray.](spropproblemarray.md)</span><span class="sxs-lookup"><span data-stu-id="aaf95-116">These methods report partial success by returning S_OK and placing error information in an [SPropProblemArray](spropproblemarray.md) structure.</span></span> <span data-ttu-id="aaf95-117">В отличие от массива значений свойств **в GetProps,** который содержит данные независимо от того, был ли метод успешным или неудачным, массив проблем свойств в этих методах существует только в том случае, если имеются ошибки и только в том случае, если вызываемая зарегистрировано заинтересованность в изучении ошибок.</span><span class="sxs-lookup"><span data-stu-id="aaf95-117">Unlike the property value array in **GetProps** that contains data regardless of whether the method succeeded or failed, the property problem array in these methods exists only if there are errors and only if the caller has registered interest in learning about the errors.</span></span> <span data-ttu-id="aaf95-118">Для регистрации сведений об ошибках звонителям необходимо указать допустимый указатель **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="aaf95-118">Callers must specify a valid **SPropProblemArray** pointer to register for error information.</span></span> 
  
<span data-ttu-id="aaf95-119">Когда значение ошибки возвращается из **SetProps,** **DeleteProps,** **CopyTo** или **CopyProps,** это указывает на сбой, а не частичный успех.</span><span class="sxs-lookup"><span data-stu-id="aaf95-119">When an error value is returned from **SetProps**, **DeleteProps**, **CopyTo**, or **CopyProps**, this indicates failure instead of partial success.</span></span> <span data-ttu-id="aaf95-120">Массив проблем свойств, если он доступен, не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="aaf95-120">The property problem array, if available, is not valid.</span></span> <span data-ttu-id="aaf95-121">Клиенты не должны пытаться получать доступ к данным, удерживаемой в структуре, и не должны пытаться освободить ее.</span><span class="sxs-lookup"><span data-stu-id="aaf95-121">Clients should not try to access data held in the structure nor should they try to free the structure itself.</span></span> <span data-ttu-id="aaf95-122">Соответствующий ответ — вызвать [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="aaf95-122">The appropriate response is to call [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span> 
  
<span data-ttu-id="aaf95-123">**GetLastError** аналогична функции с тем же именем, что и в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="aaf95-123">**GetLastError** is similar to the function of the same name provided in the Windows SDK.</span></span> <span data-ttu-id="aaf95-124">Оба предоставляют более подробные сведения об ошибке, чем доступно с возвратным значением.</span><span class="sxs-lookup"><span data-stu-id="aaf95-124">Both provide more detailed information about an error than is available with the return value.</span></span> <span data-ttu-id="aaf95-125">Они оба возвращают сведения о предыдущей ошибке, которая произошла.</span><span class="sxs-lookup"><span data-stu-id="aaf95-125">They both return information about the previous error that has occurred.</span></span> <span data-ttu-id="aaf95-126">Разница заключается в том, что функция **Win32 GetLastError** сообщает об ошибке, вызываемой потоком вызовов, а метод **IMAPIProp::GetLastError** сообщает об ошибке, порожденной текущим объектом.</span><span class="sxs-lookup"><span data-stu-id="aaf95-126">The difference is that the Win32 **GetLastError** function reports on an error generated by the calling thread and the **IMAPIProp::GetLastError** method reports on an error generated by the current object.</span></span> <span data-ttu-id="aaf95-127">То есть, если клиент вызывает **DeleteProps** в сообщении и возвращает MAPI_E_NO_ACCESS, чтобы указать, что сообщение только для чтения, **GetLastError** возвращает данные, предоставленные сообщением.</span><span class="sxs-lookup"><span data-stu-id="aaf95-127">That is, if a client calls **DeleteProps** on a message and MAPI_E_NO_ACCESS is returned to indicate that the message is read-only, **GetLastError** returns data provided by the message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aaf95-128">См. также</span><span class="sxs-lookup"><span data-stu-id="aaf95-128">See also</span></span>

- [<span data-ttu-id="aaf95-129">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="aaf95-129">MAPI Property Overview</span></span>](mapi-property-overview.md)

