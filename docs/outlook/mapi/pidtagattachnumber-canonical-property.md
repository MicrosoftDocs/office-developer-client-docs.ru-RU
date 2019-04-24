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
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="260f9-103">Каноническое свойство PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="260f9-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="260f9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="260f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="260f9-105">Содержит номер, однозначно определяющий вложение в родительском сообщении.</span><span class="sxs-lookup"><span data-stu-id="260f9-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="260f9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="260f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="260f9-107">ПР_АТТАЧ_НУМ</span><span class="sxs-lookup"><span data-stu-id="260f9-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="260f9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="260f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="260f9-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="260f9-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="260f9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="260f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="260f9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="260f9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="260f9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="260f9-112">Area:</span></span>  <br/> |<span data-ttu-id="260f9-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="260f9-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="260f9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="260f9-114">Remarks</span></span>

<span data-ttu-id="260f9-115">Хранилища сообщений создают и поддерживают это свойство.</span><span class="sxs-lookup"><span data-stu-id="260f9-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="260f9-116">Номер вложения — это дополнительный ключ сортировки после позиции отрисовки в таблице вложений.</span><span class="sxs-lookup"><span data-stu-id="260f9-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="260f9-117">**Пр_аттач_нум** используется для открытия вложения с помощью метода [iMessage:: опенаттач](imessage-openattach.md) .</span><span class="sxs-lookup"><span data-stu-id="260f9-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="260f9-118">В сеансе клиентского приложения свойство **пр_аттач_нум** вложения сообщения остается неизменным до тех пор, пока открыта таблица вложений.</span><span class="sxs-lookup"><span data-stu-id="260f9-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="260f9-119">Хранилище сообщений распространяет изменения таблицы с помощью методов **iMessage:: креатеаттач** и **iMessage::D елетеаттач** .</span><span class="sxs-lookup"><span data-stu-id="260f9-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="260f9-120">В этом случае хранилище сообщений может создавать табличные уведомления для открытых таблиц вложений, чтобы клиенты могли синхронизироваться с этими изменениями.</span><span class="sxs-lookup"><span data-stu-id="260f9-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="260f9-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="260f9-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="260f9-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="260f9-122">Protocol specifications</span></span>

<span data-ttu-id="260f9-123">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="260f9-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="260f9-124">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="260f9-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="260f9-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="260f9-125">Header files</span></span>

<span data-ttu-id="260f9-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="260f9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="260f9-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="260f9-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="260f9-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="260f9-128">Mapitags.h</span></span>
  
> <span data-ttu-id="260f9-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="260f9-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="260f9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="260f9-130">See also</span></span>



[<span data-ttu-id="260f9-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="260f9-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="260f9-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="260f9-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="260f9-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="260f9-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="260f9-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="260f9-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

