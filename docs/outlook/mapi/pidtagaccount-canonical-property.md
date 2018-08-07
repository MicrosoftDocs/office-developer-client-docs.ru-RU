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
ms.openlocfilehash: ab2efebe91f871452b243150367b83a1d53f8a52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810804"
---
# <a name="pidtagaccount-canonical-property"></a><span data-ttu-id="e2ca7-103">Каноническое свойство PidTagAccount</span><span class="sxs-lookup"><span data-stu-id="e2ca7-103">PidTagAccount Canonical Property</span></span>

  
  
<span data-ttu-id="e2ca7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2ca7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2ca7-105">Содержит имя учетной записи получателя.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-105">Contains the recipient's account name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2ca7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e2ca7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2ca7-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span><span class="sxs-lookup"><span data-stu-id="e2ca7-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span></span>  <br/> |
|<span data-ttu-id="e2ca7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e2ca7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2ca7-109">0x3A00</span><span class="sxs-lookup"><span data-stu-id="e2ca7-109">0x3A00</span></span>  <br/> |
|<span data-ttu-id="e2ca7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e2ca7-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2ca7-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2ca7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e2ca7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e2ca7-112">Area:</span></span>  <br/> |<span data-ttu-id="e2ca7-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="e2ca7-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2ca7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e2ca7-114">Remarks</span></span>

<span data-ttu-id="e2ca7-115">Эти свойства предоставляют идентификации и доступа к сведениям для получателя.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="e2ca7-116">Они определены получателя и их организации.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-116">They are defined by the recipient and their organization.</span></span>
  
<span data-ttu-id="e2ca7-117">Эти свойства обычно содержит имя электронной почты получателя, то есть, последний компонент адрес электронной почты, который уникальным образом идентифицирующее получателя в локальной организации.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-117">These properties commonly contain the recipient's email name, that is, the final component of the email address, which uniquely identifies the recipient in the local organization.</span></span> <span data-ttu-id="e2ca7-118">Имя электронной почты соответствует различающееся имя X.400, который должен быть краткое имя быть уникальным в рамках определенного домена обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-118">The email name corresponds to the X.400 distinguished name, which is meant to be a short name guaranteed to be unique within a certain messaging domain.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2ca7-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e2ca7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2ca7-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e2ca7-120">Protocol specifications</span></span>

<span data-ttu-id="e2ca7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2ca7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2ca7-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2ca7-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2ca7-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2ca7-124">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="e2ca7-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2ca7-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2ca7-126">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2ca7-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e2ca7-127">Header files</span></span>

<span data-ttu-id="e2ca7-128">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2ca7-128">mapitags.h</span></span>
  
> <span data-ttu-id="e2ca7-129">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-129">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="e2ca7-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2ca7-130">mapidefs.h</span></span>
  
> <span data-ttu-id="e2ca7-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e2ca7-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2ca7-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e2ca7-132">See also</span></span>



[<span data-ttu-id="e2ca7-133">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e2ca7-133">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)


[<span data-ttu-id="e2ca7-134">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e2ca7-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2ca7-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e2ca7-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2ca7-136">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e2ca7-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

