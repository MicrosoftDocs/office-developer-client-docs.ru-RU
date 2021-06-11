---
title: Каноническое свойство PidLidSharingResponseType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 34e8a3c73715a75b8007646e5ba3b0dc3e1ae919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331194"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a><span data-ttu-id="d5617-103">Каноническое свойство PidLidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="d5617-103">PidLidSharingResponseType Canonical Property</span></span>

  
  
<span data-ttu-id="d5617-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5617-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5617-105">Указывает тип ответа, на который ответил получатель запроса общего доступа.</span><span class="sxs-lookup"><span data-stu-id="d5617-105">Specifies the type of response with which the recipient of the sharing request responded.</span></span> <span data-ttu-id="d5617-106">Это свойство общего сообщения.</span><span class="sxs-lookup"><span data-stu-id="d5617-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d5617-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d5617-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="d5617-108">dispidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="d5617-108">dispidSharingResponseType</span></span>  <br/> |
|<span data-ttu-id="d5617-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d5617-109">Property set:</span></span>  <br/> |<span data-ttu-id="d5617-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="d5617-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="d5617-111">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d5617-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d5617-112">0x00008A27</span><span class="sxs-lookup"><span data-stu-id="d5617-112">0x00008A27</span></span>  <br/> |
|<span data-ttu-id="d5617-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d5617-113">Data type:</span></span>  <br/> |<span data-ttu-id="d5617-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d5617-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d5617-115">Область:</span><span class="sxs-lookup"><span data-stu-id="d5617-115">Area:</span></span>  <br/> |<span data-ttu-id="d5617-116">Доступ</span><span class="sxs-lookup"><span data-stu-id="d5617-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5617-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="d5617-117">Remarks</span></span>

<span data-ttu-id="d5617-118">Значение этого свойства должно быть заданной одному из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d5617-118">The value of this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="d5617-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d5617-119">**Value**</span></span>|<span data-ttu-id="d5617-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d5617-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5617-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5617-121">0x00000000</span></span>  <br/> |<span data-ttu-id="d5617-122">Нет ответа</span><span class="sxs-lookup"><span data-stu-id="d5617-122">No response</span></span>  <br/> |
|<span data-ttu-id="d5617-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d5617-123">0x00000001</span></span>  <br/> |<span data-ttu-id="d5617-124">Accepted</span><span class="sxs-lookup"><span data-stu-id="d5617-124">Accepted</span></span>  <br/> |
|<span data-ttu-id="d5617-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d5617-125">0x00000002</span></span>  <br/> |<span data-ttu-id="d5617-126">Отклонено</span><span class="sxs-lookup"><span data-stu-id="d5617-126">Denied</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d5617-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d5617-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d5617-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d5617-128">Protocol specifications</span></span>

<span data-ttu-id="d5617-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5617-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5617-130">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="d5617-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d5617-131">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5617-131">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5617-132">Делит папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="d5617-132">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d5617-133">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="d5617-133">Header files</span></span>

<span data-ttu-id="d5617-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5617-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="d5617-135">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d5617-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5617-136">См. также</span><span class="sxs-lookup"><span data-stu-id="d5617-136">See also</span></span>



[<span data-ttu-id="d5617-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d5617-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d5617-138">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d5617-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d5617-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d5617-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d5617-140">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="d5617-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

