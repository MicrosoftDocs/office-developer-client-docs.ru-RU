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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357584"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a><span data-ttu-id="3c601-103">Каноническое свойство PidLidImageAttachmentsCompressionLevel</span><span class="sxs-lookup"><span data-stu-id="3c601-103">PidLidImageAttachmentsCompressionLevel Canonical Property</span></span>

  
  
<span data-ttu-id="3c601-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c601-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c601-105">Определяет уровень сжатия, применяемый к вложениям с изображениями.</span><span class="sxs-lookup"><span data-stu-id="3c601-105">Defines a compression level to apply on image attachments.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c601-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3c601-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c601-107">Диспидимгаттчмтскомпресслевел</span><span class="sxs-lookup"><span data-stu-id="3c601-107">dispidImgAttchmtsCompressLevel</span></span>  <br/> |
|<span data-ttu-id="3c601-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="3c601-108">Property set:</span></span>  <br/> |<span data-ttu-id="3c601-109">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="3c601-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="3c601-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="3c601-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3c601-111">0x00008593</span><span class="sxs-lookup"><span data-stu-id="3c601-111">0x00008593</span></span>  <br/> |
|<span data-ttu-id="3c601-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3c601-112">Data type:</span></span>  <br/> |<span data-ttu-id="3c601-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3c601-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3c601-114">Область:</span><span class="sxs-lookup"><span data-stu-id="3c601-114">Area:</span></span>  <br/> |<span data-ttu-id="3c601-115">Настройка времени выполнения</span><span class="sxs-lookup"><span data-stu-id="3c601-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c601-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c601-116">Remarks</span></span>

<span data-ttu-id="3c601-117">Ниже приведены допустимые уровни сжатия:</span><span class="sxs-lookup"><span data-stu-id="3c601-117">The following are valid compression levels:</span></span>
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a><span data-ttu-id="3c601-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3c601-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c601-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3c601-119">Protocol specifications</span></span>

<span data-ttu-id="3c601-120">[[MS — ОКСПРОПС]]</span><span class="sxs-lookup"><span data-stu-id="3c601-120">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="3c601-121">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3c601-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c601-122">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="3c601-122">Header files</span></span>

<span data-ttu-id="3c601-123">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3c601-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c601-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3c601-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c601-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3c601-125">See also</span></span>



[<span data-ttu-id="3c601-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3c601-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c601-127">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="3c601-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c601-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3c601-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c601-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3c601-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

