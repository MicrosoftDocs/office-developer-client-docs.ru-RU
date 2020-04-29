---
title: Сохранение свойств MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425892"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="cc344-103">Сохранение свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="cc344-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="cc344-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc344-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc344-105">Многие объекты поддерживают модель транзакции обработки, в результате которой изменения свойств не будут выполняться до тех пор, пока они не будут зафиксированы позже.</span><span class="sxs-lookup"><span data-stu-id="cc344-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="cc344-106">В то время как изменения свойств обрабатываются с помощью методов [IMAPIProp:: SetProps](imapiprop-setprops.md) и [IMAPIProp::D елетепропс](imapiprop-deleteprops.md) , то этап фиксации обрабатывается [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="cc344-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="cc344-107">Он не будет выполняться до тех пор, пока не будет успешно вызвано **, что можно получить доступ к последней** версии свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="cc344-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="cc344-108">Когда **SaveChanges** возвращает значение ошибки MAPI_E_OBJECT_CHANGED, это предупреждение о том, что другой клиент одновременно фиксирует изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="cc344-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="cc344-109">В зависимости от поставщика, реализующего объект, для нескольких клиентов можно успешно открыть объект, вызвав его метод **OpenEntry** с установленным флагом MAPI_MODIFY, предоставив доступ для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="cc344-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="cc344-110">Объект, возвращаемый из такого вызова **OpenEntry** , является моментальным снимком данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="cc344-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="cc344-111">При каждой последующей попытке изменить эти данные можно перезаписать предыдущую попытку.</span><span class="sxs-lookup"><span data-stu-id="cc344-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="cc344-112">При получении MAPI_E_OBJECT_CHANGED от **SaveChanges**клиент может выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="cc344-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="cc344-113">Сделайте копию объекта, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="cc344-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="cc344-114">Выполните еще один вызов **SaveChanges**, указав FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="cc344-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="cc344-115">При вызове метода **SaveChanges** с помощью флага FORCE_SAVE перезаписывается предыдущее сохранение и вносятся изменения клиента.</span><span class="sxs-lookup"><span data-stu-id="cc344-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc344-116">См. также</span><span class="sxs-lookup"><span data-stu-id="cc344-116">See also</span></span>



[<span data-ttu-id="cc344-117">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="cc344-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

