---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 90829f8fff530d22a7dee68dc227655064147cee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575331"
---
# <a name="stnefproblem"></a><span data-ttu-id="5ecde-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="5ecde-103">STnefProblem</span></span>

  
  
<span data-ttu-id="5ecde-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ecde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ecde-105">Содержит сведения о проблеме обработки свойства или атрибута, которые произошли при выполнении кодирования и декодирования потока транспорта Neutral Encapsulation формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="5ecde-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ecde-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5ecde-106">Header file:</span></span>  <br/> |<span data-ttu-id="5ecde-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="5ecde-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="5ecde-108">Members</span><span class="sxs-lookup"><span data-stu-id="5ecde-108">Members</span></span>

 <span data-ttu-id="5ecde-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="5ecde-109">**ulComponent**</span></span>
  
> <span data-ttu-id="5ecde-110">Тип обработки, при котором возникла проблема.</span><span class="sxs-lookup"><span data-stu-id="5ecde-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="5ecde-111">Если произошла ошибка во время обработки сообщений, член **ulComponent** имеет значение нуль.</span><span class="sxs-lookup"><span data-stu-id="5ecde-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="5ecde-112">Если произошла ошибка во время обработки вложений, **ulComponent** имеет значение равно значению **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) соответствующих вложений.</span><span class="sxs-lookup"><span data-stu-id="5ecde-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="5ecde-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="5ecde-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="5ecde-114">Атрибут, связанный со свойством указал участником **ulPropTag** или при возникновении проблемы обработки TNEF при декодирование инкапсуляция заблокировать, одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5ecde-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="5ecde-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="5ecde-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="5ecde-116">Уровень сообщения</span><span class="sxs-lookup"><span data-stu-id="5ecde-116">Message level</span></span>
    
 <span data-ttu-id="5ecde-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="5ecde-117">_attAttachment_</span></span>
  
> <span data-ttu-id="5ecde-118">Уровень вложения</span><span class="sxs-lookup"><span data-stu-id="5ecde-118">Attachment level</span></span>
    
 <span data-ttu-id="5ecde-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="5ecde-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="5ecde-120">Свойство tag свойства, она вызвана TNEF обработки, за исключением проблема возникает при декодирования блок инкапсуляция, в котором case **ulPropTag** присваивается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5ecde-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="5ecde-121">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="5ecde-121">**scode**</span></span>
  
> <span data-ttu-id="5ecde-122">Ошибка значение, указывающее, проблема, возникшая при обработке.</span><span class="sxs-lookup"><span data-stu-id="5ecde-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ecde-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="5ecde-123">Remarks</span></span>

<span data-ttu-id="5ecde-124">Если структуру **STnefProblem** не создан во время обработки атрибут или свойство, оно может продолжать в разделе предполагается, что обработка атрибут или свойство успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="5ecde-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="5ecde-125">Единственное исключение происходит, когда проблемы заданных во время декодирование инкапсуляция блока.</span><span class="sxs-lookup"><span data-stu-id="5ecde-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="5ecde-126">В этом случае декодирования компонента, соответствующего блока остановлена и декодирования располагается в другой компонент.</span><span class="sxs-lookup"><span data-stu-id="5ecde-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ecde-127">См. также</span><span class="sxs-lookup"><span data-stu-id="5ecde-127">See also</span></span>



[<span data-ttu-id="5ecde-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="5ecde-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="5ecde-129">Каноническое свойство PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="5ecde-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="5ecde-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5ecde-130">MAPI Structures</span></span>](mapi-structures.md)

