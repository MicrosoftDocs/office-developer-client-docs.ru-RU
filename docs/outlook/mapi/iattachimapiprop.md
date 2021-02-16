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
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409092"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="8843c-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8843c-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="8843c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8843c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8843c-105">Поддерживает и предоставляет доступ к свойствам вложений в сообщениях.</span><span class="sxs-lookup"><span data-stu-id="8843c-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="8843c-106">Интерфейс **IAttach** не имеет собственных уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="8843c-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="8843c-107">Дополнительные сведения об использовании вложений см. в таблицах вложений и [вложений](attachment-tables.md) [MAPI.](mapi-attachments.md)</span><span class="sxs-lookup"><span data-stu-id="8843c-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8843c-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8843c-108">Header file:</span></span>  <br/> |<span data-ttu-id="8843c-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8843c-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8843c-110">Выставим:</span><span class="sxs-lookup"><span data-stu-id="8843c-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="8843c-111">Объекты вложений</span><span class="sxs-lookup"><span data-stu-id="8843c-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="8843c-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8843c-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="8843c-113">Поставщики store сообщений</span><span class="sxs-lookup"><span data-stu-id="8843c-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="8843c-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8843c-114">Called by:</span></span>  <br/> |<span data-ttu-id="8843c-115">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="8843c-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="8843c-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="8843c-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8843c-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="8843c-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="8843c-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="8843c-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="8843c-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="8843c-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="8843c-120">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="8843c-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="8843c-121">Transacted</span><span class="sxs-lookup"><span data-stu-id="8843c-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8843c-122">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="8843c-122">Vtable order</span></span>

<span data-ttu-id="8843c-123">Этот интерфейс не имеет уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="8843c-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="8843c-124">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="8843c-124">**Required properties**</span></span>|<span data-ttu-id="8843c-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="8843c-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8843c-126">**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8843c-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8843c-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="8843c-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="8843c-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod)](pidtagattachmethod-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8843c-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8843c-129">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8843c-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="8843c-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8843c-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8843c-131">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8843c-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8843c-132">См. также</span><span class="sxs-lookup"><span data-stu-id="8843c-132">See also</span></span>



[<span data-ttu-id="8843c-133">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="8843c-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

