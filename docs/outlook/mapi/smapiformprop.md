---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416701"
---
# <a name="smapiformprop"></a><span data-ttu-id="9a374-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="9a374-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="9a374-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a374-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a374-105">Описывает имя свойства, используемой с помощью формы.</span><span class="sxs-lookup"><span data-stu-id="9a374-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a374-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9a374-106">Header file:</span></span>  <br/> |<span data-ttu-id="9a374-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="9a374-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a><span data-ttu-id="9a374-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="9a374-108">Members</span></span>

 <span data-ttu-id="9a374-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9a374-109">**ulFlags**</span></span>
  
> <span data-ttu-id="9a374-110">Флаги, используемые для различия формата строк в **структуре SMAPIFormProp.**</span><span class="sxs-lookup"><span data-stu-id="9a374-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="9a374-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9a374-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="9a374-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9a374-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9a374-113">Возвращенные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a374-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="9a374-114">Если MAPI_UNICODE не установлено, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="9a374-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9a374-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="9a374-115">**nPropType**</span></span>
  
> <span data-ttu-id="9a374-116">Тип имени свойства, с самым значительным значением слова до нуля.</span><span class="sxs-lookup"><span data-stu-id="9a374-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="9a374-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="9a374-117">**nmid**</span></span>
  
> <span data-ttu-id="9a374-118">Имя имени свойства, которое включает в себя структуру **GUID,** определяя набор свойств, а также числовые или строковые значения, которые представляют идентификатор интерфейса и имя формы.</span><span class="sxs-lookup"><span data-stu-id="9a374-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="9a374-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="9a374-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="9a374-120">Указатель на отображаемого имени имени свойства.</span><span class="sxs-lookup"><span data-stu-id="9a374-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="9a374-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="9a374-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="9a374-122">Значение, описывающие тип данных,  включенных в u-member.</span><span class="sxs-lookup"><span data-stu-id="9a374-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="9a374-123">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="9a374-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="9a374-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="9a374-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="9a374-125">Член **u** не содержит переумерия.</span><span class="sxs-lookup"><span data-stu-id="9a374-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="9a374-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="9a374-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="9a374-127">Член **u** содержит структуру, описываемую переумерия.</span><span class="sxs-lookup"><span data-stu-id="9a374-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="9a374-128">**u**</span><span class="sxs-lookup"><span data-stu-id="9a374-128">**u**</span></span>
  
> <span data-ttu-id="9a374-129">Союз, описывающий связь между именем и номером имени свойства.</span><span class="sxs-lookup"><span data-stu-id="9a374-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="9a374-130">Используя некоторые свойства, **u-член** пуст.</span><span class="sxs-lookup"><span data-stu-id="9a374-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="9a374-131">С другими свойствами он представлен в структуре, состоящей из следующих участников:</span><span class="sxs-lookup"><span data-stu-id="9a374-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="9a374-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="9a374-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="9a374-133">Структура [MAPINAMEID,](mapinameid.md) которая содержит набор свойств и идентификатор для имени свойства.</span><span class="sxs-lookup"><span data-stu-id="9a374-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="9a374-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="9a374-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="9a374-135">Количество структур [SMAPIFormPropEnumVal](smapiformpropenumval.md) в массиве, на который указывает **член pfpevAvailable.**</span><span class="sxs-lookup"><span data-stu-id="9a374-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="9a374-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="9a374-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="9a374-137">Указатель на массив структур **SMAPIFormPropEnumVal,** каждая из которых содержит значение для имени свойства.</span><span class="sxs-lookup"><span data-stu-id="9a374-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9a374-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a374-138">Remarks</span></span>

<span data-ttu-id="9a374-139">Структура **SMAPIFormProp** содержит сведения о свойстве формы, используемом в рамках определений интерфейса [IMAPIFormInfo;](imapiforminfoimapiprop.md) **nSpecialType** содержит тег, применимый к **союзу u,** который является частью **SMAPIFormProp**.</span><span class="sxs-lookup"><span data-stu-id="9a374-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a374-140">См. также</span><span class="sxs-lookup"><span data-stu-id="9a374-140">See also</span></span>



[<span data-ttu-id="9a374-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="9a374-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="9a374-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="9a374-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="9a374-143">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="9a374-143">MAPI Structures</span></span>](mapi-structures.md)

