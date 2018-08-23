---
title: Каноническое свойство PidLidSpamOriginalFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 639d5e96eb56fb543d6a6026b1c9400631cee819
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593342"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="8ba92-103">Каноническое свойство PidLidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="8ba92-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="8ba92-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ba92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ba92-105">Указывает, какие папки сообщение находился до его было отфильтровано в папку нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="8ba92-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ba92-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8ba92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ba92-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="8ba92-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="8ba92-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8ba92-108">Property set:</span></span>  <br/> |<span data-ttu-id="8ba92-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="8ba92-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="8ba92-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="8ba92-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8ba92-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="8ba92-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="8ba92-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8ba92-112">Data type:</span></span>  <br/> |<span data-ttu-id="8ba92-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8ba92-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8ba92-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8ba92-114">Area:</span></span>  <br/> |<span data-ttu-id="8ba92-115">Нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="8ba92-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ba92-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="8ba92-116">Remarks</span></span>

<span data-ttu-id="8ba92-117">Значение этого свойства — это **идентификатор записи** для той папке, где сообщения до перемещения.</span><span class="sxs-lookup"><span data-stu-id="8ba92-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="8ba92-118">Это свойство необходимо задать, когда сообщение помечено как нежелательная почта.</span><span class="sxs-lookup"><span data-stu-id="8ba92-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8ba92-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8ba92-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ba92-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8ba92-120">Protocol specifications</span></span>

<span data-ttu-id="8ba92-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ba92-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ba92-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8ba92-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8ba92-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ba92-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ba92-124">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8ba92-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8ba92-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8ba92-125">Header files</span></span>

<span data-ttu-id="8ba92-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ba92-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ba92-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8ba92-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ba92-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8ba92-128">See also</span></span>



[<span data-ttu-id="8ba92-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ba92-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ba92-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ba92-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ba92-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8ba92-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ba92-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8ba92-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

