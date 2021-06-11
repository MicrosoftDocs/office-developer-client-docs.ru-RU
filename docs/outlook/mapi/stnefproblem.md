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
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435182"
---
# <a name="stnefproblem"></a><span data-ttu-id="22be5-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="22be5-103">STnefProblem</span></span>

  
  
<span data-ttu-id="22be5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22be5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22be5-105">Содержит сведения о проблеме обработки свойств или атрибутов, которая возникла во время кодирования или декодирования потока транспортной нейтральной инкапсуляции (TNEF).</span><span class="sxs-lookup"><span data-stu-id="22be5-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22be5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="22be5-106">Header file:</span></span>  <br/> |<span data-ttu-id="22be5-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="22be5-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="22be5-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="22be5-108">Members</span></span>

 <span data-ttu-id="22be5-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="22be5-109">**ulComponent**</span></span>
  
> <span data-ttu-id="22be5-110">Тип обработки, в ходе которой возникла проблема.</span><span class="sxs-lookup"><span data-stu-id="22be5-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="22be5-111">Если проблема возникла во время обработки сообщений, для **участника ulComponent** установлено значение нуля.</span><span class="sxs-lookup"><span data-stu-id="22be5-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="22be5-112">Если проблема возникла во время обработки вложений, **значение ulComponent** равно значению [PR_ATTACH_NUM (PidTagAttachNumber).](pidtagattachnumber-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="22be5-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="22be5-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="22be5-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="22be5-114">Атрибут, связанный с свойством, указанным участником **ulPropTag** или при проблеме обработки TNEF при декодировании блока инкапсуляции, одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="22be5-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="22be5-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="22be5-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="22be5-116">Уровень сообщений</span><span class="sxs-lookup"><span data-stu-id="22be5-116">Message level</span></span>
    
 <span data-ttu-id="22be5-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="22be5-117">_attAttachment_</span></span>
  
> <span data-ttu-id="22be5-118">Уровень вложения</span><span class="sxs-lookup"><span data-stu-id="22be5-118">Attachment level</span></span>
    
 <span data-ttu-id="22be5-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="22be5-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="22be5-120">Тег свойства свойства, вызвав которого возникла проблема обработки TNEF, за исключением случаев, когда возникает проблема при декодировании блока инкапсуляции, в этом случае **значение ulPropTag** задалось нулю.</span><span class="sxs-lookup"><span data-stu-id="22be5-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="22be5-121">**scode**</span><span class="sxs-lookup"><span data-stu-id="22be5-121">**scode**</span></span>
  
> <span data-ttu-id="22be5-122">Значение ошибки, указывающее на проблему, с которой возникла во время обработки.</span><span class="sxs-lookup"><span data-stu-id="22be5-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22be5-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="22be5-123">Remarks</span></span>

<span data-ttu-id="22be5-124">Если структура **STnefProblem** не создается во время обработки атрибута или свойства, приложение может продолжить работу при предположении, что обработка этого атрибута или свойства увенчалась успехом.</span><span class="sxs-lookup"><span data-stu-id="22be5-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="22be5-125">Единственное исключение возникает, когда возникла проблема при декодировании блока инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="22be5-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="22be5-126">В этом случае расшифровка компонента, соответствующего блоку, остановлена и декодирования продолжается в другом компоненте.</span><span class="sxs-lookup"><span data-stu-id="22be5-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22be5-127">См. также</span><span class="sxs-lookup"><span data-stu-id="22be5-127">See also</span></span>



[<span data-ttu-id="22be5-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="22be5-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="22be5-129">Каноническое свойство PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="22be5-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="22be5-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="22be5-130">MAPI Structures</span></span>](mapi-structures.md)

