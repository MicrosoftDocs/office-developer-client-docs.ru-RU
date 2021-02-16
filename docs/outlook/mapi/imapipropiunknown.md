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
ms.openlocfilehash: 6b0a8923ee5efe22584170ce9853698885527ee8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407664"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="ca206-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca206-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="ca206-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca206-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca206-105">Позволяет клиентам, поставщикам услуг и MAPI работать со свойствами.</span><span class="sxs-lookup"><span data-stu-id="ca206-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="ca206-106">Этот интерфейс реализован всеми объектами, которые поддерживают свойства.</span><span class="sxs-lookup"><span data-stu-id="ca206-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca206-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ca206-107">Header file:</span></span>  <br/> |<span data-ttu-id="ca206-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca206-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ca206-109">Выставим:</span><span class="sxs-lookup"><span data-stu-id="ca206-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="ca206-110">Ни один объект не предоставляет этот интерфейс напрямую.</span><span class="sxs-lookup"><span data-stu-id="ca206-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="ca206-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ca206-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ca206-112">Поставщики услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="ca206-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="ca206-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ca206-113">Called by:</span></span>  <br/> |<span data-ttu-id="ca206-114">Клиентские приложения, поставщики услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="ca206-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="ca206-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="ca206-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ca206-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ca206-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="ca206-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="ca206-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="ca206-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="ca206-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="ca206-119">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="ca206-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="ca206-120">Абстрактный класс, никогда не реализованный</span><span class="sxs-lookup"><span data-stu-id="ca206-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ca206-121">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="ca206-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ca206-122">GetLastError</span><span class="sxs-lookup"><span data-stu-id="ca206-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="ca206-123">Возвращает структуру [MAPIERROR,](mapierror.md) которая содержит сведения о предыдущей ошибке.</span><span class="sxs-lookup"><span data-stu-id="ca206-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="ca206-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="ca206-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="ca206-125">Вносит постоянные изменения, внесенные в объект с момента последней операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="ca206-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="ca206-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="ca206-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="ca206-127">Извлекает значение свойства одного или более свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="ca206-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="ca206-128">GetPropList</span><span class="sxs-lookup"><span data-stu-id="ca206-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="ca206-129">Возвращает теги свойств для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="ca206-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="ca206-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="ca206-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="ca206-131">Возвращает указатель на интерфейс, который можно использовать для доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="ca206-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="ca206-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="ca206-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="ca206-133">Обновляет одно или несколько свойств.</span><span class="sxs-lookup"><span data-stu-id="ca206-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="ca206-134">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="ca206-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="ca206-135">Удаляет одно или несколько свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="ca206-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="ca206-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="ca206-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="ca206-137">Копирует или перемещает все свойства, кроме специально исключенных.</span><span class="sxs-lookup"><span data-stu-id="ca206-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="ca206-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="ca206-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="ca206-139">Копирует или перемещает выбранные свойства.</span><span class="sxs-lookup"><span data-stu-id="ca206-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="ca206-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="ca206-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="ca206-141">Предоставляет имена свойств, соответствующие одному или более идентификаторам свойств.</span><span class="sxs-lookup"><span data-stu-id="ca206-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="ca206-142">GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="ca206-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="ca206-143">Предоставляет идентификаторы свойств, соответствующие одному или более именам свойств.</span><span class="sxs-lookup"><span data-stu-id="ca206-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca206-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca206-144">Remarks</span></span>

 <span data-ttu-id="ca206-145">**IMAPIProp —** это базовый интерфейс для следующих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="ca206-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="ca206-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="ca206-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="ca206-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="ca206-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="ca206-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ca206-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="ca206-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="ca206-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="ca206-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="ca206-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="ca206-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="ca206-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="ca206-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="ca206-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="ca206-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="ca206-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="ca206-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="ca206-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="ca206-155">См. также</span><span class="sxs-lookup"><span data-stu-id="ca206-155">See also</span></span>



[<span data-ttu-id="ca206-156">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="ca206-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

