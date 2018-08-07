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
ms.openlocfilehash: df2fa19656aa1bff810a082cda94a091e2c7fc9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811298"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="ff0d8-103">Каноническое свойство PidTagItemTemporaryflags</span><span class="sxs-lookup"><span data-stu-id="ff0d8-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="ff0d8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff0d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff0d8-105">Содержит флаг, указывающий, что сообщение было читать, но не помечается как прочтенные.</span><span class="sxs-lookup"><span data-stu-id="ff0d8-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff0d8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ff0d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff0d8-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="ff0d8-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="ff0d8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ff0d8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff0d8-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="ff0d8-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="ff0d8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ff0d8-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff0d8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ff0d8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ff0d8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ff0d8-112">Area:</span></span>  <br/> |<span data-ttu-id="ff0d8-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="ff0d8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff0d8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ff0d8-114">Remarks</span></span>

<span data-ttu-id="ff0d8-115">Это свойство используется в папке поиска непрочитанные сообщения Outlook для отслеживания сообщений будут прочитаны без фактического пометки их как чтение, которое может удалить их из папки.</span><span class="sxs-lookup"><span data-stu-id="ff0d8-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="ff0d8-116">После изменения представления, это свойство будет удален и элемент отмечен как чтение.</span><span class="sxs-lookup"><span data-stu-id="ff0d8-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="ff0d8-117">Это свойство не будут синхронизированы с сервером Exchange.</span><span class="sxs-lookup"><span data-stu-id="ff0d8-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ff0d8-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ff0d8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff0d8-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ff0d8-119">Protocol specifications</span></span>

<span data-ttu-id="ff0d8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff0d8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff0d8-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ff0d8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ff0d8-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff0d8-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff0d8-123">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="ff0d8-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff0d8-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ff0d8-124">Header files</span></span>

<span data-ttu-id="ff0d8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff0d8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff0d8-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ff0d8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff0d8-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff0d8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ff0d8-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ff0d8-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff0d8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ff0d8-129">See also</span></span>



[<span data-ttu-id="ff0d8-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ff0d8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff0d8-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ff0d8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff0d8-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ff0d8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff0d8-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ff0d8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

