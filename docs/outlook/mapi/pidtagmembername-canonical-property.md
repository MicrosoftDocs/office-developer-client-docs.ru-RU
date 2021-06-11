---
title: Каноническое свойство PidTagMemberName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberName
api_type:
- HeaderDef
ms.assetid: e19129bf-d07c-4d2e-9d4d-edbfda088ea7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342485"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="b9a9f-103">Каноническое свойство PidTagMemberName</span><span class="sxs-lookup"><span data-stu-id="b9a9f-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="b9a9f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9a9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9a9f-105">Содержит отображаемую фамилию члена таблицы управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="b9a9f-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9a9f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b9a9f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9a9f-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="b9a9f-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="b9a9f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b9a9f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9a9f-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="b9a9f-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="b9a9f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b9a9f-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9a9f-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b9a9f-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="b9a9f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b9a9f-112">Area:</span></span>  <br/> |<span data-ttu-id="b9a9f-113">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="b9a9f-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9a9f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9a9f-114">Remarks</span></span>

<span data-ttu-id="b9a9f-115">Эти свойства используются [интерфейсом IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) для отображения имени члена таблицы ACL, который является лицом или ролью с явными правами на папку или почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="b9a9f-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b9a9f-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b9a9f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b9a9f-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b9a9f-117">Protocol specifications</span></span>

<span data-ttu-id="b9a9f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9a9f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9a9f-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="b9a9f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b9a9f-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9a9f-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9a9f-121">Обрабатывает ирисовку списков разрешений папок, хранимых на сервере.</span><span class="sxs-lookup"><span data-stu-id="b9a9f-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b9a9f-122">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="b9a9f-122">Header files</span></span>

<span data-ttu-id="b9a9f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9a9f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9a9f-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b9a9f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9a9f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b9a9f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b9a9f-126">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="b9a9f-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9a9f-127">См. также</span><span class="sxs-lookup"><span data-stu-id="b9a9f-127">See also</span></span>



[<span data-ttu-id="b9a9f-128">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9a9f-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="b9a9f-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b9a9f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9a9f-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b9a9f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9a9f-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b9a9f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9a9f-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="b9a9f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

