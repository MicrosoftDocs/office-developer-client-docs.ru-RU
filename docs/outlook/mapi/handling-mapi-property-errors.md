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
# <a name="handling-mapi-property-errors"></a><span data-ttu-id="5146d-103">Обработка ошибок свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="5146d-103">Handling MAPI property errors</span></span>

<span data-ttu-id="5146d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5146d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5146d-105">Вместо полного сбоя или успеха следующие методы **IMAPIProp** отменяют частичный успех:</span><span class="sxs-lookup"><span data-stu-id="5146d-105">Instead of complete failure or success, the following **IMAPIProp** methods report partial success:</span></span> 
  
[<span data-ttu-id="5146d-106">GetProps</span><span class="sxs-lookup"><span data-stu-id="5146d-106">GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="5146d-107">SetProps</span><span class="sxs-lookup"><span data-stu-id="5146d-107">SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="5146d-108">Делетепропс</span><span class="sxs-lookup"><span data-stu-id="5146d-108">DeleteProps</span></span>](imapiprop-deleteprops.md)
  
[<span data-ttu-id="5146d-109">CopyTo</span><span class="sxs-lookup"><span data-stu-id="5146d-109">CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="5146d-110">Копипропс</span><span class="sxs-lookup"><span data-stu-id="5146d-110">CopyProps</span></span>](imapiprop-copyprops.md)
  
<span data-ttu-id="5146d-111">\*\*\*\* При получении по крайней мере одного из запрошенных свойств объекта PROPS сообщает о частичном успехе.</span><span class="sxs-lookup"><span data-stu-id="5146d-111">**GetProps** reports partial success when it can retrieve at least one of the requested properties for an object.</span></span> <span data-ttu-id="5146d-112">**PROPS** указывает на частичный успех, возвращая предупреждение мапи_в_еррорс_ретурнед и помещая сведения о недоступных свойствах в массиве значений свойств, на который указывает параметр **лпппропаррай** .</span><span class="sxs-lookup"><span data-stu-id="5146d-112">**GetProps** indicates partial success by returning the warning MAPI_W_ERRORS_RETURNED and placing information about the unavailable properties in the property value array pointed to by the **lppPropArray** parameter.</span></span> <span data-ttu-id="5146d-113">Запись недоступного свойства в этом массиве содержит ПТ_ЕРРОР для типа свойства в элементе **улпроптаг** и мапи_е_нот_фаунд или другое подходящее значение ошибки для элемента **value** .</span><span class="sxs-lookup"><span data-stu-id="5146d-113">An unavailable property's entry in this array contains PT_ERROR for the property type in the **ulPropTag** member and MAPI_E_NOT_FOUND or another appropriate error value for the **Value** member.</span></span> <span data-ttu-id="5146d-114">Например, если клиент вызывает метод PROPS папки для \*\*\*\* получения трех свойств, а третья недоступна, то поставщик хранилища сообщений помещает пт_еррор в третий тип свойства в массиве значений свойства и мапи_е_нот_фаунд в третьем значение свойства.</span><span class="sxs-lookup"><span data-stu-id="5146d-114">For example, if a client calls a folder's **GetProps** method to retrieve three properties and the third is unavailable, the message store provider places PT_ERROR in the third property type in the property value array and MAPI_E_NOT_FOUND in the third property value.</span></span> 
  
<span data-ttu-id="5146d-115">Другие методы **IMAPIProp** по-разному сообщают о частичном успехе.</span><span class="sxs-lookup"><span data-stu-id="5146d-115">The other **IMAPIProp** methods report partial success differently.</span></span> <span data-ttu-id="5146d-116">Эти методы отменяют частичный успех, возвращая значение S_OK и помещают сведения об ошибке в структуру [спроппроблемаррай](spropproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="5146d-116">These methods report partial success by returning S_OK and placing error information in an [SPropProblemArray](spropproblemarray.md) structure.</span></span> <span data-ttu-id="5146d-117">В отличие от массива значений свойства в \*\*\*\* свойствах Props, которые содержат данные независимо от того, успешно ли выполнен метод или произошел сбой, массив ошибок свойств в этих методах существует только в том случае, если у вызывающего абонента есть зарегистрированный процент обучения ошибки.</span><span class="sxs-lookup"><span data-stu-id="5146d-117">Unlike the property value array in **GetProps** that contains data regardless of whether the method succeeded or failed, the property problem array in these methods exists only if there are errors and only if the caller has registered interest in learning about the errors.</span></span> <span data-ttu-id="5146d-118">Абоненты должны указать допустимый указатель **спроппроблемаррай** для регистрации сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5146d-118">Callers must specify a valid **SPropProblemArray** pointer to register for error information.</span></span> 
  
<span data-ttu-id="5146d-119">Когда значение ошибки возвращается из **SetProps**, **делетепропс**, **CopyTo**или **копипропс**, это указывает на ошибку, а не на частичное успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="5146d-119">When an error value is returned from **SetProps**, **DeleteProps**, **CopyTo**, or **CopyProps**, this indicates failure instead of partial success.</span></span> <span data-ttu-id="5146d-120">Недопустимый массив проблем свойств, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="5146d-120">The property problem array, if available, is not valid.</span></span> <span data-ttu-id="5146d-121">Клиенты не должны пытаться получить доступ к данным, удерживаемым в структуре, и не должны пытаться освободить структуру.</span><span class="sxs-lookup"><span data-stu-id="5146d-121">Clients should not try to access data held in the structure nor should they try to free the structure itself.</span></span> <span data-ttu-id="5146d-122">Соответствующий ответ заключается в вызове [IMAPIProp:: GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="5146d-122">The appropriate response is to call [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span> 
  
<span data-ttu-id="5146d-123">**GetLastError** похожа на функцию с тем же именем, что и в пакете SDK для Windows.</span><span class="sxs-lookup"><span data-stu-id="5146d-123">**GetLastError** is similar to the function of the same name provided in the Windows SDK.</span></span> <span data-ttu-id="5146d-124">Оба предоставляют более подробные сведения об ошибке, чем доступ к возвращаемому значению.</span><span class="sxs-lookup"><span data-stu-id="5146d-124">Both provide more detailed information about an error than is available with the return value.</span></span> <span data-ttu-id="5146d-125">Они оба возвращают сведения о предыдущей произошедшей ошибке.</span><span class="sxs-lookup"><span data-stu-id="5146d-125">They both return information about the previous error that has occurred.</span></span> <span data-ttu-id="5146d-126">Разница заключается в том, что функция **GetLastError** Win32 сообщает об ошибке, созданной вызывающим потоком, и метод **IMAPIProp:: GetLastError** сообщает об ошибке, созданной текущим объектом.</span><span class="sxs-lookup"><span data-stu-id="5146d-126">The difference is that the Win32 **GetLastError** function reports on an error generated by the calling thread and the **IMAPIProp::GetLastError** method reports on an error generated by the current object.</span></span> <span data-ttu-id="5146d-127">То есть, если клиент вызывает **делетепропс** для сообщения и возвращается мапи_е_но_акцесс, чтобы указать, что сообщение доступно только для чтения, то функция **GetLastError** возвращает данные, предоставляемые сообщением.</span><span class="sxs-lookup"><span data-stu-id="5146d-127">That is, if a client calls **DeleteProps** on a message and MAPI_E_NO_ACCESS is returned to indicate that the message is read-only, **GetLastError** returns data provided by the message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5146d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="5146d-128">See also</span></span>

- [<span data-ttu-id="5146d-129">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="5146d-129">MAPI Property Overview</span></span>](mapi-property-overview.md)

