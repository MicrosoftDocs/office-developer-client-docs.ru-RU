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
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433040"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="994be-103">Каноническое свойство PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="994be-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="994be-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="994be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="994be-105">Содержит идентификатор записи объекта каталога для элемента таблицы списка управления доступом системы (SACL).</span><span class="sxs-lookup"><span data-stu-id="994be-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="994be-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="994be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="994be-107">ПР_МЕМБЕР_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="994be-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="994be-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="994be-108">Identifier:</span></span>  <br/> |<span data-ttu-id="994be-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="994be-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="994be-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="994be-110">Data type:</span></span>  <br/> |<span data-ttu-id="994be-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="994be-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="994be-112">Область:</span><span class="sxs-lookup"><span data-stu-id="994be-112">Area:</span></span>  <br/> |<span data-ttu-id="994be-113">Правила на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="994be-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="994be-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="994be-114">Remarks</span></span>

<span data-ttu-id="994be-115">Это свойство используется интерфейсом [иексчанжемодифитабле](iexchangemodifytableiunknown.md) для уникальной идентификации пользователя или роли, к которым применяется SACL.</span><span class="sxs-lookup"><span data-stu-id="994be-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="994be-116">После создания члена в таблице SACL изменить значение **EntryID** невозможно.</span><span class="sxs-lookup"><span data-stu-id="994be-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="994be-117">Чтобы изменить его, необходимо удалить элемент Table и повторно создать его с другим идентификатором **EntryID**.</span><span class="sxs-lookup"><span data-stu-id="994be-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="994be-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="994be-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="994be-119">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="994be-119">Header files</span></span>

<span data-ttu-id="994be-120">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="994be-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="994be-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="994be-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="994be-122">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="994be-122">Mapitags.h</span></span>
  
> <span data-ttu-id="994be-123">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="994be-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="994be-124">См. также</span><span class="sxs-lookup"><span data-stu-id="994be-124">See also</span></span>



[<span data-ttu-id="994be-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="994be-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="994be-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="994be-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="994be-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="994be-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="994be-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="994be-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

