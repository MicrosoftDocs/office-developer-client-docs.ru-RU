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
# <a name="saving-mapi-properties"></a><span data-ttu-id="ff9d7-103">Сохранение свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="ff9d7-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="ff9d7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff9d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff9d7-105">Многие объекты поддерживают модель транзакций обработки, при которой изменения свойств не будут постоянны, пока не будут зафиксированы позже.</span><span class="sxs-lookup"><span data-stu-id="ff9d7-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="ff9d7-106">В то время как изменения свойств обрабатываются методами [IMAPIProp::SetProps](imapiprop-setprops.md) и [IMAPIProp::D eleteProps,](imapiprop-deleteprops.md) этап фиксации обрабатывается [методом IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="ff9d7-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="ff9d7-107">Доступ к последней версии свойств объекта можно получить только после успешного вызова **SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="ff9d7-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="ff9d7-108">Когда **SaveChanges** возвращает значение ошибки MAPI_E_OBJECT_CHANGED, это предупреждение о том, что другой клиент одновременно внося изменения в объект.</span><span class="sxs-lookup"><span data-stu-id="ff9d7-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="ff9d7-109">В зависимости от поставщика, реализующих объект, несколько клиентов могут успешно открыть объект, вызывая его метод **OpenEntry** с установленным флагом MAPI_MODIFY, предоставляя им доступ для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ff9d7-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="ff9d7-110">Объект, который возвращается из такого вызова **OpenEntry,** является моментальный снимок данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="ff9d7-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="ff9d7-111">Каждая последующие попытки изменить эти данные могут переписать предыдущую попытку.</span><span class="sxs-lookup"><span data-stu-id="ff9d7-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="ff9d7-112">Получив MAPI_E_OBJECT_CHANGED из **SaveChanges,** клиент может:</span><span class="sxs-lookup"><span data-stu-id="ff9d7-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="ff9d7-113">Сделайте копию объекта для удержания изменений.</span><span class="sxs-lookup"><span data-stu-id="ff9d7-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="ff9d7-114">Еще раз вызовите **SaveChanges,** указав FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="ff9d7-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="ff9d7-115">Вызов **SaveChanges** с флагом FORCE_SAVE переоценит предыдущее сохранение и сделает изменения клиента постоянными.</span><span class="sxs-lookup"><span data-stu-id="ff9d7-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff9d7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="ff9d7-116">See also</span></span>



[<span data-ttu-id="ff9d7-117">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="ff9d7-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

