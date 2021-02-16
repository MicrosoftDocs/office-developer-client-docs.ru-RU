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
# <a name="smapiformprop"></a><span data-ttu-id="687f7-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="687f7-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="687f7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="687f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="687f7-105">Описывает именуемую свойство, используемую с формой.</span><span class="sxs-lookup"><span data-stu-id="687f7-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="687f7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="687f7-106">Header file:</span></span>  <br/> |<span data-ttu-id="687f7-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="687f7-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="687f7-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="687f7-108">Members</span></span>

 <span data-ttu-id="687f7-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="687f7-109">**ulFlags**</span></span>
  
> <span data-ttu-id="687f7-110">Флаги, используемые для различия формата строк в **структуре SMAPIFormProp.**</span><span class="sxs-lookup"><span data-stu-id="687f7-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="687f7-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="687f7-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="687f7-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="687f7-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="687f7-113">Возвращенные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="687f7-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="687f7-114">Если MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="687f7-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="687f7-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="687f7-115">**nPropType**</span></span>
  
> <span data-ttu-id="687f7-116">Тип именоваемого свойства, для которого для наиболее важного слова установлено значение "ноль".</span><span class="sxs-lookup"><span data-stu-id="687f7-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="687f7-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="687f7-117">**nmid**</span></span>
  
> <span data-ttu-id="687f7-118">Имя имененного свойства, которое включает в себя структуру **GUID,** определяя набор свойств, и числовые или строковые значения, которые представляют идентификатор интерфейса и имя формы.</span><span class="sxs-lookup"><span data-stu-id="687f7-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="687f7-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="687f7-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="687f7-120">Указатель на отображаемого имени именоваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="687f7-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="687f7-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="687f7-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="687f7-122">Значение, описывающие тип данных, включенных в **член u.**</span><span class="sxs-lookup"><span data-stu-id="687f7-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="687f7-123">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="687f7-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="687f7-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="687f7-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="687f7-125">Член **u** не содержит enumeration.</span><span class="sxs-lookup"><span data-stu-id="687f7-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="687f7-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="687f7-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="687f7-127">Член **u** содержит структуру, описываемую в описании.</span><span class="sxs-lookup"><span data-stu-id="687f7-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="687f7-128">**u**</span><span class="sxs-lookup"><span data-stu-id="687f7-128">**u**</span></span>
  
> <span data-ttu-id="687f7-129">Объединение, описывающие связь между именем и номером именоваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="687f7-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="687f7-130">При использовании некоторых свойств член **u** пуст.</span><span class="sxs-lookup"><span data-stu-id="687f7-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="687f7-131">С другими свойствами он представлен в структуре, состоящей из следующих членов:</span><span class="sxs-lookup"><span data-stu-id="687f7-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="687f7-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="687f7-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="687f7-133">Структура [MAPINAMEID,](mapinameid.md) которая содержит набор свойств и идентификатор для именоваемой свойства.</span><span class="sxs-lookup"><span data-stu-id="687f7-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="687f7-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="687f7-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="687f7-135">Количество структур [SMAPIFormPropEnumVal в](smapiformpropenumval.md) массиве, на который указывает **член pfpevAvailable.**</span><span class="sxs-lookup"><span data-stu-id="687f7-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="687f7-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="687f7-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="687f7-137">Указатель на массив структур **SMAPIFormPropEnumVal,** каждая из которых содержит значение для именоваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="687f7-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="687f7-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="687f7-138">Remarks</span></span>

<span data-ttu-id="687f7-139">Структура **SMAPIFormProp** содержит сведения о свойстве формы, используемом как часть определений интерфейса [IMAPIFormInfo;](imapiforminfoimapiprop.md) **nSpecialType** содержит тег, который применяется к объединение **u,** которое является частью **SMAPIFormProp**.</span><span class="sxs-lookup"><span data-stu-id="687f7-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="687f7-140">См. также</span><span class="sxs-lookup"><span data-stu-id="687f7-140">See also</span></span>



[<span data-ttu-id="687f7-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="687f7-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="687f7-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="687f7-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="687f7-143">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="687f7-143">MAPI Structures</span></span>](mapi-structures.md)

