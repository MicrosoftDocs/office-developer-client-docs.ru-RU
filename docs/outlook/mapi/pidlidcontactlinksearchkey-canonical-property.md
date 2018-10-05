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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387498"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a><span data-ttu-id="d04a5-103">Каноническое свойство PidLidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="d04a5-103">PidLidContactLinkSearchKey Canonical Property</span></span>

<span data-ttu-id="d04a5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d04a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d04a5-105">Содержит список **SearchKeys** для контакта, связанного с объектом сообщения.</span><span class="sxs-lookup"><span data-stu-id="d04a5-105">Contains the list of **SearchKeys** for the contact linked to by this message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d04a5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d04a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d04a5-107">dispidContactLinkSearchKey</span><span class="sxs-lookup"><span data-stu-id="d04a5-107">dispidContactLinkSearchKey</span></span>  <br/> |
|<span data-ttu-id="d04a5-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d04a5-108">Property set:</span></span>  <br/> |<span data-ttu-id="d04a5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d04a5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d04a5-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="d04a5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d04a5-111">0x00008584</span><span class="sxs-lookup"><span data-stu-id="d04a5-111">0x00008584</span></span>  <br/> |
|<span data-ttu-id="d04a5-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d04a5-112">Data type:</span></span>  <br/> |<span data-ttu-id="d04a5-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d04a5-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d04a5-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d04a5-114">Area:</span></span>  <br/> |<span data-ttu-id="d04a5-115">Contact</span><span class="sxs-lookup"><span data-stu-id="d04a5-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d04a5-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d04a5-116">Remarks</span></span>

|<span data-ttu-id="d04a5-117">**Длина в байтах**</span><span class="sxs-lookup"><span data-stu-id="d04a5-117">**Length in bytes**</span></span>|<span data-ttu-id="d04a5-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d04a5-118">**Description**</span></span>|<span data-ttu-id="d04a5-119">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="d04a5-119">**Notes**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d04a5-120">2</span><span class="sxs-lookup"><span data-stu-id="d04a5-120">2</span></span>  <br/> |<span data-ttu-id="d04a5-121">ContactEntryCount</span><span class="sxs-lookup"><span data-stu-id="d04a5-121">ContactEntryCount</span></span>  <br/> |<span data-ttu-id="d04a5-122">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="d04a5-122">None</span></span>  <br/> |
|<span data-ttu-id="d04a5-123">переменная</span><span class="sxs-lookup"><span data-stu-id="d04a5-123">variable</span></span>  <br/> |<span data-ttu-id="d04a5-124">SearchKey данных</span><span class="sxs-lookup"><span data-stu-id="d04a5-124">SearchKey data</span></span>  <br/> |<span data-ttu-id="d04a5-125">Повторяет ContactEntryCount раз</span><span class="sxs-lookup"><span data-stu-id="d04a5-125">Repeats ContactEntryCount times</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d04a5-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d04a5-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d04a5-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d04a5-127">Protocol specifications</span></span>

<span data-ttu-id="d04a5-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d04a5-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d04a5-129">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d04a5-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d04a5-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d04a5-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d04a5-131">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="d04a5-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d04a5-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d04a5-132">Header files</span></span>

<span data-ttu-id="d04a5-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d04a5-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="d04a5-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d04a5-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d04a5-135">См. также</span><span class="sxs-lookup"><span data-stu-id="d04a5-135">See also</span></span>

- [<span data-ttu-id="d04a5-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d04a5-136">MAPI Properties</span></span>](mapi-properties.md) 
- [<span data-ttu-id="d04a5-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d04a5-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="d04a5-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d04a5-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="d04a5-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d04a5-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

