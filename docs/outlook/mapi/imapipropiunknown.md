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
# <a name="imapiprop--iunknown"></a><span data-ttu-id="08c0d-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08c0d-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="08c0d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08c0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08c0d-105">Позволяет клиентам, поставщикам услуг и MAPI работать со свойствами.</span><span class="sxs-lookup"><span data-stu-id="08c0d-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="08c0d-106">Этот интерфейс реализуется всеми объектами, которые поддерживаются свойствами.</span><span class="sxs-lookup"><span data-stu-id="08c0d-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08c0d-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="08c0d-107">Header file:</span></span>  <br/> |<span data-ttu-id="08c0d-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="08c0d-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="08c0d-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="08c0d-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="08c0d-110">Ни один объект не предоставляет этот интерфейс напрямую.</span><span class="sxs-lookup"><span data-stu-id="08c0d-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="08c0d-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="08c0d-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="08c0d-112">Поставщики услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="08c0d-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="08c0d-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="08c0d-113">Called by:</span></span>  <br/> |<span data-ttu-id="08c0d-114">Клиентские приложения, поставщики служб и MAPI</span><span class="sxs-lookup"><span data-stu-id="08c0d-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="08c0d-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="08c0d-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="08c0d-116">Иид_имапипроп</span><span class="sxs-lookup"><span data-stu-id="08c0d-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="08c0d-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="08c0d-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="08c0d-118">ЛПМАПИПРОП</span><span class="sxs-lookup"><span data-stu-id="08c0d-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="08c0d-119">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="08c0d-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="08c0d-120">Абстрактный класс, никогда не реализован</span><span class="sxs-lookup"><span data-stu-id="08c0d-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="08c0d-121">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="08c0d-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="08c0d-122">GetLastError</span><span class="sxs-lookup"><span data-stu-id="08c0d-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="08c0d-123">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущем сообщении об ошибке.</span><span class="sxs-lookup"><span data-stu-id="08c0d-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="08c0d-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="08c0d-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="08c0d-125">Делает неизменными все изменения, внесенные в объект с момента последнего выполнения операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="08c0d-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="08c0d-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="08c0d-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="08c0d-127">Получает значение свойства одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="08c0d-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="08c0d-128">Жетпроплист</span><span class="sxs-lookup"><span data-stu-id="08c0d-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="08c0d-129">Возвращает теги свойств для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="08c0d-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="08c0d-130">Опенпроперти</span><span class="sxs-lookup"><span data-stu-id="08c0d-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="08c0d-131">Возвращает указатель на интерфейс, который можно использовать для доступа к свойству.</span><span class="sxs-lookup"><span data-stu-id="08c0d-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="08c0d-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="08c0d-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="08c0d-133">Обновляет одно или несколько свойств.</span><span class="sxs-lookup"><span data-stu-id="08c0d-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="08c0d-134">Делетепропс</span><span class="sxs-lookup"><span data-stu-id="08c0d-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="08c0d-135">Удаляет одно или несколько свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="08c0d-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="08c0d-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="08c0d-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="08c0d-137">Копирует или перемещает все свойства, кроме специально исключенных свойств.</span><span class="sxs-lookup"><span data-stu-id="08c0d-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="08c0d-138">Копипропс</span><span class="sxs-lookup"><span data-stu-id="08c0d-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="08c0d-139">Копирование или перемещение выбранных свойств.</span><span class="sxs-lookup"><span data-stu-id="08c0d-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="08c0d-140">Жетнамесфромидс</span><span class="sxs-lookup"><span data-stu-id="08c0d-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="08c0d-141">Предоставляет имена свойств, которые соответствуют одному или нескольким идентификаторам свойств.</span><span class="sxs-lookup"><span data-stu-id="08c0d-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="08c0d-142">Жетидсфромнамес</span><span class="sxs-lookup"><span data-stu-id="08c0d-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="08c0d-143">Предоставляет идентификаторы свойств, соответствующие одному или нескольким именам свойств.</span><span class="sxs-lookup"><span data-stu-id="08c0d-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08c0d-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="08c0d-144">Remarks</span></span>

 <span data-ttu-id="08c0d-145">**IMAPIProp** является базовым интерфейсом для следующих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="08c0d-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="08c0d-146">Иаттач</span><span class="sxs-lookup"><span data-stu-id="08c0d-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="08c0d-147">Имаилусер</span><span class="sxs-lookup"><span data-stu-id="08c0d-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="08c0d-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="08c0d-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="08c0d-149">Имапиформинфо</span><span class="sxs-lookup"><span data-stu-id="08c0d-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="08c0d-150">Имапистатус</span><span class="sxs-lookup"><span data-stu-id="08c0d-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="08c0d-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="08c0d-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="08c0d-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="08c0d-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="08c0d-153">Ипрофсект</span><span class="sxs-lookup"><span data-stu-id="08c0d-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="08c0d-154">Ипропдата</span><span class="sxs-lookup"><span data-stu-id="08c0d-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="08c0d-155">См. также</span><span class="sxs-lookup"><span data-stu-id="08c0d-155">See also</span></span>



[<span data-ttu-id="08c0d-156">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="08c0d-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

