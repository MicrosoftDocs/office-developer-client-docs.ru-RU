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
ms.openlocfilehash: b5d1d4456856f1640bbed8589fc0583060cd2520
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342639"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="e179e-103">Каноническое свойство PidTagMemberId</span><span class="sxs-lookup"><span data-stu-id="e179e-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="e179e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e179e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e179e-105">Содержит идентификатор члена таблицы с описанными правами на Microsoft Exchange Server папке или почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="e179e-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e179e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e179e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e179e-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="e179e-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="e179e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e179e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e179e-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="e179e-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="e179e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e179e-110">Data type:</span></span>  <br/> |<span data-ttu-id="e179e-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="e179e-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="e179e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e179e-112">Area:</span></span>  <br/> |<span data-ttu-id="e179e-113">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="e179e-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e179e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e179e-114">Remarks</span></span>

<span data-ttu-id="e179e-115">Это свойство возвращает уникальный идентификатор таблицы.</span><span class="sxs-lookup"><span data-stu-id="e179e-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="e179e-116">Идентификатор пользователя каталога связан с каждым идентификатором участника и задается этим свойством.</span><span class="sxs-lookup"><span data-stu-id="e179e-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="e179e-117">Это свойство используется интерфейсом [IExchangeModifyTable](iexchangemodifytableiunknown.md) для получения идентификатора записи каталога члена с явными правами на папку.</span><span class="sxs-lookup"><span data-stu-id="e179e-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e179e-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e179e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e179e-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e179e-119">Protocol specifications</span></span>

<span data-ttu-id="e179e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e179e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e179e-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="e179e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e179e-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e179e-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e179e-123">Обрабатывает и получить списки разрешений папок, хранимые на сервере.</span><span class="sxs-lookup"><span data-stu-id="e179e-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e179e-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="e179e-124">Header files</span></span>

<span data-ttu-id="e179e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e179e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e179e-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e179e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e179e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e179e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e179e-128">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e179e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e179e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e179e-129">See also</span></span>



[<span data-ttu-id="e179e-130">Каноническое свойство PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="e179e-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="e179e-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e179e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e179e-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e179e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e179e-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e179e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e179e-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e179e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

