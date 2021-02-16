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
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424506"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a><span data-ttu-id="f95bc-103">Каноническое свойство PidTagAccessControlListTable</span><span class="sxs-lookup"><span data-stu-id="f95bc-103">PidTagAccessControlListTable Canonical Property</span></span>

  
  
<span data-ttu-id="f95bc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f95bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f95bc-105">Содержит таблицу, состоящую из всех системных списков управления доступом (SACL), применяемых к папке.</span><span class="sxs-lookup"><span data-stu-id="f95bc-105">Contains a table that consists of all the system access control lists (SACL) applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f95bc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f95bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f95bc-107">PR_ACL_TABLE</span><span class="sxs-lookup"><span data-stu-id="f95bc-107">PR_ACL_TABLE</span></span>  <br/> |
|<span data-ttu-id="f95bc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f95bc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f95bc-109">0x3FE0</span><span class="sxs-lookup"><span data-stu-id="f95bc-109">0x3FE0</span></span>  <br/> |
|<span data-ttu-id="f95bc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f95bc-110">Data type:</span></span>  <br/> |<span data-ttu-id="f95bc-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="f95bc-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="f95bc-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f95bc-112">Area:</span></span>  <br/> |<span data-ttu-id="f95bc-113">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="f95bc-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f95bc-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f95bc-114">Remarks</span></span>

<span data-ttu-id="f95bc-115">Это свойство присутствует во всех объектах папок на Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f95bc-115">This property is present on all folder objects on an Exchange Server.</span></span> <span data-ttu-id="f95bc-116">Значения, включенные в это свойство, используются для чтения и изменения списков управления доступом (ALS) для папок.</span><span class="sxs-lookup"><span data-stu-id="f95bc-116">Values included in this property are used for reading and modifying access control lists (ACLs) on folders.</span></span> <span data-ttu-id="f95bc-117">Вы можете использовать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с **идентификатором интерфейса IID_IExchangeModifyTable** для получения интерфейса [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) в таблице ACL в папке.</span><span class="sxs-lookup"><span data-stu-id="f95bc-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the ACL table on a folder.</span></span> <span data-ttu-id="f95bc-118">Этот интерфейс можно использовать для чтения и изменения этих ALS.</span><span class="sxs-lookup"><span data-stu-id="f95bc-118">You can use this interface to read and modify those ACLs.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f95bc-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f95bc-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f95bc-120">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="f95bc-120">Header files</span></span>

<span data-ttu-id="f95bc-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f95bc-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="f95bc-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f95bc-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="f95bc-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f95bc-123">Mapitags.h</span></span>
  
> <span data-ttu-id="f95bc-124">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="f95bc-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f95bc-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f95bc-125">See also</span></span>



[<span data-ttu-id="f95bc-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f95bc-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f95bc-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f95bc-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f95bc-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f95bc-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f95bc-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f95bc-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

