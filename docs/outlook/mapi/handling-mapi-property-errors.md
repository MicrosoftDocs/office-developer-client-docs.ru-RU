---
title: Обработка ошибок свойство MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 82f37e2a6f6834c7a8553a3d9d364f7e657d81da
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579510"
---
# <a name="handling-mapi-property-errors"></a><span data-ttu-id="eb87e-103">Обработка ошибок свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="eb87e-103">Handling MAPI property errors</span></span>

<span data-ttu-id="eb87e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb87e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb87e-105">Вместо завершения сбоя или успеха следующие методы **IMAPIProp** сообщить о частичном успехе:</span><span class="sxs-lookup"><span data-stu-id="eb87e-105">Instead of complete failure or success, the following **IMAPIProp** methods report partial success:</span></span> 
  
[<span data-ttu-id="eb87e-106">GetProps</span><span class="sxs-lookup"><span data-stu-id="eb87e-106">GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="eb87e-107">SetProps</span><span class="sxs-lookup"><span data-stu-id="eb87e-107">SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="eb87e-108">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="eb87e-108">DeleteProps</span></span>](imapiprop-deleteprops.md)
  
[<span data-ttu-id="eb87e-109">CopyTo</span><span class="sxs-lookup"><span data-stu-id="eb87e-109">CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="eb87e-110">CopyProps</span><span class="sxs-lookup"><span data-stu-id="eb87e-110">CopyProps</span></span>](imapiprop-copyprops.md)
  
<span data-ttu-id="eb87e-111">**GetProps** отчетов частичного успеха при его можно получить по крайней мере один из запрошенного свойства для объекта.</span><span class="sxs-lookup"><span data-stu-id="eb87e-111">**GetProps** reports partial success when it can retrieve at least one of the requested properties for an object.</span></span> <span data-ttu-id="eb87e-112">**GetProps** указывает частичный успех возвращение предупреждение MAPI_W_ERRORS_RETURNED и поместить сведения о свойствах, недоступны в массиве значение свойства указывает параметр **lppPropArray** .</span><span class="sxs-lookup"><span data-stu-id="eb87e-112">**GetProps** indicates partial success by returning the warning MAPI_W_ERRORS_RETURNED and placing information about the unavailable properties in the property value array pointed to by the **lppPropArray** parameter.</span></span> <span data-ttu-id="eb87e-113">Запись недоступна свойство в этот массив содержит PT_ERROR тип свойства в элемент **ulPropTag** и MAPI_E_NOT_FOUND или другой соответствующего значения ошибки для элемента **значение** .</span><span class="sxs-lookup"><span data-stu-id="eb87e-113">An unavailable property's entry in this array contains PT_ERROR for the property type in the **ulPropTag** member and MAPI_E_NOT_FOUND or another appropriate error value for the **Value** member.</span></span> <span data-ttu-id="eb87e-114">Например если клиент вызывает метод **GetProps** папки для извлечения три свойства и третий недоступна, поставщика хранилища сообщений помещает PT_ERROR в третий тип свойства в массив значений свойств и MAPI_E_NOT_FOUND в третьей значение свойства.</span><span class="sxs-lookup"><span data-stu-id="eb87e-114">For example, if a client calls a folder's **GetProps** method to retrieve three properties and the third is unavailable, the message store provider places PT_ERROR in the third property type in the property value array and MAPI_E_NOT_FOUND in the third property value.</span></span> 
  
<span data-ttu-id="eb87e-115">Другие методы **IMAPIProp** о частичном успехе по-разному.</span><span class="sxs-lookup"><span data-stu-id="eb87e-115">The other **IMAPIProp** methods report partial success differently.</span></span> <span data-ttu-id="eb87e-116">Эти методы о частичного успеха возвращает значение S_OK и поместить сведения об ошибке в структуре [SPropProblemArray](spropproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="eb87e-116">These methods report partial success by returning S_OK and placing error information in an [SPropProblemArray](spropproblemarray.md) structure.</span></span> <span data-ttu-id="eb87e-117">В отличие от массива значение свойства в **GetProps** , который содержит данные, независимо от того, как метод выполнен успешно, так и не удалось, свойство массива проблемы в эти методы существует только в случае обнаружения ошибок и только в том случае, если вызывающий объект имеет зарегистрированных заинтересованность в общие сведения о ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb87e-117">Unlike the property value array in **GetProps** that contains data regardless of whether the method succeeded or failed, the property problem array in these methods exists only if there are errors and only if the caller has registered interest in learning about the errors.</span></span> <span data-ttu-id="eb87e-118">Вызывающие необходимо указать допустимое указатель **SPropProblemArray** регистрировать сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="eb87e-118">Callers must specify a valid **SPropProblemArray** pointer to register for error information.</span></span> 
  
<span data-ttu-id="eb87e-119">Если возвращает код ошибки **SetProps**, **DeleteProps**, **CopyTo**или **CopyProps**, это значит, сбоя вместо частичный успех.</span><span class="sxs-lookup"><span data-stu-id="eb87e-119">When an error value is returned from **SetProps**, **DeleteProps**, **CopyTo**, or **CopyProps**, this indicates failure instead of partial success.</span></span> <span data-ttu-id="eb87e-120">Проблема массива свойства, если он доступен, недействительны.</span><span class="sxs-lookup"><span data-stu-id="eb87e-120">The property problem array, if available, is not valid.</span></span> <span data-ttu-id="eb87e-121">Клиенты не рекомендуется для доступа к данным, которые проводятся в структуре, а также они должны пытаться освободить самой структуре.</span><span class="sxs-lookup"><span data-stu-id="eb87e-121">Clients should not try to access data held in the structure nor should they try to free the structure itself.</span></span> <span data-ttu-id="eb87e-122">Соответствующий ответ — вызов [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="eb87e-122">The appropriate response is to call [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span> 
  
<span data-ttu-id="eb87e-123">**GetLastError** аналогична функции с таким же именем, входящий в пакет SDK для Windows.</span><span class="sxs-lookup"><span data-stu-id="eb87e-123">**GetLastError** is similar to the function of the same name provided in the Windows SDK.</span></span> <span data-ttu-id="eb87e-124">Оба предоставляют более подробные сведения об ошибке не возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="eb87e-124">Both provide more detailed information about an error than is available with the return value.</span></span> <span data-ttu-id="eb87e-125">Обе они возвращают сведения о предыдущем произошедшей ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb87e-125">They both return information about the previous error that has occurred.</span></span> <span data-ttu-id="eb87e-126">Разница в том, что функция Win32 **GetLastError** отчетов об ошибках, вызывающий поток, а метод **IMAPIProp::GetLastError** отчетов об ошибках для текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="eb87e-126">The difference is that the Win32 **GetLastError** function reports on an error generated by the calling thread and the **IMAPIProp::GetLastError** method reports on an error generated by the current object.</span></span> <span data-ttu-id="eb87e-127">То есть если клиент вызывает **DeleteProps** на сообщение и MAPI_E_NO_ACCESS возвращается указать, что сообщение доступно только для чтения, **код последней ошибки** возвращается данные, предоставляемые сообщения.</span><span class="sxs-lookup"><span data-stu-id="eb87e-127">That is, if a client calls **DeleteProps** on a message and MAPI_E_NO_ACCESS is returned to indicate that the message is read-only, **GetLastError** returns data provided by the message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb87e-128">См. также</span><span class="sxs-lookup"><span data-stu-id="eb87e-128">See also</span></span>

- [<span data-ttu-id="eb87e-129">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="eb87e-129">MAPI Property Overview</span></span>](mapi-property-overview.md)

