---
title: Каноническое свойство PidTagDefaultViewEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270016"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a><span data-ttu-id="70377-103">Каноническое свойство PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="70377-103">PidTagDefaultViewEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="70377-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70377-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70377-105">Содержит идентификатор элемента представления по умолчанию для папки.</span><span class="sxs-lookup"><span data-stu-id="70377-105">Contains the entry identifier of a folder's default view.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70377-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="70377-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70377-107">ПР_ДЕФАУЛТ_ВИЕВ_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="70377-107">PR_DEFAULT_VIEW_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="70377-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="70377-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70377-109">0x3616</span><span class="sxs-lookup"><span data-stu-id="70377-109">0x3616</span></span>  <br/> |
|<span data-ttu-id="70377-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="70377-110">Data type:</span></span>  <br/> |<span data-ttu-id="70377-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="70377-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="70377-112">Область:</span><span class="sxs-lookup"><span data-stu-id="70377-112">Area:</span></span>  <br/> |<span data-ttu-id="70377-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="70377-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70377-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="70377-114">Remarks</span></span>

<span data-ttu-id="70377-115">Это свойство представляет собой идентификатор элемента представления папки, который должен быть установлен в качестве исходного представления.</span><span class="sxs-lookup"><span data-stu-id="70377-115">This property is the entry identifier of the folder view that should be set as the initial view.</span></span> <span data-ttu-id="70377-116">Свойство не требуется задавать, если в качестве начального представления используется "обычное представление".</span><span class="sxs-lookup"><span data-stu-id="70377-116">The property need not be set if the "Normal" view is to be used as the initial view.</span></span>
  
<span data-ttu-id="70377-117">Клиентское приложение может получить это свойство во время открытия папки и добиться значительного выигрыша в производительности.</span><span class="sxs-lookup"><span data-stu-id="70377-117">A client application can obtain this property at the time it opens the folder and realize significant performance gains.</span></span> <span data-ttu-id="70377-118">Это свойство можно использовать в качестве ярлыка для получения представления по умолчанию вместо того, чтобы открывать связанную таблицу содержимого и отправить ограничение.</span><span class="sxs-lookup"><span data-stu-id="70377-118">This property can be used as a shortcut to obtain the default view, instead of opening the associated contents table and submitting a restriction.</span></span>
  
<span data-ttu-id="70377-119">Реализация поставщика услуг метода [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) может копировать это свойство при копировании папок.</span><span class="sxs-lookup"><span data-stu-id="70377-119">A service provider implementation of the [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) method can copy this property when it copies folders.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="70377-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="70377-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70377-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="70377-121">Protocol specifications</span></span>

<span data-ttu-id="70377-122">[[MS — ОКСКФОЛД]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70377-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70377-123">Обрабатывает операции с папками.</span><span class="sxs-lookup"><span data-stu-id="70377-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70377-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="70377-124">Header files</span></span>

<span data-ttu-id="70377-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="70377-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="70377-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="70377-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="70377-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="70377-127">Mapitags.h</span></span>
  
> <span data-ttu-id="70377-128">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="70377-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70377-129">См. также</span><span class="sxs-lookup"><span data-stu-id="70377-129">See also</span></span>



[<span data-ttu-id="70377-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="70377-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70377-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="70377-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70377-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="70377-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70377-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="70377-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

