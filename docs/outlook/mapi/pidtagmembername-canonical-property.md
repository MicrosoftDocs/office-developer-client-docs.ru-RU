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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390893"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="64fb3-103">Каноническое свойство PidTagMemberName</span><span class="sxs-lookup"><span data-stu-id="64fb3-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="64fb3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64fb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64fb3-105">Содержит отображаемое имя элемента в список управления Доступом таблицы управления доступа.</span><span class="sxs-lookup"><span data-stu-id="64fb3-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64fb3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="64fb3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64fb3-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="64fb3-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="64fb3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="64fb3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="64fb3-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="64fb3-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="64fb3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="64fb3-110">Data type:</span></span>  <br/> |<span data-ttu-id="64fb3-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="64fb3-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="64fb3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="64fb3-112">Area:</span></span>  <br/> |<span data-ttu-id="64fb3-113">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="64fb3-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64fb3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="64fb3-114">Remarks</span></span>

<span data-ttu-id="64fb3-115">Эти свойства используются [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) интерфейс для отображения имени элемента в таблицу управления Доступом, в которой — это лицо или роль с явные права на папок или почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="64fb3-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="64fb3-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="64fb3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64fb3-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="64fb3-117">Protocol specifications</span></span>

<span data-ttu-id="64fb3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64fb3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64fb3-119">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="64fb3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64fb3-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64fb3-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64fb3-121">Обрабатывает извлечения списков разрешений папки, которые хранятся на сервере.</span><span class="sxs-lookup"><span data-stu-id="64fb3-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64fb3-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="64fb3-122">Header files</span></span>

<span data-ttu-id="64fb3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64fb3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="64fb3-124">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="64fb3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="64fb3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="64fb3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="64fb3-126">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="64fb3-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64fb3-127">См. также</span><span class="sxs-lookup"><span data-stu-id="64fb3-127">See also</span></span>



[<span data-ttu-id="64fb3-128">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="64fb3-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="64fb3-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="64fb3-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64fb3-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="64fb3-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64fb3-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="64fb3-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64fb3-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="64fb3-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

