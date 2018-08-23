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
ms.openlocfilehash: ce2b2497bd89f00ce7f063d3e482752fabfeb731
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594336"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="197c1-103">Синтаксис потока TNEF</span><span class="sxs-lookup"><span data-stu-id="197c1-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="197c1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="197c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="197c1-105">В этом разделе представлены Bakus Nauer как описание синтаксиса поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="197c1-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="197c1-106">В это описание нетерминальных элементов, которые имеют дополнительные определения, курсивом.</span><span class="sxs-lookup"><span data-stu-id="197c1-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="197c1-107">Константы и литерал элементов — полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="197c1-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="197c1-108">Последовательностей элементов перечислены в порядке на одну строку.</span><span class="sxs-lookup"><span data-stu-id="197c1-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="197c1-109">Например элемент _потока_ состоит из константу **TNEF_SIGNATURE**, а затем _ключ_, а затем с помощью _объекта_.</span><span class="sxs-lookup"><span data-stu-id="197c1-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="197c1-110">Если элемент содержит более одного из возможных вариантов реализации, варианты перечисляются в последовательных строк.</span><span class="sxs-lookup"><span data-stu-id="197c1-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="197c1-111">Например, _объект_ может состоять из _Message_Seq_, _Message_Seq_ , за которым следует _Attach_Seq_или просто _Attach_Seq_.</span><span class="sxs-lookup"><span data-stu-id="197c1-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="197c1-112">_TNEF_Stream:_</span><span class="sxs-lookup"><span data-stu-id="197c1-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="197c1-113">**TNEF_SIGNATURE** _Ключ_ _Объект_</span><span class="sxs-lookup"><span data-stu-id="197c1-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="197c1-114">_Ключ:_</span><span class="sxs-lookup"><span data-stu-id="197c1-114">_Key:_</span></span>
  
> <span data-ttu-id="197c1-115">ненулевое 16-разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="197c1-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="197c1-116">Включено TNEF транспортов создать это значение перед использованием реализации TNEF для создания потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="197c1-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="197c1-117">_Объект:_</span><span class="sxs-lookup"><span data-stu-id="197c1-117">_Object:_</span></span>
  
>  <span data-ttu-id="197c1-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="197c1-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="197c1-119">_Message_Seq:_</span><span class="sxs-lookup"><span data-stu-id="197c1-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="197c1-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="197c1-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="197c1-121">_attTnefVersion:_</span><span class="sxs-lookup"><span data-stu-id="197c1-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="197c1-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** контрольная сумма **0x00010000**</span><span class="sxs-lookup"><span data-stu-id="197c1-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="197c1-123">_attMessageClass:_</span><span class="sxs-lookup"><span data-stu-id="197c1-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="197c1-124">**LVL_MESSAGE attMessageClass** контрольная сумма _msg_class_length msg_class_</span><span class="sxs-lookup"><span data-stu-id="197c1-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="197c1-125">_Msg_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="197c1-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="197c1-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="197c1-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="197c1-127">_Msg_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="197c1-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="197c1-128">Контрольная сумма данных атрибутов **LVL_MESSAGE** идентификатор атрибута длина атрибутов</span><span class="sxs-lookup"><span data-stu-id="197c1-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="197c1-129">Идентификатор атрибута — это один из идентификаторы атрибута TNEF, такие как **attSubject**.</span><span class="sxs-lookup"><span data-stu-id="197c1-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="197c1-130">Длина атрибутов — это длина в байтах данных атрибута.</span><span class="sxs-lookup"><span data-stu-id="197c1-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="197c1-131">Атрибут data содержит данные, связанные с помощью атрибута.</span><span class="sxs-lookup"><span data-stu-id="197c1-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="197c1-132">_Attach_Seq:_</span><span class="sxs-lookup"><span data-stu-id="197c1-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="197c1-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="197c1-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="197c1-134">_attRenddata:_</span><span class="sxs-lookup"><span data-stu-id="197c1-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="197c1-135">**LVL_ATTACHMENT attRenddata** контрольная сумма renddata **sizeof(RENDDATA)**</span><span class="sxs-lookup"><span data-stu-id="197c1-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="197c1-136">Renddata — это данные, связанные со структурой **RENDDATA** , который содержит сведения о визуализации для соответствующих вложений.</span><span class="sxs-lookup"><span data-stu-id="197c1-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="197c1-137">Структура **RENDDATA** определен в формате TNEF. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="197c1-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="197c1-138">_Att_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="197c1-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="197c1-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="197c1-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="197c1-140">_Att_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="197c1-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="197c1-141">Контрольная сумма данных атрибутов **LVL_ATTACHMENT** идентификатор атрибута длина атрибутов</span><span class="sxs-lookup"><span data-stu-id="197c1-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="197c1-142">Идентификатор атрибута, длина атрибутов и данных атрибутов имеют же значения, как для элемента Msg_Attribute.</span><span class="sxs-lookup"><span data-stu-id="197c1-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

