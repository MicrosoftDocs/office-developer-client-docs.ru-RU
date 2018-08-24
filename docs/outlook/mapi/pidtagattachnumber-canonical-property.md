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
ms.openlocfilehash: f6de157864bff5be41b6e030d555be7b60dcda5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594756"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="35f12-103">Каноническое свойство PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="35f12-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="35f12-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35f12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35f12-105">Содержит номер, который уникальным образом определяет вложения в сообщении его родительского.</span><span class="sxs-lookup"><span data-stu-id="35f12-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35f12-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="35f12-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35f12-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="35f12-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="35f12-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="35f12-108">Identifier:</span></span>  <br/> |<span data-ttu-id="35f12-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="35f12-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="35f12-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="35f12-110">Data type:</span></span>  <br/> |<span data-ttu-id="35f12-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="35f12-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="35f12-112">Область:</span><span class="sxs-lookup"><span data-stu-id="35f12-112">Area:</span></span>  <br/> |<span data-ttu-id="35f12-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="35f12-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35f12-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="35f12-114">Remarks</span></span>

<span data-ttu-id="35f12-115">Хранилищ сообщений создания и обслуживания этого свойства.</span><span class="sxs-lookup"><span data-stu-id="35f12-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="35f12-116">Число вложений — второй ключ сортировки, после положения, в таблице вложений.</span><span class="sxs-lookup"><span data-stu-id="35f12-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="35f12-117">**PR_ATTACH_NUM** используется для открытия вложения с помощью метода [IMessage::OpenAttach](imessage-openattach.md) .</span><span class="sxs-lookup"><span data-stu-id="35f12-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="35f12-118">В рамках сеанса клиентского приложения со значением свойства **PR_ATTACH_NUM** вложения сообщения не изменяется до тех пор, пока открыта в таблице вложений.</span><span class="sxs-lookup"><span data-stu-id="35f12-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="35f12-119">Хранилище сообщений распространяет изменения в таблицу с помощью методов **IMessage::CreateAttach** и **IMessage::DeleteAttach** .</span><span class="sxs-lookup"><span data-stu-id="35f12-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="35f12-120">В его параметр хранилище сообщений может создавать уведомления в таблице в таблицах открыть вложение, чтобы клиенты можно синхронизировать на такие изменения.</span><span class="sxs-lookup"><span data-stu-id="35f12-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="35f12-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="35f12-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="35f12-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="35f12-122">Protocol specifications</span></span>

<span data-ttu-id="35f12-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35f12-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35f12-124">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="35f12-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="35f12-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="35f12-125">Header files</span></span>

<span data-ttu-id="35f12-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35f12-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="35f12-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="35f12-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="35f12-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="35f12-128">Mapitags.h</span></span>
  
> <span data-ttu-id="35f12-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="35f12-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35f12-130">См. также</span><span class="sxs-lookup"><span data-stu-id="35f12-130">See also</span></span>



[<span data-ttu-id="35f12-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="35f12-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35f12-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="35f12-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35f12-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="35f12-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35f12-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="35f12-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

