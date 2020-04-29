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
# <a name="smapiformprop"></a><span data-ttu-id="988e2-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="988e2-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="988e2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="988e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="988e2-105">Описывает именованное свойство, используемое с формой.</span><span class="sxs-lookup"><span data-stu-id="988e2-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="988e2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="988e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="988e2-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="988e2-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="988e2-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="988e2-108">Members</span></span>

 <span data-ttu-id="988e2-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="988e2-109">**ulFlags**</span></span>
  
> <span data-ttu-id="988e2-110">Флаги, используемые для различения формата строк в структуре **смапиформпроп** .</span><span class="sxs-lookup"><span data-stu-id="988e2-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="988e2-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="988e2-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="988e2-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="988e2-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="988e2-113">Возвращаемые строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="988e2-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="988e2-114">Если MAPI_UNICODE не заданы, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="988e2-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="988e2-115">**нпроптипе**</span><span class="sxs-lookup"><span data-stu-id="988e2-115">**nPropType**</span></span>
  
> <span data-ttu-id="988e2-116">Тип именованного свойства с наиболее значительным набором слов, равным нулю.</span><span class="sxs-lookup"><span data-stu-id="988e2-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="988e2-117">**нмид**</span><span class="sxs-lookup"><span data-stu-id="988e2-117">**nmid**</span></span>
  
> <span data-ttu-id="988e2-118">Имя для именованного свойства, которое включает структуру **GUID** , определяющую набор свойств, а также числовое или строковое значение, представляющее идентификатор интерфейса и имя формы.</span><span class="sxs-lookup"><span data-stu-id="988e2-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="988e2-119">**псздисплайнаме**</span><span class="sxs-lookup"><span data-stu-id="988e2-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="988e2-120">Указатель на отображаемое имя именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="988e2-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="988e2-121">**нспеЦиалтипе**</span><span class="sxs-lookup"><span data-stu-id="988e2-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="988e2-122">Значение, описывающее тип данных, включенных в элемент **u** .</span><span class="sxs-lookup"><span data-stu-id="988e2-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="988e2-123">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="988e2-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="988e2-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="988e2-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="988e2-125">Член **u** не содержит перечисление.</span><span class="sxs-lookup"><span data-stu-id="988e2-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="988e2-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="988e2-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="988e2-127">Член **u** содержит структуру, описывающую перечисление.</span><span class="sxs-lookup"><span data-stu-id="988e2-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="988e2-128">**u**</span><span class="sxs-lookup"><span data-stu-id="988e2-128">**u**</span></span>
  
> <span data-ttu-id="988e2-129">Объединение, описывающее связь между именем и номером именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="988e2-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="988e2-130">При использовании некоторых свойств член **u** пуст.</span><span class="sxs-lookup"><span data-stu-id="988e2-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="988e2-131">С другими свойствами она представлена в структуре, состоящей из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="988e2-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="988e2-132">**нмидидкс**</span><span class="sxs-lookup"><span data-stu-id="988e2-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="988e2-133">Структура [мапинамеид](mapinameid.md) , содержащая набор свойств и идентификатор для именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="988e2-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="988e2-134">**кфпеваваилабле**</span><span class="sxs-lookup"><span data-stu-id="988e2-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="988e2-135">Количество структур [смапиформпропенумвал](smapiformpropenumval.md) в массиве, на которое указывает элемент **пфпеваваилабле** .</span><span class="sxs-lookup"><span data-stu-id="988e2-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="988e2-136">**пфпеваваилабле**</span><span class="sxs-lookup"><span data-stu-id="988e2-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="988e2-137">Указатель на массив структур **смапиформпропенумвал** , каждый из которых содержит значение именованного свойства.</span><span class="sxs-lookup"><span data-stu-id="988e2-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="988e2-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="988e2-138">Remarks</span></span>

<span data-ttu-id="988e2-139">Структура **смапиформпроп** содержит сведения о свойстве формы, используемом в составе определений интерфейса [имапиформинфо](imapiforminfoimapiprop.md) ; **нспеЦиалтипе** содержит тег, который применяется к объединению **u** , которое входит в состав **смапиформпроп**.</span><span class="sxs-lookup"><span data-stu-id="988e2-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="988e2-140">См. также</span><span class="sxs-lookup"><span data-stu-id="988e2-140">See also</span></span>



[<span data-ttu-id="988e2-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="988e2-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="988e2-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="988e2-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="988e2-143">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="988e2-143">MAPI Structures</span></span>](mapi-structures.md)

