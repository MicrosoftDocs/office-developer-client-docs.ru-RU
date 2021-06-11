---
title: Каноническое свойство PidTagDetailsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419256"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="02e42-103">Каноническое свойство PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="02e42-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="02e42-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02e42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02e42-105">Содержит встроенный объект таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="02e42-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02e42-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="02e42-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02e42-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="02e42-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="02e42-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="02e42-108">Identifier:</span></span>  <br/> |<span data-ttu-id="02e42-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="02e42-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="02e42-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="02e42-110">Data type:</span></span>  <br/> |<span data-ttu-id="02e42-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="02e42-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="02e42-112">Область:</span><span class="sxs-lookup"><span data-stu-id="02e42-112">Area:</span></span>  <br/> |<span data-ttu-id="02e42-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="02e42-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02e42-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="02e42-114">Remarks</span></span>

<span data-ttu-id="02e42-115">Передача этого свойства методу [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для объекта возвращает [интерфейс IMAPITable,](imapitableiunknown.md) который позволяет создавать таблицу отображения.</span><span class="sxs-lookup"><span data-stu-id="02e42-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="02e42-116">MAPI использует эту таблицу для отображения листов свойств объекта адресной книги в ответ на вызов [IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="02e42-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="02e42-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="02e42-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="02e42-118">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="02e42-118">Header files</span></span>

<span data-ttu-id="02e42-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02e42-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="02e42-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="02e42-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="02e42-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="02e42-121">Mapitags.h</span></span>
  
> <span data-ttu-id="02e42-122">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="02e42-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02e42-123">См. также</span><span class="sxs-lookup"><span data-stu-id="02e42-123">See also</span></span>



[<span data-ttu-id="02e42-124">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="02e42-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="02e42-125">Каноническое свойство PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="02e42-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="02e42-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02e42-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02e42-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02e42-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02e42-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="02e42-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02e42-129">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="02e42-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

