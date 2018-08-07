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
ms.openlocfilehash: 13e2ac93e7e3ba46bf25b26e76bd44c15f2b89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810378"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="8f35a-103">Каноническое свойство PidLidImageAttachmentsCompressionLevel</span><span class="sxs-lookup"><span data-stu-id="8f35a-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="8f35a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8f35a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8f35a-105">Определяет уровень сжатия для применения на attachments изображения.</span><span class="sxs-lookup"><span data-stu-id="8f35a-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8f35a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8f35a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f35a-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="8f35a-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="8f35a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8f35a-108">Property set:</span></span>  <br/> |<span data-ttu-id="8f35a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="8f35a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="8f35a-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="8f35a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8f35a-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="8f35a-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="8f35a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8f35a-112">Data type:</span></span>  <br/> |<span data-ttu-id="8f35a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8f35a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8f35a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8f35a-114">Area:</span></span>  <br/> |<span data-ttu-id="8f35a-115">Конфигурация во время выполнения</span><span class="sxs-lookup"><span data-stu-id="8f35a-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f35a-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="8f35a-116">Remarks</span></span>

<span data-ttu-id="8f35a-117">Ниже приведены уровни допустимый сжатие.</span><span class="sxs-lookup"><span data-stu-id="8f35a-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="8f35a-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8f35a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8f35a-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8f35a-119">Protocol specifications</span></span>

<span data-ttu-id="8f35a-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="8f35a-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="8f35a-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8f35a-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8f35a-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8f35a-122">Header files</span></span>

<span data-ttu-id="8f35a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8f35a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f35a-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8f35a-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f35a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="8f35a-125">See also</span></span>



[<span data-ttu-id="8f35a-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8f35a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f35a-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8f35a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f35a-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8f35a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f35a-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8f35a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

