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
ms.openlocfilehash: 4e8e2474d2adb882dd0ba43aeb0d8b05044a6ce6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592061"
---
# <a name="smapiformprop"></a><span data-ttu-id="a725d-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="a725d-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="a725d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a725d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a725d-105">Описание именованного свойства, используемые с формой.</span><span class="sxs-lookup"><span data-stu-id="a725d-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a725d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a725d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a725d-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="a725d-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="a725d-108">Members</span><span class="sxs-lookup"><span data-stu-id="a725d-108">Members</span></span>

 <span data-ttu-id="a725d-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a725d-109">**ulFlags**</span></span>
  
> <span data-ttu-id="a725d-110">Флаги, используемые для различения формат строк в структуре **SMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="a725d-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="a725d-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a725d-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="a725d-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a725d-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a725d-113">Строк, возвращаемых находятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="a725d-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="a725d-114">Если MAPI_UNICODE не задано, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a725d-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a725d-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="a725d-115">**nPropType**</span></span>
  
> <span data-ttu-id="a725d-116">Тип именованного свойства с наиболее важных word, равным нулю.</span><span class="sxs-lookup"><span data-stu-id="a725d-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="a725d-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="a725d-117">**nmid**</span></span>
  
> <span data-ttu-id="a725d-118">Имя для именованного свойства, который включает структуру **идентификатор GUID** , идентифицирующий значение свойства set и числовой или строка, которая представляет имя интерфейса идентификатор и формы.</span><span class="sxs-lookup"><span data-stu-id="a725d-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="a725d-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="a725d-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="a725d-120">Указатель на отображаемое имя именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="a725d-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="a725d-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="a725d-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="a725d-122">Значение, указывающее тип данных, включенных в член **u** .</span><span class="sxs-lookup"><span data-stu-id="a725d-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="a725d-123">Ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="a725d-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="a725d-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="a725d-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="a725d-125">Член **u** не содержит перечисление.</span><span class="sxs-lookup"><span data-stu-id="a725d-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="a725d-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="a725d-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="a725d-127">Член **u** содержит структуру, которая описывает перечисление.</span><span class="sxs-lookup"><span data-stu-id="a725d-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="a725d-128">**u**</span><span class="sxs-lookup"><span data-stu-id="a725d-128">**u**</span></span>
  
> <span data-ttu-id="a725d-129">Объединение, описывающие связь между имя и номер именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="a725d-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="a725d-130">С помощью некоторых свойств, **u** элемента будет пустым.</span><span class="sxs-lookup"><span data-stu-id="a725d-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="a725d-131">С другими свойствами представленным в структуре, состоящий из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="a725d-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="a725d-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="a725d-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="a725d-133">Структура [MAPINAMEID](mapinameid.md) , содержащая набор свойств и идентификатор для именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="a725d-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="a725d-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="a725d-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="a725d-135">Число структур [SMAPIFormPropEnumVal](smapiformpropenumval.md) в массиве, на который указывает член **pfpevAvailable** .</span><span class="sxs-lookup"><span data-stu-id="a725d-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="a725d-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="a725d-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="a725d-137">Указатель на массив структур **SMAPIFormPropEnumVal** , каждая из которых содержит значение именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="a725d-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a725d-138">Замечания</span><span class="sxs-lookup"><span data-stu-id="a725d-138">Remarks</span></span>

<span data-ttu-id="a725d-139">Структура **SMAPIFormProp** содержит информацию о свойствах формы, используется как часть определения интерфейс [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType** содержит тег, которое применяется для объединения **u** , который является частью **SMAPIFormProp**.</span><span class="sxs-lookup"><span data-stu-id="a725d-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a725d-140">См. также</span><span class="sxs-lookup"><span data-stu-id="a725d-140">See also</span></span>



[<span data-ttu-id="a725d-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="a725d-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="a725d-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="a725d-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="a725d-143">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a725d-143">MAPI Structures</span></span>](mapi-structures.md)

