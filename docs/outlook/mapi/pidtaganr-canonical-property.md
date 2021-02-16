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
# <a name="pidtaganr-canonical-property"></a><span data-ttu-id="c2f64-103">Каноническое свойство PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="c2f64-103">PidTagAnr Canonical Property</span></span>

  
  
<span data-ttu-id="c2f64-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2f64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2f64-105">Содержит строку, используемую в ограничении свойств для таблицы содержимого контейнера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c2f64-105">Contains a string value for use in a property restriction on an address book container contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2f64-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c2f64-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2f64-107">PR_ANR, PR_ANR_A, PR_ANR_W</span><span class="sxs-lookup"><span data-stu-id="c2f64-107">PR_ANR, PR_ANR_A, PR_ANR_W</span></span>  <br/> |
|<span data-ttu-id="c2f64-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c2f64-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2f64-109">0x360C</span><span class="sxs-lookup"><span data-stu-id="c2f64-109">0x360C</span></span>  <br/> |
|<span data-ttu-id="c2f64-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c2f64-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2f64-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c2f64-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c2f64-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c2f64-112">Area:</span></span>  <br/> |<span data-ttu-id="c2f64-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="c2f64-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2f64-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c2f64-114">Remarks</span></span>

<span data-ttu-id="c2f64-115">Эти свойства не принадлежат ни одному объекту; она предоставлена поставщиками адресных книг в [структурах SPropertyRestriction.](spropertyrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="c2f64-115">These properties do not belong to any object; it is furnished by address book providers in [SPropertyRestriction](spropertyrestriction.md) structures.</span></span> <span data-ttu-id="c2f64-116">Это свойство содержит строку разрешения неоднозначных имен (ANR), которую можно проверить с таблицей содержимого контейнера адресной книги, чтобы найти соответствующих получателей сообщений.</span><span class="sxs-lookup"><span data-stu-id="c2f64-116">This property contains an ambiguous name resolution (ANR) string that can be tested against an address book container's contents table to find corresponding message recipients.</span></span> 
  
<span data-ttu-id="c2f64-117">Поставщики адресных книг  соответствуют значению PR_ANR и связанным свойствам для каждой записи в таблице содержимого с помощью определенного поставщиком алгоритма совпадения.</span><span class="sxs-lookup"><span data-stu-id="c2f64-117">Address book providers match the value of **PR_ANR** and associated properties against every entry in the contents table, using a provider-defined matching algorithm.</span></span> <span data-ttu-id="c2f64-118">Столбцы или столбцы, используемые в этом совпадении, выбираются поставщиком в рамках алгоритма.</span><span class="sxs-lookup"><span data-stu-id="c2f64-118">The column or columns that are used in this match are chosen by the provider as part of the algorithm.</span></span> <span data-ttu-id="c2f64-119">Столбец **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)является наиболее часто используемым; Столбец **PR_ACCOUNT** [(PidTagAccount)](pidtagaccount-canonical-property.md)также полезен, если он содержит имя электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2f64-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column is the most commonly used; the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) column is also useful when it contains the user's email name.</span></span> 
  
<span data-ttu-id="c2f64-120">Дополнительные сведения об разрешении неоднозначных имен см. в сведениях [об ограничениях адресной книги.](address-book-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="c2f64-120">For more information on ambiguous name resolution, see [Address Book Restrictions](address-book-restrictions.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c2f64-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c2f64-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c2f64-122">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c2f64-122">Protocol specifications</span></span>

<span data-ttu-id="c2f64-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2f64-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2f64-124">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="c2f64-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c2f64-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2f64-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2f64-126">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2f64-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c2f64-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="c2f64-127">Header files</span></span>

<span data-ttu-id="c2f64-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2f64-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2f64-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c2f64-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="c2f64-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c2f64-130">Mapitags.h</span></span>
  
> <span data-ttu-id="c2f64-131">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="c2f64-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2f64-132">См. также</span><span class="sxs-lookup"><span data-stu-id="c2f64-132">See also</span></span>



[<span data-ttu-id="c2f64-133">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="c2f64-133">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="c2f64-134">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="c2f64-134">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="c2f64-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c2f64-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2f64-136">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c2f64-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2f64-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c2f64-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2f64-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c2f64-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

