---
title: Каноническое свойство PidLidContactLinkSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea815631f63b5585a3f2705cfbd2639b8c655e6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319777"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a><span data-ttu-id="4661a-103">Каноническое свойство PidLidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="4661a-103">PidLidContactLinkSearchKey Canonical Property</span></span>

<span data-ttu-id="4661a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4661a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4661a-105">Содержит список **сеарчкэйс** для контакта, связанного с этим объектом Message.</span><span class="sxs-lookup"><span data-stu-id="4661a-105">Contains the list of **SearchKeys** for the contact linked to by this message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4661a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4661a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4661a-107">диспидконтактлинксеарчкэй</span><span class="sxs-lookup"><span data-stu-id="4661a-107">dispidContactLinkSearchKey</span></span>  <br/> |
|<span data-ttu-id="4661a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="4661a-108">Property set:</span></span>  <br/> |<span data-ttu-id="4661a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4661a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4661a-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="4661a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4661a-111">0x00008584</span><span class="sxs-lookup"><span data-stu-id="4661a-111">0x00008584</span></span>  <br/> |
|<span data-ttu-id="4661a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4661a-112">Data type:</span></span>  <br/> |<span data-ttu-id="4661a-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4661a-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4661a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="4661a-114">Area:</span></span>  <br/> |<span data-ttu-id="4661a-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="4661a-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4661a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4661a-116">Remarks</span></span>

|<span data-ttu-id="4661a-117">**Длина в байтах**</span><span class="sxs-lookup"><span data-stu-id="4661a-117">**Length in bytes**</span></span>|<span data-ttu-id="4661a-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4661a-118">**Description**</span></span>|<span data-ttu-id="4661a-119">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="4661a-119">**Notes**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4661a-120">2</span><span class="sxs-lookup"><span data-stu-id="4661a-120">2</span></span>  <br/> |<span data-ttu-id="4661a-121">контактентрикаунт</span><span class="sxs-lookup"><span data-stu-id="4661a-121">ContactEntryCount</span></span>  <br/> |<span data-ttu-id="4661a-122">Нет</span><span class="sxs-lookup"><span data-stu-id="4661a-122">None</span></span>  <br/> |
|<span data-ttu-id="4661a-123">переменная</span><span class="sxs-lookup"><span data-stu-id="4661a-123">variable</span></span>  <br/> |<span data-ttu-id="4661a-124">Данные Сеарчкэй</span><span class="sxs-lookup"><span data-stu-id="4661a-124">SearchKey data</span></span>  <br/> |<span data-ttu-id="4661a-125">Повторяет Контактентрикаунт раз</span><span class="sxs-lookup"><span data-stu-id="4661a-125">Repeats ContactEntryCount times</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4661a-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4661a-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4661a-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4661a-127">Protocol specifications</span></span>

<span data-ttu-id="4661a-128">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4661a-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4661a-129">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4661a-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4661a-130">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4661a-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4661a-131">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="4661a-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4661a-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4661a-132">Header files</span></span>

<span data-ttu-id="4661a-133">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4661a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="4661a-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4661a-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4661a-135">См. также</span><span class="sxs-lookup"><span data-stu-id="4661a-135">See also</span></span>

- [<span data-ttu-id="4661a-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4661a-136">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="4661a-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="4661a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="4661a-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4661a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="4661a-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4661a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

