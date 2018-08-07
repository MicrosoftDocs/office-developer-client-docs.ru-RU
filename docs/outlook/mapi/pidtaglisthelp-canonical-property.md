---
title: Каноническое свойство PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7a9a5d090babce8105fab43bf8401448373777cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811334"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="2c1a3-103">Каноническое свойство PidTagListHelp</span><span class="sxs-lookup"><span data-stu-id="2c1a3-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="2c1a3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c1a3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c1a3-105">Содержит значение в поле Заголовок списка-Help сообщение Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="2c1a3-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c1a3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2c1a3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c1a3-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="2c1a3-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="2c1a3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2c1a3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c1a3-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="2c1a3-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="2c1a3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2c1a3-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c1a3-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2c1a3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2c1a3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2c1a3-112">Area:</span></span>  <br/> |<span data-ttu-id="2c1a3-113">Разное</span><span class="sxs-lookup"><span data-stu-id="2c1a3-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c1a3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2c1a3-114">Remarks</span></span>

<span data-ttu-id="2c1a3-115">Чтобы создать поле заголовка списка-Help, клиенты необходимо установить значение **PR_LIST_HELP** или свойство нужное значение.</span><span class="sxs-lookup"><span data-stu-id="2c1a3-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="2c1a3-116">Записи MIME необходимо скопировать это значение в поле Заголовок списка-Help.</span><span class="sxs-lookup"><span data-stu-id="2c1a3-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="2c1a3-117">Чтобы задать значение эти свойства списка, связанные с сервера, клиенты MIME необходимо создать поля заголовка, как указано в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="2c1a3-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="2c1a3-118">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="2c1a3-118">**Property**</span></span>|<span data-ttu-id="2c1a3-119">**Имя поля Предпочитаемый заголовка**</span><span class="sxs-lookup"><span data-stu-id="2c1a3-119">**Preferred header field name**</span></span>|<span data-ttu-id="2c1a3-120">**Альтернативные заголовок поля имя**</span><span class="sxs-lookup"><span data-stu-id="2c1a3-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2c1a3-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="2c1a3-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="2c1a3-122">Справка для списка</span><span class="sxs-lookup"><span data-stu-id="2c1a3-122">List-Help</span></span>  <br/> |<span data-ttu-id="2c1a3-123">Справка для списка X</span><span class="sxs-lookup"><span data-stu-id="2c1a3-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2c1a3-124">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2c1a3-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c1a3-125">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2c1a3-125">Protocol specifications</span></span>

<span data-ttu-id="2c1a3-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c1a3-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c1a3-127">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2c1a3-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c1a3-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c1a3-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c1a3-129">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c1a3-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c1a3-130">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2c1a3-130">Header files</span></span>

<span data-ttu-id="2c1a3-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c1a3-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c1a3-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2c1a3-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c1a3-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2c1a3-133">Mapitags.h</span></span>
  
> <span data-ttu-id="2c1a3-134">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2c1a3-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c1a3-135">См. также</span><span class="sxs-lookup"><span data-stu-id="2c1a3-135">See also</span></span>



[<span data-ttu-id="2c1a3-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2c1a3-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c1a3-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2c1a3-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c1a3-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2c1a3-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c1a3-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2c1a3-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

