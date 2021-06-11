---
title: Синтаксис потока TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423029"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="f81c1-103">Синтаксис потока TNEF</span><span class="sxs-lookup"><span data-stu-id="f81c1-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="f81c1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f81c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f81c1-105">В этом разделе Bakus-Nauer описание синтаксиса потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="f81c1-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="f81c1-106">В этом описании нетерминалические элементы, которые имеют дальнейшее определение, находятся в italics.</span><span class="sxs-lookup"><span data-stu-id="f81c1-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="f81c1-107">Константы и буквальные элементы имеют жирный шрифт.</span><span class="sxs-lookup"><span data-stu-id="f81c1-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="f81c1-108">Последовательности элементов перечислены в порядке в одной строке.</span><span class="sxs-lookup"><span data-stu-id="f81c1-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="f81c1-109">Например, элемент  _Stream_ состоит из постоянной **TNEF_SIGNATURE,** а затем  _ключа_, а затем  _объекта_.</span><span class="sxs-lookup"><span data-stu-id="f81c1-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="f81c1-110">Если элемент имеет несколько возможных реализаций, альтернативы перечислены в последовательной строке.</span><span class="sxs-lookup"><span data-stu-id="f81c1-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="f81c1-111">Например, _объект_ может состоять из Message_Seq ,  Message_Seq с последующим Attach_Seq или просто _Attach_Seq_. </span><span class="sxs-lookup"><span data-stu-id="f81c1-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="f81c1-112">_TNEF_Stream:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="f81c1-113">**TNEF_SIGNATURE** _Key_ _Object_</span><span class="sxs-lookup"><span data-stu-id="f81c1-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="f81c1-114">_Клавиша:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-114">_Key:_</span></span>
  
> <span data-ttu-id="f81c1-115">16-битный неподписаный 16-битный неподписаный ряд</span><span class="sxs-lookup"><span data-stu-id="f81c1-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="f81c1-116">Транспорты с поддержкой TNEF создают это значение перед использованием реализации TNEF для создания потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="f81c1-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="f81c1-117">_Объект:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-117">_Object:_</span></span>
  
>  <span data-ttu-id="f81c1-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="f81c1-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="f81c1-119">_Message_Seq:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="f81c1-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="f81c1-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="f81c1-121">_attTnefVersion:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="f81c1-122">**LVL_MESSAGE attTnefVersion sizeof (ULONG)** **0x00010000** checksum</span><span class="sxs-lookup"><span data-stu-id="f81c1-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="f81c1-123">_attMessageClass:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="f81c1-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span><span class="sxs-lookup"><span data-stu-id="f81c1-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="f81c1-125">_Msg_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="f81c1-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="f81c1-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="f81c1-127">_Msg_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="f81c1-128">**LVL_MESSAGE** атрибут-ID атрибут-длина атрибута-данные checksum</span><span class="sxs-lookup"><span data-stu-id="f81c1-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="f81c1-129">Attribute-ID — это один из идентификаторов атрибутов TNEF, например **attSubject.**</span><span class="sxs-lookup"><span data-stu-id="f81c1-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="f81c1-130">Длина атрибута — это длина в bytes данных атрибута.</span><span class="sxs-lookup"><span data-stu-id="f81c1-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="f81c1-131">Атрибут-данные — это данные, связанные с атрибутом.</span><span class="sxs-lookup"><span data-stu-id="f81c1-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="f81c1-132">_Attach_Seq:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="f81c1-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="f81c1-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="f81c1-134">_attRenddata:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="f81c1-135">**LVL_ATTACHMENT attRenddata** **sizeof (RENDDATA) renddata** checksum</span><span class="sxs-lookup"><span data-stu-id="f81c1-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="f81c1-136">Renddata — это данные, связанные со структурой **RENDDATA,** которая содержит сведения о отрисовки соответствующего вложения.</span><span class="sxs-lookup"><span data-stu-id="f81c1-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="f81c1-137">Структура **RENDDATA** определяется в TNEF. Файл заглавной папки H.</span><span class="sxs-lookup"><span data-stu-id="f81c1-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="f81c1-138">_Att_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="f81c1-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="f81c1-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="f81c1-140">_Att_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="f81c1-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="f81c1-141">**LVL_ATTACHMENT** атрибута-ID атрибут-длина атрибут-данные checksum</span><span class="sxs-lookup"><span data-stu-id="f81c1-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="f81c1-142">Атрибут-ID, длина атрибута и данные атрибута имеют те же значения, что и для элемента Msg_Attribute.</span><span class="sxs-lookup"><span data-stu-id="f81c1-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

