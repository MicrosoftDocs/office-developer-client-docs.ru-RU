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
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410681"
---
# <a name="mvi_prop"></a><span data-ttu-id="e620f-103">MVI_PROP</span><span class="sxs-lookup"><span data-stu-id="e620f-103">MVI_PROP</span></span>

  
  
<span data-ttu-id="e620f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e620f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e620f-105">Задает MVI_FLAG для указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="e620f-105">Sets the MVI_FLAG for a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e620f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e620f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e620f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e620f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e620f-108">Связанная структура:</span><span class="sxs-lookup"><span data-stu-id="e620f-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="e620f-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e620f-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a><span data-ttu-id="e620f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e620f-110">Parameters</span></span>

 <span data-ttu-id="e620f-111">_tag_</span><span class="sxs-lookup"><span data-stu-id="e620f-111">_tag_</span></span>
  
> <span data-ttu-id="e620f-112">Тег свойства, который необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="e620f-112">The property tag to be modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e620f-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="e620f-113">Remarks</span></span>

<span data-ttu-id="e620f-114">В MVI_FLAG параметр MV_FLAG, идентифицируя свойство как много значение, и MV_INSTANCE, запрашивая, чтобы много значение свойства отображалось в таблице в нескольких строках.</span><span class="sxs-lookup"><span data-stu-id="e620f-114">The MVI_FLAG combines the setting of MV_FLAG, identifying a property as multi-valued, and MV_INSTANCE, requesting that a multi-valued property be displayed in a table in multiple rows.</span></span> <span data-ttu-id="e620f-115">Тип свойства затронутого свойства изменяется, но идентификатор остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="e620f-115">The property type of the affected property is modified, but the identifier remains unchanged.</span></span> 
  
<span data-ttu-id="e620f-116">Например, если макрос MVI_PROP к свойству типа PT_FLOAT, его тип меняется на PT_MV_FLOAT.</span><span class="sxs-lookup"><span data-stu-id="e620f-116">For example, when the MVI_PROP macro is applied to a property of type PT_FLOAT, its type is changed to PT_MV_FLOAT.</span></span> <span data-ttu-id="e620f-117">При добавлении в таблицу несколько строк используются для представления свойства, которое содержит по одной строке для каждого значения.</span><span class="sxs-lookup"><span data-stu-id="e620f-117">When included in a table, multiple rows are used to represent the property that has one row for each value.</span></span> <span data-ttu-id="e620f-118">Свойства для других столбцов повторяются.</span><span class="sxs-lookup"><span data-stu-id="e620f-118">The properties for the other columns are repeated.</span></span> 
  
<span data-ttu-id="e620f-119">Дополнительные сведения об этих флагах см. в статье [MapI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns.](working-with-multivalued-columns.md)</span><span class="sxs-lookup"><span data-stu-id="e620f-119">For more information about these flags, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e620f-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e620f-120">See also</span></span>



[<span data-ttu-id="e620f-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e620f-121">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e620f-122">Макросы, связанные со структурами</span><span class="sxs-lookup"><span data-stu-id="e620f-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

