---
title: Каноническое свойство PidTagMemberEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3139f7cc60d19048fb17c64101f279ce377e9b26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811354"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="21271-103">Каноническое свойство PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="21271-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="21271-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21271-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21271-105">Содержит идентификатор каталога объект запись члена в таблице список управления ДОСТУПОМ системы доступа элемента управления.</span><span class="sxs-lookup"><span data-stu-id="21271-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21271-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="21271-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21271-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="21271-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="21271-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="21271-108">Identifier:</span></span>  <br/> |<span data-ttu-id="21271-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="21271-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="21271-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="21271-110">Data type:</span></span>  <br/> |<span data-ttu-id="21271-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="21271-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="21271-112">Область:</span><span class="sxs-lookup"><span data-stu-id="21271-112">Area:</span></span>  <br/> |<span data-ttu-id="21271-113">Правила со стороны сервера</span><span class="sxs-lookup"><span data-stu-id="21271-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21271-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="21271-114">Remarks</span></span>

<span data-ttu-id="21271-115">Это свойство используется интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) для уникальной идентификации лицо или роль, к которому относится список SACL.</span><span class="sxs-lookup"><span data-stu-id="21271-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="21271-116">После создания члена в таблице SACL **ENTRYID** нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="21271-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="21271-117">Чтобы изменить его, необходимо удалить элемент в таблице и повторно создать его с помощью различных **ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="21271-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="21271-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="21271-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="21271-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="21271-119">Header files</span></span>

<span data-ttu-id="21271-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21271-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="21271-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="21271-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="21271-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="21271-122">Mapitags.h</span></span>
  
> <span data-ttu-id="21271-123">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="21271-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21271-124">См. также</span><span class="sxs-lookup"><span data-stu-id="21271-124">See also</span></span>



[<span data-ttu-id="21271-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="21271-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21271-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="21271-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21271-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="21271-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21271-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="21271-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

