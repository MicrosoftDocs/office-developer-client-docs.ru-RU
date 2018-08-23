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
ms.openlocfilehash: 1602d1753d9f7f6e6f407a85dab0a33255db7aae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585789"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="369af-103">Каноническое свойство PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="369af-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="369af-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="369af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="369af-105">Содержит объект отображения внедренных в таблице.</span><span class="sxs-lookup"><span data-stu-id="369af-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="369af-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="369af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="369af-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="369af-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="369af-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="369af-108">Identifier:</span></span>  <br/> |<span data-ttu-id="369af-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="369af-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="369af-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="369af-110">Data type:</span></span>  <br/> |<span data-ttu-id="369af-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="369af-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="369af-112">Область:</span><span class="sxs-lookup"><span data-stu-id="369af-112">Area:</span></span>  <br/> |<span data-ttu-id="369af-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="369af-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="369af-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="369af-114">Remarks</span></span>

<span data-ttu-id="369af-115">Передача этого свойства в метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для объекта возвращает [IMAPITable](imapitableiunknown.md) интерфейс, который позволяет создавать в таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="369af-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="369af-116">Эта таблица MAPI используется для отображения свойств для объекта адресной книги в ответ на вызов [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="369af-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="369af-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="369af-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="369af-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="369af-118">Header files</span></span>

<span data-ttu-id="369af-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="369af-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="369af-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="369af-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="369af-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="369af-121">Mapitags.h</span></span>
  
> <span data-ttu-id="369af-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="369af-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="369af-123">См. также</span><span class="sxs-lookup"><span data-stu-id="369af-123">See also</span></span>



[<span data-ttu-id="369af-124">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="369af-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="369af-125">Каноническое свойство PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="369af-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="369af-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="369af-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="369af-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="369af-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="369af-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="369af-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="369af-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="369af-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

