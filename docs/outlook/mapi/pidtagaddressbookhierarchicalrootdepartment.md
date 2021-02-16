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
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="40e0a-103">Каноническое свойство PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="40e0a-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="40e0a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40e0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="40e0a-105">Содержит различающейся имя иерархического корневого адреса (HAB).</span><span class="sxs-lookup"><span data-stu-id="40e0a-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40e0a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="40e0a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40e0a-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="40e0a-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="40e0a-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="40e0a-108">Property set:</span></span>  <br/> |<span data-ttu-id="40e0a-109">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="40e0a-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="40e0a-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="40e0a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="40e0a-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="40e0a-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="40e0a-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="40e0a-112">Data type:</span></span>  <br/> |<span data-ttu-id="40e0a-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="40e0a-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="40e0a-114">Область:</span><span class="sxs-lookup"><span data-stu-id="40e0a-114">Area:</span></span>  <br/> |<span data-ttu-id="40e0a-115">Адресная книга Exchange</span><span class="sxs-lookup"><span data-stu-id="40e0a-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40e0a-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="40e0a-116">Remarks</span></span>

<span data-ttu-id="40e0a-117">Это свойство в контейнере глобального списка адресов (GAL) и представляет различается имя корневого иерархического адреса.</span><span class="sxs-lookup"><span data-stu-id="40e0a-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="40e0a-118">Это свойство присутствует только в автономной адресной книге и никогда не находится в доменных службах Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="40e0a-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="40e0a-119">Во избежание удаленного вызова процедур MAPI_CACHE_ONLY вызову GetProps.</span><span class="sxs-lookup"><span data-stu-id="40e0a-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="40e0a-120">Если это не так, звоня PR_EMS_AB_HAB_ROOT_DEPARTMENT, тип PT_OBJECT, для поиска корневого отдела.</span><span class="sxs-lookup"><span data-stu-id="40e0a-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="40e0a-121">После того как корневой отдел будет получен, он может иметь тип MAPI_MAILUSER или MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="40e0a-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="40e0a-122">Если тип объекта MAPI_DISTLIST, используется новая схема.</span><span class="sxs-lookup"><span data-stu-id="40e0a-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="40e0a-123">Если тип объекта MAPI_MAILUSER, используется предыдущая схема.</span><span class="sxs-lookup"><span data-stu-id="40e0a-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="40e0a-124">Microsoft Office Outlook 2007 Пакет обновления 2 поддерживает обе схемы.</span><span class="sxs-lookup"><span data-stu-id="40e0a-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="40e0a-125">Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013 поддерживают новую схему.</span><span class="sxs-lookup"><span data-stu-id="40e0a-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="40e0a-126">В новой схеме все группы отделов также являются списками рассылки и имеют тип MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="40e0a-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="40e0a-127">Члены групп отделов и отделы в группах отделов получаются с помощью PR_EMS_AB_MEMBER точно так же, как участники списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="40e0a-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="40e0a-128">После того как корневой отдел будет получен, он может иметь тип MAPI_MAILUSER или MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="40e0a-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="40e0a-129">Если тип объекта MAPI_DISTLIST, используется новая схема.</span><span class="sxs-lookup"><span data-stu-id="40e0a-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="40e0a-130">Если тип объекта MAPI_MAILUSER, используется старая схема.</span><span class="sxs-lookup"><span data-stu-id="40e0a-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="40e0a-131">В новой схеме все группы отделов также являются DLS и имеют тип MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="40e0a-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="40e0a-132">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="40e0a-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="40e0a-133">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="40e0a-133">Protocol specifications</span></span>

<span data-ttu-id="40e0a-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="40e0a-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="40e0a-135">Предоставляет определения набора свойств и ссылки на связанные Microsoft Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="40e0a-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="40e0a-136">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="40e0a-136">Header files</span></span>

<span data-ttu-id="40e0a-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40e0a-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="40e0a-138">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="40e0a-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="40e0a-139">См. также</span><span class="sxs-lookup"><span data-stu-id="40e0a-139">See also</span></span>



[<span data-ttu-id="40e0a-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="40e0a-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="40e0a-141">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="40e0a-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="40e0a-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="40e0a-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="40e0a-143">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="40e0a-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

