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
ms.openlocfilehash: 66e318c3b7b772f2713b5c730590ce4a8ad5965b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808764"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="a3a34-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a3a34-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="a3a34-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3a34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3a34-105">Поддерживает и предоставляет доступ к свойствам вложений в сообщениях.</span><span class="sxs-lookup"><span data-stu-id="a3a34-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="a3a34-106">Интерфейс **IAttach** не имеет уникальное методов свои собственные.</span><span class="sxs-lookup"><span data-stu-id="a3a34-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="a3a34-107">Дополнительные сведения об использовании вложения можно [Вложений MAPI](mapi-attachments.md) и [Таблиц вложений](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a3a34-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3a34-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a3a34-108">Header file:</span></span>  <br/> |<span data-ttu-id="a3a34-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3a34-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a3a34-110">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="a3a34-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="a3a34-111">Объекты вложения</span><span class="sxs-lookup"><span data-stu-id="a3a34-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="a3a34-112">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="a3a34-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3a34-113">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="a3a34-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="a3a34-114">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="a3a34-114">Called by:</span></span>  <br/> |<span data-ttu-id="a3a34-115">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="a3a34-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="a3a34-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="a3a34-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a3a34-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="a3a34-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="a3a34-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="a3a34-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="a3a34-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="a3a34-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="a3a34-120">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="a3a34-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="a3a34-121">В транзакции</span><span class="sxs-lookup"><span data-stu-id="a3a34-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a3a34-122">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="a3a34-122">Vtable order</span></span>

<span data-ttu-id="a3a34-123">Этот интерфейс не имеет каких-либо уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="a3a34-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="a3a34-124">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="a3a34-124">**Required properties**</span></span>|<span data-ttu-id="a3a34-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="a3a34-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3a34-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3a34-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3a34-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a3a34-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="a3a34-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3a34-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3a34-129">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a3a34-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="a3a34-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3a34-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3a34-131">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a3a34-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3a34-132">См. также</span><span class="sxs-lookup"><span data-stu-id="a3a34-132">See also</span></span>



[<span data-ttu-id="a3a34-133">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="a3a34-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

