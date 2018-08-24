---
title: Каноническое свойство PidTagAccessControlListTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 40a2bc8a27ec3ce3df610b9c7364719c2b5ee750
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572790"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="837ed-103">Каноническое свойство PidTagAccessControlListTable</span><span class="sxs-lookup"><span data-stu-id="837ed-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="837ed-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="837ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="837ed-105">Содержит таблицу, состоящую из всех системы списки управления доступом (SACL) применения к папке.</span><span class="sxs-lookup"><span data-stu-id="837ed-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="837ed-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="837ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="837ed-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="837ed-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="837ed-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="837ed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="837ed-109">0x3FE0</span><span class="sxs-lookup"><span data-stu-id="837ed-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="837ed-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="837ed-110">Data type:</span></span>  <br/> |<span data-ttu-id="837ed-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="837ed-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="837ed-112">Область:</span><span class="sxs-lookup"><span data-stu-id="837ed-112">Area:</span></span>  <br/> |<span data-ttu-id="837ed-113">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="837ed-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="837ed-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="837ed-114">Remarks</span></span>

<span data-ttu-id="837ed-115">Это свойство присутствует на всех объектов папок на сервере Exchange.</span><span class="sxs-lookup"><span data-stu-id="837ed-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="837ed-116">Значения, включенные в этом свойстве используются для чтения, и изменение управления доступом списков управления доступом к папкам.</span><span class="sxs-lookup"><span data-stu-id="837ed-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="837ed-117">Можно использовать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатором интерфейса **IID_IExchangeModifyTable** для получения [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) интерфейса в таблице списка управления Доступом на папку.</span><span class="sxs-lookup"><span data-stu-id="837ed-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="837ed-118">Этот интерфейс можно использовать для чтения и изменения эти списки управления доступом.</span><span class="sxs-lookup"><span data-stu-id="837ed-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="837ed-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="837ed-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="837ed-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="837ed-120">Header files</span></span>

<span data-ttu-id="837ed-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="837ed-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="837ed-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="837ed-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="837ed-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="837ed-123">Mapitags.h</span></span>
  
> <span data-ttu-id="837ed-124">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="837ed-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="837ed-125">См. также</span><span class="sxs-lookup"><span data-stu-id="837ed-125">See also</span></span>



[<span data-ttu-id="837ed-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="837ed-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="837ed-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="837ed-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="837ed-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="837ed-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="837ed-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="837ed-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

