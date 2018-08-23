---
title: Каноническое свойство PidTagAnr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAnr
api_type:
- HeaderDef
ms.assetid: eca3d4ff-2e92-4d20-a498-98e0773c1962
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6cc5edf1c93ca94fb9d8cab302ccd8e96373cd94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581946"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="27382-103">Каноническое свойство PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="27382-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="27382-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27382-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27382-105">Содержит значение строки для использования в качестве свойства ограничения на содержимое таблицы контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="27382-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27382-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="27382-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27382-107">PR_ANR, PR_ANR_A, PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="27382-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="27382-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="27382-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27382-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="27382-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="27382-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="27382-110">Data type:</span></span>  <br/> |<span data-ttu-id="27382-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="27382-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="27382-112">Область:</span><span class="sxs-lookup"><span data-stu-id="27382-112">Area:</span></span>  <br/> |<span data-ttu-id="27382-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="27382-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27382-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="27382-114">Remarks</span></span>

<span data-ttu-id="27382-115">Эти свойства не принадлежат каждого объекта; Он поставляется с поставщиками адресной книги в [SPropertyRestriction](spropertyrestriction.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="27382-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="27382-116">Это свойство содержит строку решение (ANR) неоднозначное имя, которое можно проверить на таблицу содержимого контейнер адресной книги для поиска соответствующего получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="27382-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="27382-117">Поставщиками адресных книг соответствует значению **PR_ANR** и связанными свойствами для каждой записи в таблице содержимое с помощью соответствующего алгоритма, определяемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="27382-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="27382-118">Столбец или столбцы, которые используются в этом сопоставлении выбираются поставщиком как часть алгоритм.</span><span class="sxs-lookup"><span data-stu-id="27382-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="27382-119">Наиболее часто используется в столбце **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)); в столбце **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) также полезна, если оно содержит имя электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="27382-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="27382-120">Дополнительные сведения о разрешения неоднозначных псевдонимов видеть [Ограничения адресной книги](address-book-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="27382-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="27382-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="27382-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27382-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="27382-122">Protocol specifications</span></span>

<span data-ttu-id="27382-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27382-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27382-124">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="27382-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27382-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27382-125">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27382-126">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27382-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27382-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="27382-127">Header files</span></span>

<span data-ttu-id="27382-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27382-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="27382-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="27382-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="27382-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="27382-130">Mapitags.h</span></span>
  
> <span data-ttu-id="27382-131">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="27382-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27382-132">См. также</span><span class="sxs-lookup"><span data-stu-id="27382-132">See also</span></span>



[<span data-ttu-id="27382-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="27382-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="27382-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="27382-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="27382-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="27382-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27382-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="27382-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27382-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="27382-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27382-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="27382-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

