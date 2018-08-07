---
title: Каноническое свойство PidTagContactAddressBookMultipleAddressFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fbe955d3e7a509edf6ba10678e1e2538c9185193
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810939"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="a4212-103">Каноническое свойство PidTagContactAddressBookMultipleAddressFlags</span><span class="sxs-lookup"><span data-stu-id="a4212-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="a4212-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4212-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4212-105">Содержит флаги, указывающее, поддерживает ли поставщики нескольких электронной почты решает каждого элемента контакта.</span><span class="sxs-lookup"><span data-stu-id="a4212-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4212-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a4212-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4212-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a4212-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="a4212-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a4212-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4212-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="a4212-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="a4212-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a4212-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4212-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="a4212-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="a4212-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a4212-112">Area:</span></span>  <br/> |<span data-ttu-id="a4212-113">Адресная книга контактов</span><span class="sxs-lookup"><span data-stu-id="a4212-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4212-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a4212-114">Remarks</span></span>

<span data-ttu-id="a4212-115">Если флаги в этом свойстве значение TRUE, поставщик не включает контакты без адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a4212-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="a4212-116">Будет учитываться только основной адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a4212-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="a4212-117">Это свойство в разделе профилей контактов адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a4212-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a4212-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a4212-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a4212-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a4212-119">Header files</span></span>

<span data-ttu-id="a4212-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4212-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4212-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a4212-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="a4212-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a4212-122">Mapitags.h</span></span>
  
> <span data-ttu-id="a4212-123">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="a4212-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4212-124">См. также</span><span class="sxs-lookup"><span data-stu-id="a4212-124">See also</span></span>



[<span data-ttu-id="a4212-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a4212-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4212-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a4212-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4212-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a4212-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4212-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a4212-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

