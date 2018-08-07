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
ms.openlocfilehash: 4cc97647c60322783050abbebd18726434632a43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811337"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="4d70e-103">Каноническое свойство PidTagMailPermission</span><span class="sxs-lookup"><span data-stu-id="4d70e-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="4d70e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4d70e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4d70e-105">Содержит значение TRUE, если пользователь обмена сообщениями может отправлять и получать сообщения.</span><span class="sxs-lookup"><span data-stu-id="4d70e-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d70e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4d70e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d70e-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="4d70e-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="4d70e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4d70e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d70e-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="4d70e-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="4d70e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4d70e-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d70e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4d70e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4d70e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4d70e-112">Area:</span></span>  <br/> |<span data-ttu-id="4d70e-113">Address</span><span class="sxs-lookup"><span data-stu-id="4d70e-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d70e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4d70e-114">Remarks</span></span>

<span data-ttu-id="4d70e-115">Если это свойство не задано, MAPI обрабатывает ее как имеющий значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="4d70e-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="4d70e-116">Этому свойству присвоено значение FALSE в каталоге организации которых некоторые записи не включенной поддержкой электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4d70e-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4d70e-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4d70e-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4d70e-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4d70e-118">Header files</span></span>

<span data-ttu-id="4d70e-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d70e-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d70e-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4d70e-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d70e-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4d70e-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4d70e-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="4d70e-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d70e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="4d70e-123">See also</span></span>



[<span data-ttu-id="4d70e-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4d70e-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d70e-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4d70e-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d70e-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4d70e-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d70e-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4d70e-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

