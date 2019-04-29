---
title: Каноническое свойство PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429861"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="77bc6-103">Каноническое свойство PidTagResourcePath</span><span class="sxs-lookup"><span data-stu-id="77bc6-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="77bc6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77bc6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77bc6-105">Содержит путь к серверу поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="77bc6-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77bc6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="77bc6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77bc6-107">ПР_РЕСАУРЦЕ_ПАС, ПР_РЕСАУРЦЕ_ПАС_А, ПР_РЕСАУРЦЕ_ПАС_В</span><span class="sxs-lookup"><span data-stu-id="77bc6-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="77bc6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="77bc6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="77bc6-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="77bc6-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="77bc6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="77bc6-110">Data type:</span></span>  <br/> |<span data-ttu-id="77bc6-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="77bc6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="77bc6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="77bc6-112">Area:</span></span>  <br/> |<span data-ttu-id="77bc6-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="77bc6-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77bc6-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="77bc6-114">Remarks</span></span>

<span data-ttu-id="77bc6-115">Путь, содержащийся в этих свойствах, представляет предполагаемый путь, по которому пользователь может найти ресурсы.</span><span class="sxs-lookup"><span data-stu-id="77bc6-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="77bc6-116">Определение этих свойств относится к конкретному поставщику.</span><span class="sxs-lookup"><span data-stu-id="77bc6-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="77bc6-117">Например, приложение для планирования использует эти свойства, чтобы указать предполагаемое расположение для файлов приложений планирования.</span><span class="sxs-lookup"><span data-stu-id="77bc6-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="77bc6-118">Профиль пользователя обмена сообщениями предоставляет эти свойства для удобства, чтобы клиентское приложение не предложит пользователю обмена сообщениями сетевой путь или букву сетевого диска.</span><span class="sxs-lookup"><span data-stu-id="77bc6-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="77bc6-119">MAPI работает только с именами файлов в наборе символов ANSI (американский национальный институт стандартизации).</span><span class="sxs-lookup"><span data-stu-id="77bc6-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="77bc6-120">Приложения, использующие имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом функции MAPI.</span><span class="sxs-lookup"><span data-stu-id="77bc6-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="77bc6-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="77bc6-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="77bc6-122">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="77bc6-122">Header files</span></span>

<span data-ttu-id="77bc6-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="77bc6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="77bc6-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="77bc6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="77bc6-125">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="77bc6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="77bc6-126">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="77bc6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77bc6-127">См. также</span><span class="sxs-lookup"><span data-stu-id="77bc6-127">See also</span></span>



[<span data-ttu-id="77bc6-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="77bc6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77bc6-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="77bc6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77bc6-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="77bc6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77bc6-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="77bc6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

