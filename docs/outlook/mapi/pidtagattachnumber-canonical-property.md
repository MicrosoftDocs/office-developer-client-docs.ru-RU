---
title: Каноническое свойство PidTagAttachNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327253"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="5dee2-103">Каноническое свойство PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="5dee2-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="5dee2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dee2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dee2-105">Содержит номер, уникальный для идентификации вложения в родительском сообщении.</span><span class="sxs-lookup"><span data-stu-id="5dee2-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5dee2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5dee2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5dee2-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="5dee2-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="5dee2-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5dee2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5dee2-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="5dee2-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="5dee2-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5dee2-110">Data type:</span></span>  <br/> |<span data-ttu-id="5dee2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5dee2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5dee2-112">Область:</span><span class="sxs-lookup"><span data-stu-id="5dee2-112">Area:</span></span>  <br/> |<span data-ttu-id="5dee2-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="5dee2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5dee2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5dee2-114">Remarks</span></span>

<span data-ttu-id="5dee2-115">Хранилища сообщений создают и поддерживают это свойство.</span><span class="sxs-lookup"><span data-stu-id="5dee2-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="5dee2-116">Номер вложения — это клавиша вторичного сортировки после позиции отрисовки в таблице вложений.</span><span class="sxs-lookup"><span data-stu-id="5dee2-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="5dee2-117">**PR_ATTACH_NUM** используется для открытия вложения методом [IMessage::OpenAttach.](imessage-openattach.md)</span><span class="sxs-lookup"><span data-stu-id="5dee2-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="5dee2-118">В сеансе клиентского приложения свойство **PR_ATTACH_NUM** вложения сообщений остается неизменным до тех пор, пока открыта таблица вложений.</span><span class="sxs-lookup"><span data-stu-id="5dee2-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="5dee2-119">Хранилище сообщений распространяет изменения в таблице с помощью **методов IMessage::CreateAttach** и **IMessage::D eleteAttach.**</span><span class="sxs-lookup"><span data-stu-id="5dee2-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="5dee2-120">В своем варианте хранилище сообщений может создавать уведомления таблиц на открытых столах вложений, чтобы клиенты могли повторно скоминализовать эти изменения.</span><span class="sxs-lookup"><span data-stu-id="5dee2-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5dee2-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5dee2-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5dee2-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5dee2-122">Protocol specifications</span></span>

<span data-ttu-id="5dee2-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dee2-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dee2-124">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="5dee2-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5dee2-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="5dee2-125">Header files</span></span>

<span data-ttu-id="5dee2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5dee2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5dee2-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5dee2-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="5dee2-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5dee2-128">Mapitags.h</span></span>
  
> <span data-ttu-id="5dee2-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="5dee2-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5dee2-130">См. также</span><span class="sxs-lookup"><span data-stu-id="5dee2-130">See also</span></span>



[<span data-ttu-id="5dee2-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5dee2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5dee2-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5dee2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5dee2-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5dee2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5dee2-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="5dee2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

