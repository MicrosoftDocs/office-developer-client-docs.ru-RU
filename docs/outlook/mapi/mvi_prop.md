---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6a3d0d79d190b318d36fd9be8a3ec39d6aa7ad29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593979"
---
# <a name="mviprop"></a><span data-ttu-id="c04f3-103">MVI_PROP</span><span class="sxs-lookup"><span data-stu-id="c04f3-103">MVI_PROP</span></span>

  
  
<span data-ttu-id="c04f3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c04f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c04f3-105">Задает MVI_FLAG для указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="c04f3-105">Sets the MVI_FLAG for a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c04f3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c04f3-106">Header file:</span></span>  <br/> |<span data-ttu-id="c04f3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c04f3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c04f3-108">Связанные структуры:</span><span class="sxs-lookup"><span data-stu-id="c04f3-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="c04f3-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c04f3-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a><span data-ttu-id="c04f3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c04f3-110">Parameters</span></span>

 <span data-ttu-id="c04f3-111">_тег_</span><span class="sxs-lookup"><span data-stu-id="c04f3-111">_tag_</span></span>
  
> <span data-ttu-id="c04f3-112">Тег свойства, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="c04f3-112">The property tag to be modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c04f3-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="c04f3-113">Remarks</span></span>

<span data-ttu-id="c04f3-114">MVI_FLAG объединяет значения MV_FLAG, идентифицирующий свойства, поддерживающий несколько значений и MV_INSTANCE, запрашивающего отображаться несколько значений в таблице в нескольких строках.</span><span class="sxs-lookup"><span data-stu-id="c04f3-114">The MVI_FLAG combines the setting of MV_FLAG, identifying a property as multi-valued, and MV_INSTANCE, requesting that a multi-valued property be displayed in a table in multiple rows.</span></span> <span data-ttu-id="c04f3-115">Изменен тип свойства указанного свойства, но идентификатор не изменяется.</span><span class="sxs-lookup"><span data-stu-id="c04f3-115">The property type of the affected property is modified, but the identifier remains unchanged.</span></span> 
  
<span data-ttu-id="c04f3-116">Например при применении макрос MVI_PROP свойства типа PT_FLOAT, его тип изменяется на PT_MV_FLOAT.</span><span class="sxs-lookup"><span data-stu-id="c04f3-116">For example, when the MVI_PROP macro is applied to a property of type PT_FLOAT, its type is changed to PT_MV_FLOAT.</span></span> <span data-ttu-id="c04f3-117">Если функция входит в таблице несколько строк используются для представления, которая содержится одна строка для каждого значения свойства.</span><span class="sxs-lookup"><span data-stu-id="c04f3-117">When included in a table, multiple rows are used to represent the property that has one row for each value.</span></span> <span data-ttu-id="c04f3-118">Свойства для других столбцов повторяются.</span><span class="sxs-lookup"><span data-stu-id="c04f3-118">The properties for the other columns are repeated.</span></span> 
  
<span data-ttu-id="c04f3-119">Дополнительные сведения об этих флагов можно [Обзор типа свойств MAPI](mapi-property-type-overview.md) и [Работа с несколькими значениями столбцов](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="c04f3-119">For more information about these flags, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c04f3-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c04f3-120">See also</span></span>



[<span data-ttu-id="c04f3-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c04f3-121">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c04f3-122">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="c04f3-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

