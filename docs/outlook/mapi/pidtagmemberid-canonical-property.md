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
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="c22c3-103">Каноническое свойство PidTagMemberId</span><span class="sxs-lookup"><span data-stu-id="c22c3-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="c22c3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c22c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c22c3-105">Содержит идентификатор элемента таблицы, который имеет описанные права для папки или почтового ящика Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c22c3-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c22c3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c22c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c22c3-107">ПР_МЕМБЕР_ИД</span><span class="sxs-lookup"><span data-stu-id="c22c3-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="c22c3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c22c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c22c3-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="c22c3-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="c22c3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c22c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="c22c3-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="c22c3-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="c22c3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c22c3-112">Area:</span></span>  <br/> |<span data-ttu-id="c22c3-113">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="c22c3-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c22c3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c22c3-114">Remarks</span></span>

<span data-ttu-id="c22c3-115">Это свойство возвращает идентификатор, уникальный для таблицы.</span><span class="sxs-lookup"><span data-stu-id="c22c3-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="c22c3-116">Идентификатор пользователя каталога связан с каждым идентификатором элемента и задается этим свойством.</span><span class="sxs-lookup"><span data-stu-id="c22c3-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="c22c3-117">Это свойство используется интерфейсом [иексчанжемодифитабле](iexchangemodifytableiunknown.md) для получения идентификатора записи каталога члена с явными правами на папку.</span><span class="sxs-lookup"><span data-stu-id="c22c3-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c22c3-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c22c3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c22c3-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c22c3-119">Protocol specifications</span></span>

<span data-ttu-id="c22c3-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c22c3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c22c3-121">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c22c3-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c22c3-122">[[MS — ОКСКПЕРМ]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c22c3-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c22c3-123">Обрабатывает получение списков разрешений на доступ к папкам, которые хранятся на сервере.</span><span class="sxs-lookup"><span data-stu-id="c22c3-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c22c3-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="c22c3-124">Header files</span></span>

<span data-ttu-id="c22c3-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c22c3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c22c3-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c22c3-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c22c3-127">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="c22c3-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c22c3-128">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="c22c3-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c22c3-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c22c3-129">See also</span></span>



[<span data-ttu-id="c22c3-130">Каноническое свойство PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="c22c3-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="c22c3-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c22c3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c22c3-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c22c3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c22c3-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c22c3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c22c3-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c22c3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

