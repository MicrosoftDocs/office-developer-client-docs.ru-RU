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
ms.openlocfilehash: ce08ba971662b7f5060e6b24a6d2c5ee1a921d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327967"
---
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="6b192-103">Каноническое свойство PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="6b192-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="6b192-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b192-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b192-105">Содержит строковое значение, используемое в ограничении свойств в таблице содержимого контейнера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6b192-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b192-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6b192-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b192-107">PR_ANR, PR_ANR_A PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="6b192-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="6b192-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6b192-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6b192-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="6b192-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="6b192-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6b192-110">Data type:</span></span>  <br/> |<span data-ttu-id="6b192-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="6b192-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="6b192-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6b192-112">Area:</span></span>  <br/> |<span data-ttu-id="6b192-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="6b192-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b192-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b192-114">Remarks</span></span>

<span data-ttu-id="6b192-115">Эти свойства не принадлежат никаким объектам; они предоставляются поставщиками адресных книг в структурах [спропертирестриктион](spropertyrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="6b192-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="6b192-116">Данное свойство содержит строку с непонятным сопоставлением имен (ANR), которую можно проверить с помощью таблицы содержимого контейнера адресной книги, чтобы найти соответствующих получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="6b192-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="6b192-117">Поставщики адресных книг соответствуют значению **PR_ANR** и связанным свойствам каждой записи в таблице содержимого с помощью алгоритма проверки соответствия, определяемого поставщиком.</span><span class="sxs-lookup"><span data-stu-id="6b192-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="6b192-118">Столбец или столбцы, используемые в этом соотношении, выбираются поставщиком в составе алгоритма.</span><span class="sxs-lookup"><span data-stu-id="6b192-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="6b192-119">Наиболее часто используется столбец **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)); столбец **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) также полезен, если он содержит имя электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b192-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="6b192-120">Дополнительные сведения об устранении неоднозначных имен приведены в разделе [ограничения адресной книги](address-book-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="6b192-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6b192-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6b192-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6b192-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6b192-122">Protocol specifications</span></span>

<span data-ttu-id="6b192-123">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b192-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b192-124">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6b192-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6b192-125">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b192-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b192-126">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b192-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6b192-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6b192-127">Header files</span></span>

<span data-ttu-id="6b192-128">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6b192-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b192-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6b192-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="6b192-130">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="6b192-130">Mapitags.h</span></span>
  
> <span data-ttu-id="6b192-131">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="6b192-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b192-132">См. также</span><span class="sxs-lookup"><span data-stu-id="6b192-132">See also</span></span>



[<span data-ttu-id="6b192-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="6b192-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="6b192-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="6b192-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="6b192-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6b192-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b192-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="6b192-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b192-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6b192-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b192-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6b192-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

