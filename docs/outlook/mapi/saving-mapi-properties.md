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
ms.openlocfilehash: 6135dfae915a1e70743f9224352390c4b56ea02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812172"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="2cb69-103">Сохранение свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="2cb69-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="2cb69-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2cb69-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2cb69-105">Многие объекты поддержки модели транзакций обработки посредством изменения свойств не становятся постоянной до момента фиксации в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="2cb69-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="2cb69-106">В то время как изменения свойства обрабатываются с помощью методов [IMAPIProp::SetProps](imapiprop-setprops.md) и [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) , действие фиксации обрабатывается [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="2cb69-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="2cb69-107">Файл не является только после успешного вызова **SaveChanges** , что можно получить доступ к наиболее поздней версии для свойств объектов.</span><span class="sxs-lookup"><span data-stu-id="2cb69-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="2cb69-108">Когда **SaveChanges** возвращает значение ошибки MAPI_E_OBJECT_CHANGED, это предупреждение, что другой клиент одновременно внесением изменений на объект.</span><span class="sxs-lookup"><span data-stu-id="2cb69-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="2cb69-109">Возможно, в зависимости от поставщика, реализация объекта для нескольких клиентов, чтобы успешно откройте объект путем вызова метода **OpenEntry** с установленным флагом MAPI_MODIFY, предоставляя доступ на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="2cb69-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="2cb69-110">Объект, который возвращается из таких, что на вызов **OpenEntry** — моментальный снимок данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="2cb69-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="2cb69-111">Каждый повторная попытка изменить эти данные можно перезаписать Предыдущая попытка.</span><span class="sxs-lookup"><span data-stu-id="2cb69-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="2cb69-112">При получении MAPI_E_OBJECT_CHANGED от **SaveChanges**, клиент имеет возможность:</span><span class="sxs-lookup"><span data-stu-id="2cb69-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="2cb69-113">Создайте копию объекта для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="2cb69-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="2cb69-114">Сделайте другой вызов **SaveChanges**, определяющее FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="2cb69-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="2cb69-115">При вызове **SaveChanges** флаг FORCE_SAVE перезаписывает предыдущей сохранить и внесите необходимые изменения клиента было постоянным.</span><span class="sxs-lookup"><span data-stu-id="2cb69-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2cb69-116">См. также</span><span class="sxs-lookup"><span data-stu-id="2cb69-116">See also</span></span>



[<span data-ttu-id="2cb69-117">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="2cb69-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

