---
title: Каноническое свойство PidLidSharingRemoteType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteType
api_type:
- COM
ms.assetid: e9bc7c7c-86df-45d8-922b-76e3b076144a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8a9975090a8b90946482fa77fd2dafdb503c1f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810549"
---
# <a name="pidlidsharingremotetype-canonical-property"></a><span data-ttu-id="b010b-103">Каноническое свойство PidLidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="b010b-103">PidLidSharingRemoteType Canonical Property</span></span>

  
  
<span data-ttu-id="b010b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b010b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b010b-105">Указывает тип удаленной общей папке.</span><span class="sxs-lookup"><span data-stu-id="b010b-105">Specifies the type of the remote shared folder.</span></span> <span data-ttu-id="b010b-106">Это свойство общего доступа сообщения.</span><span class="sxs-lookup"><span data-stu-id="b010b-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b010b-107">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b010b-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="b010b-108">dispidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="b010b-108">dispidSharingRemoteType</span></span>  <br/> |
|<span data-ttu-id="b010b-109">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b010b-109">Property set:</span></span>  <br/> |<span data-ttu-id="b010b-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="b010b-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="b010b-111">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="b010b-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b010b-112">0x00008A1D</span><span class="sxs-lookup"><span data-stu-id="b010b-112">0x00008A1D</span></span>  <br/> |
|<span data-ttu-id="b010b-113">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b010b-113">Data type:</span></span>  <br/> |<span data-ttu-id="b010b-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b010b-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b010b-115">Область:</span><span class="sxs-lookup"><span data-stu-id="b010b-115">Area:</span></span>  <br/> |<span data-ttu-id="b010b-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="b010b-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b010b-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="b010b-117">Remarks</span></span>

<span data-ttu-id="b010b-118">Это свойство должно иметь значение совпадает со значением свойства **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) и можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="b010b-118">This property must be set to the same value as the **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b010b-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b010b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b010b-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b010b-120">Protocol specifications</span></span>

<span data-ttu-id="b010b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b010b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b010b-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b010b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b010b-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b010b-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b010b-124">Открывает общий доступ папки почтовых ящиков между клиентами.</span><span class="sxs-lookup"><span data-stu-id="b010b-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b010b-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b010b-125">Header files</span></span>

<span data-ttu-id="b010b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b010b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b010b-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b010b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b010b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b010b-128">See also</span></span>



[<span data-ttu-id="b010b-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b010b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b010b-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b010b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b010b-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b010b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b010b-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b010b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

