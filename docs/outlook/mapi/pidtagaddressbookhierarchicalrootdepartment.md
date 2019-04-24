---
title: Каноническое свойство PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326126"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="b64dd-103">Каноническое свойство PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="b64dd-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="b64dd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b64dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b64dd-105">Содержит различающееся имя (DN) иерархического корня адресов (ИЕРАРХИческой адресной книги).</span><span class="sxs-lookup"><span data-stu-id="b64dd-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b64dd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b64dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b64dd-107">ПР_ЕМС_АБ_ХАБ_РУТ_ДЕПАРТМЕНТ, ПР_ЕМС_АБ_ХАБ_РУТ_ДЕПАРТМЕНТ_А</span><span class="sxs-lookup"><span data-stu-id="b64dd-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="b64dd-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="b64dd-108">Property set:</span></span>  <br/> |<span data-ttu-id="b64dd-109">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="b64dd-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="b64dd-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="b64dd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b64dd-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="b64dd-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="b64dd-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b64dd-112">Data type:</span></span>  <br/> |<span data-ttu-id="b64dd-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b64dd-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="b64dd-114">Область:</span><span class="sxs-lookup"><span data-stu-id="b64dd-114">Area:</span></span>  <br/> |<span data-ttu-id="b64dd-115">Адресная книга Exchange</span><span class="sxs-lookup"><span data-stu-id="b64dd-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b64dd-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="b64dd-116">Remarks</span></span>

<span data-ttu-id="b64dd-117">Это свойство в контейнере глобального списка адресов (GAL), представляющее различающееся имя иерархического корня адреса.</span><span class="sxs-lookup"><span data-stu-id="b64dd-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="b64dd-118">Это свойство присутствует только в автономной адресной книге и никогда в доменных службах Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="b64dd-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="b64dd-119">Вызывающие абоненты должны передавать МАПИ_КАЧЕ_ОНЛИ в вызове метода Props, чтобы избежать вызова удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="b64dd-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="b64dd-120">Если этот параметр отсутствует, вызывающим абонентам следует использовать ПР_ЕМС_АБ_ХАБ_РУТ_ДЕПАРТМЕНТ, имеющий тип ПТ_ОБЖЕКТ, чтобы найти корневой отдел.</span><span class="sxs-lookup"><span data-stu-id="b64dd-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="b64dd-121">После получения корневого отдела он может иметь тип объекта МАПИ_МАИЛУСЕР или МАПИ_ДИСТЛИСТ.</span><span class="sxs-lookup"><span data-stu-id="b64dd-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="b64dd-122">Если типом объекта является МАПИ_ДИСТЛИСТ, используется новая схема.</span><span class="sxs-lookup"><span data-stu-id="b64dd-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="b64dd-123">Если типом объекта является МАПИ_МАИЛУСЕР, используется Предыдущая схема.</span><span class="sxs-lookup"><span data-stu-id="b64dd-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="b64dd-124">Microsoft Office Outlook 2007 с пакетом обновления 2 поддерживает обе схемы.</span><span class="sxs-lookup"><span data-stu-id="b64dd-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="b64dd-125">Microsoft Outlook 2010 и Microsoft Outlook 2013 поддерживают новую схему.</span><span class="sxs-lookup"><span data-stu-id="b64dd-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="b64dd-126">В новой схеме все группы отделов также являются списками рассылки и относятся к типу МАПИ_ДИСТЛИСТ.</span><span class="sxs-lookup"><span data-stu-id="b64dd-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="b64dd-127">Члены групп отделов и отделов в группах отделов получаются с помощью ПР_ЕМС_АБ_МЕМБЕР, точно так же, как члены списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="b64dd-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="b64dd-128">После получения корневого отдела он может иметь тип объекта МАПИ_МАИЛУСЕР или МАПИ_ДИСТЛИСТ.</span><span class="sxs-lookup"><span data-stu-id="b64dd-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="b64dd-129">Если типом объекта является МАПИ_ДИСТЛИСТ, используется новая схема.</span><span class="sxs-lookup"><span data-stu-id="b64dd-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="b64dd-130">Если типом объекта является МАПИ_МАИЛУСЕР, используется старая схема.</span><span class="sxs-lookup"><span data-stu-id="b64dd-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="b64dd-131">В новой схеме все группы отделов также являются разделами и относятся к типу МАПИ_ДИСТЛИСТ.</span><span class="sxs-lookup"><span data-stu-id="b64dd-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b64dd-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b64dd-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b64dd-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b64dd-133">Protocol specifications</span></span>

<span data-ttu-id="b64dd-134">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b64dd-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b64dd-135">Предоставляет определения свойств и ссылки на связанные спецификации протокола Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b64dd-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b64dd-136">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="b64dd-136">Header files</span></span>

<span data-ttu-id="b64dd-137">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b64dd-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="b64dd-138">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b64dd-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b64dd-139">См. также</span><span class="sxs-lookup"><span data-stu-id="b64dd-139">See also</span></span>



[<span data-ttu-id="b64dd-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b64dd-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b64dd-141">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b64dd-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b64dd-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b64dd-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b64dd-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b64dd-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

