---
title: Каноническое свойство PidLidImageAttachmentsCompressionLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 55b965374bb1d7e5859f0cac5cc2f61956ea5b55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578922"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="2ebd0-103">Каноническое свойство PidLidImageAttachmentsCompressionLevel</span><span class="sxs-lookup"><span data-stu-id="2ebd0-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="2ebd0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ebd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ebd0-105">Определяет уровень сжатия для применения на attachments изображения.</span><span class="sxs-lookup"><span data-stu-id="2ebd0-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ebd0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2ebd0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ebd0-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="2ebd0-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="2ebd0-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="2ebd0-108">Property set:</span></span>  <br/> |<span data-ttu-id="2ebd0-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="2ebd0-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="2ebd0-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="2ebd0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2ebd0-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="2ebd0-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="2ebd0-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2ebd0-112">Data type:</span></span>  <br/> |<span data-ttu-id="2ebd0-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2ebd0-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2ebd0-114">Область:</span><span class="sxs-lookup"><span data-stu-id="2ebd0-114">Area:</span></span>  <br/> |<span data-ttu-id="2ebd0-115">Конфигурация во время выполнения</span><span class="sxs-lookup"><span data-stu-id="2ebd0-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ebd0-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="2ebd0-116">Remarks</span></span>

<span data-ttu-id="2ebd0-117">Ниже приведены уровни допустимый сжатие.</span><span class="sxs-lookup"><span data-stu-id="2ebd0-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="2ebd0-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2ebd0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ebd0-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2ebd0-119">Protocol specifications</span></span>

<span data-ttu-id="2ebd0-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="2ebd0-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="2ebd0-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2ebd0-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ebd0-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2ebd0-122">Header files</span></span>

<span data-ttu-id="2ebd0-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ebd0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ebd0-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2ebd0-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ebd0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="2ebd0-125">See also</span></span>



[<span data-ttu-id="2ebd0-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ebd0-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ebd0-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2ebd0-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ebd0-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2ebd0-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ebd0-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2ebd0-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

