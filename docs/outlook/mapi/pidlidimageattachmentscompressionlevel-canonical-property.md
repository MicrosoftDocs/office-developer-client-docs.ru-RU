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
ms.openlocfilehash: 8600cc7071fbe5c08d5df074f9bf59f4320b7f18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413831"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="f6e78-103">Каноническое свойство PidLidImageAttachmentsCompressionLevel</span><span class="sxs-lookup"><span data-stu-id="f6e78-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="f6e78-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6e78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6e78-105">Определяет уровень сжатия для применения к вложениям изображений.</span><span class="sxs-lookup"><span data-stu-id="f6e78-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6e78-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f6e78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6e78-107">dispidImgAttchmtsCompressLevel</span><span class="sxs-lookup"><span data-stu-id="f6e78-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="f6e78-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="f6e78-108">Property set:</span></span>  <br/> |<span data-ttu-id="f6e78-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f6e78-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f6e78-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="f6e78-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f6e78-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="f6e78-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="f6e78-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f6e78-112">Data type:</span></span>  <br/> |<span data-ttu-id="f6e78-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f6e78-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f6e78-114">Область:</span><span class="sxs-lookup"><span data-stu-id="f6e78-114">Area:</span></span>  <br/> |<span data-ttu-id="f6e78-115">Настройка времени запуска</span><span class="sxs-lookup"><span data-stu-id="f6e78-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6e78-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f6e78-116">Remarks</span></span>

<span data-ttu-id="f6e78-117">Допустимые уровни сжатия:</span><span class="sxs-lookup"><span data-stu-id="f6e78-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="f6e78-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f6e78-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f6e78-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f6e78-119">Protocol specifications</span></span>

<span data-ttu-id="f6e78-120">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="f6e78-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="f6e78-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="f6e78-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f6e78-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="f6e78-122">Header files</span></span>

<span data-ttu-id="f6e78-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6e78-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6e78-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f6e78-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6e78-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f6e78-125">See also</span></span>



[<span data-ttu-id="f6e78-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f6e78-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6e78-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f6e78-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6e78-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f6e78-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6e78-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f6e78-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

