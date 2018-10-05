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
ms.openlocfilehash: 3be288b606e197b350c1b053303077c1cb984e9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398292"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="3c40a-103">Каноническое свойство PidLidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="3c40a-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="3c40a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c40a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c40a-105">Указывает имя удаленного общей папки.</span><span class="sxs-lookup"><span data-stu-id="3c40a-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="3c40a-106">Это свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="3c40a-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c40a-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3c40a-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c40a-108">dispidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="3c40a-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="3c40a-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="3c40a-109">Property set:</span></span>  <br/> |<span data-ttu-id="3c40a-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="3c40a-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="3c40a-111">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="3c40a-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3c40a-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="3c40a-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="3c40a-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3c40a-113">Data type:</span></span>  <br/> |<span data-ttu-id="3c40a-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3c40a-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3c40a-115">Область:</span><span class="sxs-lookup"><span data-stu-id="3c40a-115">Area:</span></span>  <br/> |<span data-ttu-id="3c40a-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="3c40a-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c40a-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="3c40a-117">Remarks</span></span>

<span data-ttu-id="3c40a-118">Это свойство должно быть присвоено значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) в общей папке.</span><span class="sxs-lookup"><span data-stu-id="3c40a-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3c40a-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3c40a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c40a-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3c40a-120">Protocol specifications</span></span>

<span data-ttu-id="3c40a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c40a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c40a-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3c40a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3c40a-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c40a-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c40a-124">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="3c40a-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c40a-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3c40a-125">Header files</span></span>

<span data-ttu-id="3c40a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c40a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c40a-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3c40a-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c40a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="3c40a-128">See also</span></span>



[<span data-ttu-id="3c40a-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c40a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c40a-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c40a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c40a-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3c40a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c40a-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3c40a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

