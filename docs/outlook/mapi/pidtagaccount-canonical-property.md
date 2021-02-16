---
title: Каноническое свойство PidTagAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359782"
---
# <a name="pidtagaccount-canonical-property"></a><span data-ttu-id="84f6c-103">Каноническое свойство PidTagAccount</span><span class="sxs-lookup"><span data-stu-id="84f6c-103">PidTagAccount Canonical Property</span></span>

  
  
<span data-ttu-id="84f6c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84f6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84f6c-105">Содержит имя учетной записи получателя.</span><span class="sxs-lookup"><span data-stu-id="84f6c-105">Contains the recipient's account name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84f6c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="84f6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84f6c-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span><span class="sxs-lookup"><span data-stu-id="84f6c-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span></span>  <br/> |
|<span data-ttu-id="84f6c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="84f6c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84f6c-109">0x3A00</span><span class="sxs-lookup"><span data-stu-id="84f6c-109">0x3A00</span></span>  <br/> |
|<span data-ttu-id="84f6c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="84f6c-110">Data type:</span></span>  <br/> |<span data-ttu-id="84f6c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="84f6c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="84f6c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="84f6c-112">Area:</span></span>  <br/> |<span data-ttu-id="84f6c-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="84f6c-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84f6c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="84f6c-114">Remarks</span></span>

<span data-ttu-id="84f6c-115">Эти свойства предоставляют сведения об идентификации и доступе для получателя.</span><span class="sxs-lookup"><span data-stu-id="84f6c-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="84f6c-116">Они определяются получателем и его организацией.</span><span class="sxs-lookup"><span data-stu-id="84f6c-116">They are defined by the recipient and their organization.</span></span>
  
<span data-ttu-id="84f6c-117">Эти свойства обычно содержат имя электронной почты получателя, то есть конечный компонент адреса электронной почты, который уникальным образом идентифицирует получателя в локальной организации.</span><span class="sxs-lookup"><span data-stu-id="84f6c-117">These properties commonly contain the recipient's email name, that is, the final component of the email address, which uniquely identifies the recipient in the local organization.</span></span> <span data-ttu-id="84f6c-118">Имя электронной почты соответствует различаемого имени X.400, которое должно быть коротким именем, гарантированно уникальным в пределах определенного домена обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="84f6c-118">The email name corresponds to the X.400 distinguished name, which is meant to be a short name guaranteed to be unique within a certain messaging domain.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84f6c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="84f6c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84f6c-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="84f6c-120">Protocol specifications</span></span>

<span data-ttu-id="84f6c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84f6c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84f6c-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="84f6c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84f6c-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84f6c-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84f6c-124">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="84f6c-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="84f6c-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84f6c-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84f6c-126">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84f6c-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84f6c-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="84f6c-127">Header files</span></span>

<span data-ttu-id="84f6c-128">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84f6c-128">mapitags.h</span></span>
  
> <span data-ttu-id="84f6c-129">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="84f6c-129">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="84f6c-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84f6c-130">mapidefs.h</span></span>
  
> <span data-ttu-id="84f6c-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="84f6c-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84f6c-132">См. также</span><span class="sxs-lookup"><span data-stu-id="84f6c-132">See also</span></span>



[<span data-ttu-id="84f6c-133">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="84f6c-133">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)


[<span data-ttu-id="84f6c-134">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="84f6c-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84f6c-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="84f6c-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84f6c-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="84f6c-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

