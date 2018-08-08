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
ms.openlocfilehash: 02d2b136ed1437ba53ce1e54a202d70a48b2abe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809050"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="d3ee8-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d3ee8-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="d3ee8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3ee8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3ee8-105">Включает клиентов, поставщиков услуг и MAPI, для работы со свойствами.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="d3ee8-106">Все объекты, которые поддерживают свойства реализовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d3ee8-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d3ee8-107">Header file:</span></span>  <br/> |<span data-ttu-id="d3ee8-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3ee8-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d3ee8-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="d3ee8-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="d3ee8-110">Объект не предоставляет этот интерфейс напрямую.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="d3ee8-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="d3ee8-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="d3ee8-112">Поставщиков услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="d3ee8-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="d3ee8-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="d3ee8-113">Called by:</span></span>  <br/> |<span data-ttu-id="d3ee8-114">Клиентские приложения, поставщиков услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="d3ee8-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="d3ee8-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="d3ee8-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d3ee8-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d3ee8-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="d3ee8-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="d3ee8-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="d3ee8-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="d3ee8-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="d3ee8-119">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="d3ee8-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="d3ee8-120">Абстрактный класс, никогда не реализовано</span><span class="sxs-lookup"><span data-stu-id="d3ee8-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d3ee8-121">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="d3ee8-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d3ee8-122">GetLastError</span><span class="sxs-lookup"><span data-stu-id="d3ee8-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="d3ee8-123">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="d3ee8-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="d3ee8-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="d3ee8-125">Выполняет постоянное все изменения, внесенные в объект с момента последней операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="d3ee8-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="d3ee8-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="d3ee8-127">Получает значение свойства из одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="d3ee8-128">GetPropList</span><span class="sxs-lookup"><span data-stu-id="d3ee8-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="d3ee8-129">Возвращает свойство теги для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="d3ee8-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="d3ee8-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="d3ee8-131">Возвращает указатель на интерфейс, который можно использовать для доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="d3ee8-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="d3ee8-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="d3ee8-133">Обновление одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="d3ee8-134">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="d3ee8-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="d3ee8-135">Удаляет одно или несколько свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="d3ee8-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="d3ee8-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="d3ee8-137">Копирует или переносит все свойства, за исключением специально исключенные свойства.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="d3ee8-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="d3ee8-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="d3ee8-139">Копирование или Перемещение выбранных свойств.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="d3ee8-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="d3ee8-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="d3ee8-141">Содержит имена свойств, которые соответствуют один или несколько идентификаторов свойств.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="d3ee8-142">GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="d3ee8-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="d3ee8-143">Предоставляет свойство идентификаторы, соответствующие имена одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="d3ee8-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3ee8-144">Замечания</span><span class="sxs-lookup"><span data-stu-id="d3ee8-144">Remarks</span></span>

 <span data-ttu-id="d3ee8-145">**IMAPIProp** — это основной интерфейс для следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="d3ee8-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="d3ee8-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="d3ee8-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="d3ee8-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="d3ee8-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="d3ee8-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d3ee8-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="d3ee8-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="d3ee8-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="d3ee8-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="d3ee8-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="d3ee8-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="d3ee8-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="d3ee8-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="d3ee8-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="d3ee8-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="d3ee8-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="d3ee8-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="d3ee8-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="d3ee8-155">См. также</span><span class="sxs-lookup"><span data-stu-id="d3ee8-155">See also</span></span>



[<span data-ttu-id="d3ee8-156">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="d3ee8-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

