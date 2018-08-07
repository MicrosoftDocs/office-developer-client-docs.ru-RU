---
title: Каноническое свойство PidLidSharingRemoteName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteName
api_type:
- COM
ms.assetid: be975f74-4b95-45a4-bbee-959fa8e4ad45
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fc3324cb686733f06b9cc0945c93b7df2e5980ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810548"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="5bcab-103">Каноническое свойство PidLidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="5bcab-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="5bcab-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bcab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bcab-105">Указывает имя удаленного общей папки.</span><span class="sxs-lookup"><span data-stu-id="5bcab-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="5bcab-106">Это свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="5bcab-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5bcab-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5bcab-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="5bcab-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="5bcab-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="5bcab-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="5bcab-109">Property set:</span></span>  <br/> |<span data-ttu-id="5bcab-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="5bcab-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="5bcab-111">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="5bcab-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5bcab-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="5bcab-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="5bcab-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5bcab-113">Data type:</span></span>  <br/> |<span data-ttu-id="5bcab-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5bcab-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5bcab-115">Область:</span><span class="sxs-lookup"><span data-stu-id="5bcab-115">Area:</span></span>  <br/> |<span data-ttu-id="5bcab-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="5bcab-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bcab-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bcab-117">Remarks</span></span>

<span data-ttu-id="5bcab-118">Это свойство должно быть присвоено значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) в общей папке.</span><span class="sxs-lookup"><span data-stu-id="5bcab-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5bcab-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5bcab-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5bcab-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5bcab-120">Protocol specifications</span></span>

<span data-ttu-id="5bcab-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bcab-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bcab-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5bcab-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5bcab-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5bcab-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5bcab-124">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="5bcab-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5bcab-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5bcab-125">Header files</span></span>

<span data-ttu-id="5bcab-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5bcab-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5bcab-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5bcab-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bcab-128">См. также</span><span class="sxs-lookup"><span data-stu-id="5bcab-128">See also</span></span>



[<span data-ttu-id="5bcab-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5bcab-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5bcab-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5bcab-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5bcab-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5bcab-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5bcab-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5bcab-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

