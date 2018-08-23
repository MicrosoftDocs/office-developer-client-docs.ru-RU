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
ms.openlocfilehash: caf1cb2e16c298af452e638631293379fdd68b10
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589786"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="0558d-103">Каноническое свойство PidTagMemberId</span><span class="sxs-lookup"><span data-stu-id="0558d-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="0558d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0558d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0558d-105">Содержит идентификатор элемента в таблице, имеющей описано права на почтового ящика или папки Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0558d-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0558d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0558d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0558d-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="0558d-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="0558d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0558d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0558d-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="0558d-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="0558d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0558d-110">Data type:</span></span>  <br/> |<span data-ttu-id="0558d-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="0558d-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="0558d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0558d-112">Area:</span></span>  <br/> |<span data-ttu-id="0558d-113">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="0558d-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0558d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="0558d-114">Remarks</span></span>

<span data-ttu-id="0558d-115">Данное свойство возвращает уникальный идентификатор в таблицу.</span><span class="sxs-lookup"><span data-stu-id="0558d-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="0558d-116">Идентификатор пользователя каталог связан с каждой идентификатор элемента и заданную с помощью этого свойства.</span><span class="sxs-lookup"><span data-stu-id="0558d-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="0558d-117">Это свойство используется интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) получить идентификатор записи каталога элемента с помощью явных права на папку.</span><span class="sxs-lookup"><span data-stu-id="0558d-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0558d-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0558d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0558d-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0558d-119">Protocol specifications</span></span>

<span data-ttu-id="0558d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0558d-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0558d-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0558d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0558d-122">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0558d-122">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0558d-123">Обрабатывает извлечения списков разрешений папки, которые хранятся на сервере.</span><span class="sxs-lookup"><span data-stu-id="0558d-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0558d-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0558d-124">Header files</span></span>

<span data-ttu-id="0558d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0558d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0558d-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0558d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0558d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0558d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0558d-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0558d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0558d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0558d-129">See also</span></span>



[<span data-ttu-id="0558d-130">Каноническое свойство PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="0558d-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="0558d-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0558d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0558d-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0558d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0558d-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0558d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0558d-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0558d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

