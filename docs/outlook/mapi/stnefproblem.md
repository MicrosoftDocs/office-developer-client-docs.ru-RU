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
# <a name="stnefproblem"></a><span data-ttu-id="82c44-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="82c44-103">STnefProblem</span></span>

  
  
<span data-ttu-id="82c44-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82c44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82c44-105">Содержит сведения о проблеме обработки свойства или атрибута, возникшей во время кодирования или декодирования потока формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="82c44-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82c44-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="82c44-106">Header file:</span></span>  <br/> |<span data-ttu-id="82c44-107">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="82c44-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="82c44-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="82c44-108">Members</span></span>

 <span data-ttu-id="82c44-109">**улкомпонент**</span><span class="sxs-lookup"><span data-stu-id="82c44-109">**ulComponent**</span></span>
  
> <span data-ttu-id="82c44-110">Тип обработки, в которой возникла проблема.</span><span class="sxs-lookup"><span data-stu-id="82c44-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="82c44-111">Если во время обработки сообщения возникла проблема, для члена **улкомпонент** устанавливается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="82c44-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="82c44-112">Если во время обработки вложений возникла проблема, **улкомпонент** задается равным значению соответствующего **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) соответствующего вложения.</span><span class="sxs-lookup"><span data-stu-id="82c44-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="82c44-113">**улаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="82c44-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="82c44-114">Атрибут, связанный со свойством, указанным элементом **улпроптаг** , или при возникновении ошибки обработки TNEF при декодировании блока инкапсуляции одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="82c44-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="82c44-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="82c44-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="82c44-116">Уровень сообщения</span><span class="sxs-lookup"><span data-stu-id="82c44-116">Message level</span></span>
    
 <span data-ttu-id="82c44-117">_аттаттачмент_</span><span class="sxs-lookup"><span data-stu-id="82c44-117">_attAttachment_</span></span>
  
> <span data-ttu-id="82c44-118">Уровень вложенности</span><span class="sxs-lookup"><span data-stu-id="82c44-118">Attachment level</span></span>
    
 <span data-ttu-id="82c44-119">**улпроптаг**</span><span class="sxs-lookup"><span data-stu-id="82c44-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="82c44-120">Свойство, которое вызвало проблему с обработкой TNEF, за исключением случаев, когда проблема возникает при декодировании блока инкапсуляции, в котором **улпроптаг** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="82c44-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="82c44-121">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="82c44-121">**scode**</span></span>
  
> <span data-ttu-id="82c44-122">Значение ошибки, указывающее на проблему, возникшую во время обработки.</span><span class="sxs-lookup"><span data-stu-id="82c44-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82c44-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="82c44-123">Remarks</span></span>

<span data-ttu-id="82c44-124">Если структура **стнефпроблем** не создается во время обработки атрибута или свойства, то приложение может продолжать работу в предположении, что обработка этого атрибута или свойства прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="82c44-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="82c44-125">Единственное исключение возникает, когда проблема возникших во время декодирования блока инкапсуляции.</span><span class="sxs-lookup"><span data-stu-id="82c44-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="82c44-126">В этом случае декодирование компонента, соответствующего блоку, останавливается и декодирование продолжается в другом компоненте.</span><span class="sxs-lookup"><span data-stu-id="82c44-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82c44-127">См. также</span><span class="sxs-lookup"><span data-stu-id="82c44-127">See also</span></span>



[<span data-ttu-id="82c44-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="82c44-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="82c44-129">Каноническое свойство PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="82c44-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="82c44-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="82c44-130">MAPI Structures</span></span>](mapi-structures.md)

