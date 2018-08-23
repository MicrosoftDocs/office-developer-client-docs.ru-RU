---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a397ac9110429911755552298ffe244343d54a8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583731"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="0f576-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0f576-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="0f576-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f576-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f576-105">Включает клиентов, поставщиков услуг и MAPI, для работы со свойствами.</span><span class="sxs-lookup"><span data-stu-id="0f576-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="0f576-106">Все объекты, которые поддерживают свойства реализовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0f576-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f576-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0f576-107">Header file:</span></span>  <br/> |<span data-ttu-id="0f576-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f576-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0f576-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="0f576-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="0f576-110">Объект не предоставляет этот интерфейс напрямую.</span><span class="sxs-lookup"><span data-stu-id="0f576-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="0f576-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="0f576-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="0f576-112">Поставщиков услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="0f576-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="0f576-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="0f576-113">Called by:</span></span>  <br/> |<span data-ttu-id="0f576-114">Клиентские приложения, поставщиков услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="0f576-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="0f576-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="0f576-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0f576-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0f576-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="0f576-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="0f576-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="0f576-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="0f576-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="0f576-119">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="0f576-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="0f576-120">Абстрактный класс, никогда не реализовано</span><span class="sxs-lookup"><span data-stu-id="0f576-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0f576-121">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="0f576-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0f576-122">GetLastError</span><span class="sxs-lookup"><span data-stu-id="0f576-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="0f576-123">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки.</span><span class="sxs-lookup"><span data-stu-id="0f576-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="0f576-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="0f576-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="0f576-125">Выполняет постоянное все изменения, внесенные в объект с момента последней операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="0f576-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="0f576-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="0f576-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="0f576-127">Получает значение свойства из одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="0f576-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="0f576-128">GetPropList</span><span class="sxs-lookup"><span data-stu-id="0f576-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="0f576-129">Возвращает свойство теги для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="0f576-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="0f576-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="0f576-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="0f576-131">Возвращает указатель на интерфейс, который можно использовать для доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="0f576-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="0f576-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="0f576-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="0f576-133">Обновление одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="0f576-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="0f576-134">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="0f576-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="0f576-135">Удаляет одно или несколько свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="0f576-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="0f576-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="0f576-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="0f576-137">Копирует или переносит все свойства, за исключением специально исключенные свойства.</span><span class="sxs-lookup"><span data-stu-id="0f576-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="0f576-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="0f576-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="0f576-139">Копирование или Перемещение выбранных свойств.</span><span class="sxs-lookup"><span data-stu-id="0f576-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="0f576-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="0f576-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="0f576-141">Содержит имена свойств, которые соответствуют один или несколько идентификаторов свойств.</span><span class="sxs-lookup"><span data-stu-id="0f576-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="0f576-142">GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="0f576-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="0f576-143">Предоставляет свойство идентификаторы, соответствующие имена одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="0f576-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f576-144">Замечания</span><span class="sxs-lookup"><span data-stu-id="0f576-144">Remarks</span></span>

 <span data-ttu-id="0f576-145">**IMAPIProp** — это основной интерфейс для следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="0f576-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="0f576-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="0f576-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="0f576-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="0f576-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="0f576-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0f576-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="0f576-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="0f576-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="0f576-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="0f576-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="0f576-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="0f576-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="0f576-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="0f576-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="0f576-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="0f576-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="0f576-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="0f576-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="0f576-155">См. также</span><span class="sxs-lookup"><span data-stu-id="0f576-155">See also</span></span>



[<span data-ttu-id="0f576-156">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="0f576-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

