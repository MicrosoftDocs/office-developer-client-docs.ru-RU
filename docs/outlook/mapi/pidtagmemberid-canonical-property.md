---
title: Каноническое свойство PidTagMemberId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ce6925f40e09261494e4edbcbd7314728debbe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811362"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="e1de8-103">Каноническое свойство PidTagMemberId</span><span class="sxs-lookup"><span data-stu-id="e1de8-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="e1de8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1de8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1de8-105">Содержит идентификатор элемента в таблице, имеющей описано права на почтового ящика или папки Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e1de8-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1de8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e1de8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1de8-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="e1de8-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="e1de8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e1de8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1de8-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="e1de8-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="e1de8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e1de8-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1de8-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="e1de8-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="e1de8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e1de8-112">Area:</span></span>  <br/> |<span data-ttu-id="e1de8-113">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="e1de8-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1de8-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e1de8-114">Remarks</span></span>

<span data-ttu-id="e1de8-115">Данное свойство возвращает уникальный идентификатор в таблицу.</span><span class="sxs-lookup"><span data-stu-id="e1de8-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="e1de8-116">Идентификатор пользователя каталог связан с каждой идентификатор элемента и заданную с помощью этого свойства.</span><span class="sxs-lookup"><span data-stu-id="e1de8-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="e1de8-117">Это свойство используется интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) получить идентификатор записи каталога элемента с помощью явных права на папку.</span><span class="sxs-lookup"><span data-stu-id="e1de8-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e1de8-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e1de8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1de8-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e1de8-119">Protocol specifications</span></span>

<span data-ttu-id="e1de8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1de8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1de8-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e1de8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1de8-122">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1de8-122">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1de8-123">Обрабатывает извлечения списков разрешений папки, которые хранятся на сервере.</span><span class="sxs-lookup"><span data-stu-id="e1de8-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1de8-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e1de8-124">Header files</span></span>

<span data-ttu-id="e1de8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1de8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1de8-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e1de8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1de8-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1de8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e1de8-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e1de8-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1de8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e1de8-129">See also</span></span>



[<span data-ttu-id="e1de8-130">Каноническое свойство PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="e1de8-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="e1de8-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e1de8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1de8-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e1de8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1de8-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e1de8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1de8-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e1de8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

