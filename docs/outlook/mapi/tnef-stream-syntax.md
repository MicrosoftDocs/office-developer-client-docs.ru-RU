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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339636"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="6ad44-103">Синтаксис потока TNEF</span><span class="sxs-lookup"><span data-stu-id="6ad44-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="6ad44-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ad44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ad44-105">В этом разделе представлено описание синтаксиса потока TNEF Бакус – Науер Like.</span><span class="sxs-lookup"><span data-stu-id="6ad44-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="6ad44-106">В этом описании Нетерминальные элементы с дополнительным определением заменяются курсивом.</span><span class="sxs-lookup"><span data-stu-id="6ad44-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="6ad44-107">Константы и элементы литералов выделяются полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="6ad44-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="6ad44-108">Последовательности элементов перечисляются в одной строке по порядку.</span><span class="sxs-lookup"><span data-stu-id="6ad44-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="6ad44-109">Например, элемент _Stream_ состоит из константы **тнеф_сигнатуре**, за которыми следует _ключ_, за которым следует _объект_.</span><span class="sxs-lookup"><span data-stu-id="6ad44-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="6ad44-110">Если элемент имеет несколько возможных реализаций, альтернативные варианты перечисляются в строке подряд.</span><span class="sxs-lookup"><span data-stu-id="6ad44-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="6ad44-111">Например, _объект_ может состоять из _мессаже_сек_, _Мессаже_сек_ , за которым следует _аттач_сек_, или просто _аттач_сек_.</span><span class="sxs-lookup"><span data-stu-id="6ad44-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="6ad44-112">_Тнеф_стреам:_</span><span class="sxs-lookup"><span data-stu-id="6ad44-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="6ad44-113">**Тнеф_сигнатуре** _Key (ключ_ ) _Object (объект_ )</span><span class="sxs-lookup"><span data-stu-id="6ad44-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="6ad44-114">_Разделе_</span><span class="sxs-lookup"><span data-stu-id="6ad44-114">_Key:_</span></span>
  
> <span data-ttu-id="6ad44-115">ненулевое 16 – разрядное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="6ad44-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="6ad44-116">Транспорты с включенной поддержкой TNEF. это значение создается перед использованием реализации TNEF для создания потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="6ad44-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="6ad44-117">_Объектам_</span><span class="sxs-lookup"><span data-stu-id="6ad44-117">_Object:_</span></span>
  
>  <span data-ttu-id="6ad44-118">_Мессаже_сек Мессаже_сек Аттач_сек Аттач_сек_</span><span class="sxs-lookup"><span data-stu-id="6ad44-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="6ad44-119">_Мессаже_сек:_</span><span class="sxs-lookup"><span data-stu-id="6ad44-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="6ad44-120">_Атттнефверсион Атттнефверсион Мсг_аттрибуте_сек Атттнефверсион Аттмессажекласс Атттнефверсион attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="6ad44-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="6ad44-121">_Атттнефверсион:_</span><span class="sxs-lookup"><span data-stu-id="6ad44-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="6ad44-122">**Лвл_мессаже атттнефверсион sizeof (ulong)** Контрольная сумма **0x00010000**</span><span class="sxs-lookup"><span data-stu-id="6ad44-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="6ad44-123">_Аттмессажекласс:_</span><span class="sxs-lookup"><span data-stu-id="6ad44-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="6ad44-124">**Лвл_мессаже аттмессажекласс** Контрольная сумма _мсг_класс мсг_класс_ленгс_</span><span class="sxs-lookup"><span data-stu-id="6ad44-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="6ad44-125">_Мсг_аттрибуте_сек:_</span><span class="sxs-lookup"><span data-stu-id="6ad44-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="6ad44-126">_Мсг_аттрибуте Мсг_аттрибуте Мсг_аттрибуте_сек_</span><span class="sxs-lookup"><span data-stu-id="6ad44-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="6ad44-127">_Мсг_аттрибуте:_</span><span class="sxs-lookup"><span data-stu-id="6ad44-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="6ad44-128">Атрибут **лвл_мессаже** Attribute – length Attribute — контрольная сумма данных</span><span class="sxs-lookup"><span data-stu-id="6ad44-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="6ad44-129">Attribute-ID — это один из идентификаторов атрибутов TNEF, например **аттсубжект**.</span><span class="sxs-lookup"><span data-stu-id="6ad44-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="6ad44-130">Attribute-length — это длина данных атрибута в байтах.</span><span class="sxs-lookup"><span data-stu-id="6ad44-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="6ad44-131">Attribute-Data — это данные, связанные с атрибутом.</span><span class="sxs-lookup"><span data-stu-id="6ad44-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="6ad44-132">_Аттач_сек:_</span><span class="sxs-lookup"><span data-stu-id="6ad44-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="6ad44-133">_Аттренддата Аттренддата Атт_аттрибуте_сек_</span><span class="sxs-lookup"><span data-stu-id="6ad44-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="6ad44-134">_Аттренддата:_</span><span class="sxs-lookup"><span data-stu-id="6ad44-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="6ad44-135">**Лвл_аттачмент аттренддата** Контрольная сумма для **sizeof (ренддата)** ренддата</span><span class="sxs-lookup"><span data-stu-id="6ad44-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="6ad44-136">Ренддата — это данные, связанные с структурой **ренддата** , которые содержат информацию отображения для соответствующего вложения.</span><span class="sxs-lookup"><span data-stu-id="6ad44-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="6ad44-137">Структура **ренддата** определена в формате TNEF. H файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="6ad44-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="6ad44-138">_Атт_аттрибуте_сек:_</span><span class="sxs-lookup"><span data-stu-id="6ad44-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="6ad44-139">_Атт_аттрибуте Атт_аттрибуте Атт_аттрибуте_сек_</span><span class="sxs-lookup"><span data-stu-id="6ad44-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="6ad44-140">_Атт_аттрибуте:_</span><span class="sxs-lookup"><span data-stu-id="6ad44-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="6ad44-141">Атрибут **лвл_аттачмент** Attribute – length Attribute — контрольная сумма данных</span><span class="sxs-lookup"><span data-stu-id="6ad44-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="6ad44-142">Атрибуты Attribute (ID), Attribute – length и Attribute – Data имеют те же значения, что и для элемента Мсг_аттрибуте.</span><span class="sxs-lookup"><span data-stu-id="6ad44-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

