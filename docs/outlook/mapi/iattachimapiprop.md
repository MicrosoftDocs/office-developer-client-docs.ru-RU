---
title: Иаттач IMAPIProp
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341624"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="e5b81-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e5b81-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="e5b81-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5b81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5b81-105">Поддерживает и предоставляет доступ к свойствам вложений в сообщениях.</span><span class="sxs-lookup"><span data-stu-id="e5b81-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="e5b81-106">Интерфейс **иаттач** не обладает уникальными методами.</span><span class="sxs-lookup"><span data-stu-id="e5b81-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="e5b81-107">Более подробную информацию об использовании вложений можно узнать в статье [вложения MAPI](mapi-attachments.md) и [таблицы вложений](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e5b81-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5b81-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e5b81-108">Header file:</span></span>  <br/> |<span data-ttu-id="e5b81-109">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e5b81-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e5b81-110">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="e5b81-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="e5b81-111">Объекты вложений</span><span class="sxs-lookup"><span data-stu-id="e5b81-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="e5b81-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e5b81-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="e5b81-113">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="e5b81-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="e5b81-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e5b81-114">Called by:</span></span>  <br/> |<span data-ttu-id="e5b81-115">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="e5b81-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="e5b81-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="e5b81-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e5b81-117">Иид_иаттачмент</span><span class="sxs-lookup"><span data-stu-id="e5b81-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="e5b81-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="e5b81-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="e5b81-119">ЛПАТТАЧ</span><span class="sxs-lookup"><span data-stu-id="e5b81-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="e5b81-120">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="e5b81-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="e5b81-121">Транзакции</span><span class="sxs-lookup"><span data-stu-id="e5b81-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e5b81-122">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="e5b81-122">Vtable order</span></span>

<span data-ttu-id="e5b81-123">У этого интерфейса нет уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="e5b81-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="e5b81-124">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="e5b81-124">**Required properties**</span></span>|<span data-ttu-id="e5b81-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="e5b81-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e5b81-126">**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5b81-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e5b81-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5b81-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="e5b81-128">**Пр_аттач_месод** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5b81-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e5b81-129">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e5b81-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="e5b81-130">**Пр_рендеринг_поситион** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e5b81-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e5b81-131">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e5b81-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e5b81-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e5b81-132">See also</span></span>



[<span data-ttu-id="e5b81-133">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="e5b81-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

