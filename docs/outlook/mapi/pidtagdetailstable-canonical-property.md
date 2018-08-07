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
ms.openlocfilehash: a267f9a9fb8d97256cf7a448b453d04db2118180
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811055"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="7b9fd-103">Каноническое свойство PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="7b9fd-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="7b9fd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b9fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b9fd-105">Содержит объект отображения внедренных в таблице.</span><span class="sxs-lookup"><span data-stu-id="7b9fd-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b9fd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7b9fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b9fd-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="7b9fd-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="7b9fd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7b9fd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b9fd-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="7b9fd-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="7b9fd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7b9fd-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b9fd-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="7b9fd-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="7b9fd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7b9fd-112">Area:</span></span>  <br/> |<span data-ttu-id="7b9fd-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="7b9fd-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b9fd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b9fd-114">Remarks</span></span>

<span data-ttu-id="7b9fd-115">Передача этого свойства в метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для объекта возвращает [IMAPITable](imapitableiunknown.md) интерфейс, который позволяет создавать в таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="7b9fd-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="7b9fd-116">Эта таблица MAPI используется для отображения свойств для объекта адресной книги в ответ на вызов [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="7b9fd-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7b9fd-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7b9fd-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7b9fd-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7b9fd-118">Header files</span></span>

<span data-ttu-id="7b9fd-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b9fd-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b9fd-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7b9fd-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b9fd-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7b9fd-121">Mapitags.h</span></span>
  
> <span data-ttu-id="7b9fd-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="7b9fd-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b9fd-123">См. также</span><span class="sxs-lookup"><span data-stu-id="7b9fd-123">See also</span></span>



[<span data-ttu-id="7b9fd-124">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="7b9fd-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="7b9fd-125">Каноническое свойство PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="7b9fd-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="7b9fd-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b9fd-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b9fd-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7b9fd-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b9fd-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7b9fd-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b9fd-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7b9fd-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

