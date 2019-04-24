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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303096"
---
# <a name="pidlidsharingremotename-canonical-property"></a><span data-ttu-id="796ec-103">Каноническое свойство PidLidSharingRemoteName</span><span class="sxs-lookup"><span data-stu-id="796ec-103">PidLidSharingRemoteName Canonical Property</span></span>

  
  
<span data-ttu-id="796ec-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="796ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="796ec-105">Указывает имя удаленной папки, к которой предоставлен общий доступ.</span><span class="sxs-lookup"><span data-stu-id="796ec-105">Specifies the name of the remote folder that is being shared.</span></span> <span data-ttu-id="796ec-106">Это свойство сообщения о совместном доступе.</span><span class="sxs-lookup"><span data-stu-id="796ec-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="796ec-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="796ec-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="796ec-108">Диспидшарингремотенаме</span><span class="sxs-lookup"><span data-stu-id="796ec-108">dispidSharingRemoteName</span></span>  <br/> |
|<span data-ttu-id="796ec-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="796ec-109">Property set:</span></span>  <br/> |<span data-ttu-id="796ec-110">Псетид_шаринг</span><span class="sxs-lookup"><span data-stu-id="796ec-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="796ec-111">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="796ec-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="796ec-112">0x00008A05</span><span class="sxs-lookup"><span data-stu-id="796ec-112">0x00008A05</span></span>  <br/> |
|<span data-ttu-id="796ec-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="796ec-113">Data type:</span></span>  <br/> |<span data-ttu-id="796ec-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="796ec-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="796ec-115">Область:</span><span class="sxs-lookup"><span data-stu-id="796ec-115">Area:</span></span>  <br/> |<span data-ttu-id="796ec-116">Общий доступ</span><span class="sxs-lookup"><span data-stu-id="796ec-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="796ec-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="796ec-117">Remarks</span></span>

<span data-ttu-id="796ec-118">Этому свойству должно быть присвоено значение свойства **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) для общей папки.</span><span class="sxs-lookup"><span data-stu-id="796ec-118">This property must be set to the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property on the folder being shared.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="796ec-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="796ec-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="796ec-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="796ec-120">Protocol specifications</span></span>

<span data-ttu-id="796ec-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796ec-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796ec-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="796ec-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="796ec-123">[[MS — ОКСШАРЕ]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="796ec-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="796ec-124">Предоставляет общий доступ к папкам почтового ящика между клиентами.</span><span class="sxs-lookup"><span data-stu-id="796ec-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="796ec-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="796ec-125">Header files</span></span>

<span data-ttu-id="796ec-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="796ec-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="796ec-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="796ec-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="796ec-128">См. также</span><span class="sxs-lookup"><span data-stu-id="796ec-128">See also</span></span>



[<span data-ttu-id="796ec-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="796ec-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="796ec-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="796ec-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="796ec-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="796ec-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="796ec-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="796ec-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

