---
title: Каноническое свойство PidTagItemTemporaryflags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagItemTemporaryflags
api_type:
- HeaderDef
ms.assetid: 8066de8e-2b77-4bac-8df3-e64b03ee42b9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ec092e6cc6174e156dbfe7784143c9d74715eef7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357703"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="2e117-103">Каноническое свойство PidTagItemTemporaryflags</span><span class="sxs-lookup"><span data-stu-id="2e117-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="2e117-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e117-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e117-105">Содержит флаг, который указывает, что сообщение прочитано, но не помечено как прочитано.</span><span class="sxs-lookup"><span data-stu-id="2e117-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e117-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2e117-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e117-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="2e117-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="2e117-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2e117-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e117-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="2e117-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="2e117-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2e117-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e117-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2e117-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2e117-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2e117-112">Area:</span></span>  <br/> |<span data-ttu-id="2e117-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="2e117-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e117-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e117-114">Remarks</span></span>

<span data-ttu-id="2e117-115">Это свойство используется в папке поиска непрочитанные сообщения Outlook для отслеживания сообщений, прочитанные без их пометки как прочитанные, что позволит удалить их из папки.</span><span class="sxs-lookup"><span data-stu-id="2e117-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="2e117-116">При смене представления это свойство удаляется, а элемент помечается как прочитаенный.</span><span class="sxs-lookup"><span data-stu-id="2e117-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="2e117-117">Это свойство не будет синхронизироваться с Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2e117-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2e117-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2e117-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2e117-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2e117-119">Protocol specifications</span></span>

<span data-ttu-id="2e117-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e117-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e117-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="2e117-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2e117-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e117-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e117-123">Обрабатывает операции с папками.</span><span class="sxs-lookup"><span data-stu-id="2e117-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2e117-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="2e117-124">Header files</span></span>

<span data-ttu-id="2e117-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e117-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e117-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2e117-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e117-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2e117-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2e117-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2e117-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e117-129">См. также</span><span class="sxs-lookup"><span data-stu-id="2e117-129">See also</span></span>



[<span data-ttu-id="2e117-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2e117-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e117-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2e117-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e117-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2e117-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e117-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2e117-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

