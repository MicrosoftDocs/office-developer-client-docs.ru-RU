---
title: Каноническое свойство PidTagMailPermission
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b396cd326dd25fd72346f9f8037e8a712b84a196
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278874"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="9f014-103">Каноническое свойство PidTagMailPermission</span><span class="sxs-lookup"><span data-stu-id="9f014-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="9f014-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f014-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f014-105">Содержит значение TRUE, если пользователю обмена сообщениями разрешено отправлять и получать сообщения.</span><span class="sxs-lookup"><span data-stu-id="9f014-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f014-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9f014-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f014-107">ПР_МАИЛ_ПЕРМИССИОН</span><span class="sxs-lookup"><span data-stu-id="9f014-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="9f014-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9f014-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f014-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="9f014-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="9f014-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9f014-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f014-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9f014-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9f014-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9f014-112">Area:</span></span>  <br/> |<span data-ttu-id="9f014-113">Address</span><span class="sxs-lookup"><span data-stu-id="9f014-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f014-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9f014-114">Remarks</span></span>

<span data-ttu-id="9f014-115">Если это свойство не задано, MAPI рассматривает его как имеющий значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="9f014-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="9f014-116">Установите для этого свойства значение FALSE в корпоративном каталоге, в котором для некоторых записей не включена поддержка электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9f014-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9f014-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9f014-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9f014-118">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="9f014-118">Header files</span></span>

<span data-ttu-id="9f014-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9f014-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f014-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9f014-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9f014-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="9f014-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9f014-122">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="9f014-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f014-123">См. также</span><span class="sxs-lookup"><span data-stu-id="9f014-123">See also</span></span>



[<span data-ttu-id="9f014-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9f014-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f014-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9f014-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f014-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9f014-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f014-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9f014-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

