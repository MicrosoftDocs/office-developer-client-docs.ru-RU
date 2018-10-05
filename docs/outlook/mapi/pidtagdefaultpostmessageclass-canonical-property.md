---
title: Каноническое свойство PidTagDefaultPostMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0ab904625d3a23462a4fedf3b64f49c54b34ad28
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401729"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="06c6a-103">Каноническое свойство PidTagDefaultPostMessageClass</span><span class="sxs-lookup"><span data-stu-id="06c6a-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="06c6a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06c6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06c6a-105">Содержит имя настраиваемой формы класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="06c6a-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06c6a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="06c6a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06c6a-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="06c6a-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="06c6a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="06c6a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06c6a-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="06c6a-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="06c6a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="06c6a-110">Data type:</span></span>  <br/> |<span data-ttu-id="06c6a-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="06c6a-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="06c6a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="06c6a-112">Area:</span></span>  <br/> |<span data-ttu-id="06c6a-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="06c6a-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06c6a-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="06c6a-114">Remarks</span></span>

<span data-ttu-id="06c6a-115">Если это свойство задано для папки, значение должно содержать либо точно базового класса сообщения (например, «IPM. Контакт» для папки «Контакты» или «IPM. Встреча» для папки «Календарь»), или начинаться с базового класса сообщения (например, «IPM. [[[Contact.MyContact»).</span><span class="sxs-lookup"><span data-stu-id="06c6a-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="06c6a-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="06c6a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06c6a-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="06c6a-117">Protocol specifications</span></span>

<span data-ttu-id="06c6a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06c6a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06c6a-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="06c6a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06c6a-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06c6a-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06c6a-121">Задает свойства и операции для встречи, приглашения на собрание и ответы.</span><span class="sxs-lookup"><span data-stu-id="06c6a-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06c6a-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="06c6a-122">Header files</span></span>

<span data-ttu-id="06c6a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06c6a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="06c6a-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="06c6a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="06c6a-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06c6a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="06c6a-126">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="06c6a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06c6a-127">См. также</span><span class="sxs-lookup"><span data-stu-id="06c6a-127">See also</span></span>



[<span data-ttu-id="06c6a-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="06c6a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06c6a-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="06c6a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06c6a-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="06c6a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06c6a-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="06c6a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

