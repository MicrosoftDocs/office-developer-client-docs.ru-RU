---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ce9c8b189991e4102fcc9d17b88747d4ce55efec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570914"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="5ff7e-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5ff7e-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="5ff7e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ff7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ff7e-105">Поддерживает и предоставляет доступ к свойствам вложений в сообщениях.</span><span class="sxs-lookup"><span data-stu-id="5ff7e-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="5ff7e-106">Интерфейс **IAttach** не имеет уникальное методов свои собственные.</span><span class="sxs-lookup"><span data-stu-id="5ff7e-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="5ff7e-107">Дополнительные сведения об использовании вложения можно [Вложений MAPI](mapi-attachments.md) и [Таблиц вложений](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5ff7e-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ff7e-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5ff7e-108">Header file:</span></span>  <br/> |<span data-ttu-id="5ff7e-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ff7e-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5ff7e-110">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="5ff7e-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="5ff7e-111">Объекты вложения</span><span class="sxs-lookup"><span data-stu-id="5ff7e-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="5ff7e-112">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="5ff7e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="5ff7e-113">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="5ff7e-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="5ff7e-114">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="5ff7e-114">Called by:</span></span>  <br/> |<span data-ttu-id="5ff7e-115">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="5ff7e-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="5ff7e-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="5ff7e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5ff7e-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="5ff7e-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="5ff7e-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="5ff7e-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="5ff7e-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="5ff7e-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="5ff7e-120">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="5ff7e-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="5ff7e-121">В транзакции</span><span class="sxs-lookup"><span data-stu-id="5ff7e-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5ff7e-122">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="5ff7e-122">Vtable order</span></span>

<span data-ttu-id="5ff7e-123">Этот интерфейс не имеет каких-либо уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="5ff7e-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="5ff7e-124">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="5ff7e-124">**Required properties**</span></span>|<span data-ttu-id="5ff7e-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="5ff7e-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ff7e-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ff7e-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ff7e-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5ff7e-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="5ff7e-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ff7e-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ff7e-129">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5ff7e-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="5ff7e-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5ff7e-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5ff7e-131">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5ff7e-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5ff7e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="5ff7e-132">See also</span></span>



[<span data-ttu-id="5ff7e-133">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="5ff7e-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

