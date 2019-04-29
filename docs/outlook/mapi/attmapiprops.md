---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 185bfbb151c4f8d4e36b40b94393d14d50c33edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410457"
---
# <a name="attmapiprops"></a><span data-ttu-id="3d03e-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="3d03e-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="3d03e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d03e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d03e-105">Атрибут **аттмапипропс** является особым, поэтому его можно использовать для кодирования любого свойства MAPI, у которого нет аналога в наборе существующих атрибутов TNEF.</span><span class="sxs-lookup"><span data-stu-id="3d03e-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="3d03e-106">Данные атрибута — это подсчитанный набор свойств MAPI, который располагается от конца к концу.</span><span class="sxs-lookup"><span data-stu-id="3d03e-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="3d03e-107">Формат этой кодировки, который позволяет использовать любой набор свойств MAPI, выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3d03e-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="3d03e-108">_Проперти_сек:_</span><span class="sxs-lookup"><span data-stu-id="3d03e-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="3d03e-109">Свойство — число _проперти_валуе,..._</span><span class="sxs-lookup"><span data-stu-id="3d03e-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="3d03e-110">Количество элементов _проперти_валуе_ должно быть таким же, как значение счетчика свойства.</span><span class="sxs-lookup"><span data-stu-id="3d03e-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="3d03e-111">_Проперти_валуе:_</span><span class="sxs-lookup"><span data-stu-id="3d03e-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="3d03e-112">Свойство – Tag _Проперти_проперти — _свойство проптаг_наме_</span><span class="sxs-lookup"><span data-stu-id="3d03e-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="3d03e-113">Свойство-Tag — это просто значение, связанное с идентификатором свойства, например 0x0037001F для **пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3d03e-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="3d03e-114">_Свойств_</span><span class="sxs-lookup"><span data-stu-id="3d03e-114">_Property:_</span></span>
  
>  <span data-ttu-id="3d03e-115">__ Value Value — значение счетчика _,..._</span><span class="sxs-lookup"><span data-stu-id="3d03e-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="3d03e-116">_Значение:_</span><span class="sxs-lookup"><span data-stu-id="3d03e-116">_Value:_</span></span>
  
> <span data-ttu-id="3d03e-117">Value: Data Value — значение size — заполнение данных — значение размера — значение IID — заполнение данных</span><span class="sxs-lookup"><span data-stu-id="3d03e-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="3d03e-118">_Проптаг_наме:_</span><span class="sxs-lookup"><span data-stu-id="3d03e-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="3d03e-119">Name — имя GUID: имя имя — идентификатор имя — GUID имя — имя типа — строка с именем строки имени строки</span><span class="sxs-lookup"><span data-stu-id="3d03e-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="3d03e-120">Инкапсуляция каждого свойства зависит от идентификатора свойства и типа свойства.</span><span class="sxs-lookup"><span data-stu-id="3d03e-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="3d03e-121">Теги свойств, идентификаторы и типы определены в файлах заголовков Мапитагс. h и MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="3d03e-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="3d03e-122">Если свойство является именованным, то тег свойства сразу же сопровождается именем свойства MAPI, состоящим из глобального уникального идентификатора (GUID), типа, а также идентификатора или строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="3d03e-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="3d03e-123">Многозначные свойства и свойства со значениями переменной длины, такими как типы свойств ПТ_БИНАРИ, PT_STRING8, ПТ_УНИКОДЕ или ПТ_ОБЖЕКТ, рассматриваются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="3d03e-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="3d03e-124">Первое число значений, закодированных как 32-разрядное длинное длинное, помещается в поток TNEF, за которым следуют отдельные значения.</span><span class="sxs-lookup"><span data-stu-id="3d03e-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="3d03e-125">Каждое значение свойства — данные кодируются как размер в байтах, за которым следуют данные value.</span><span class="sxs-lookup"><span data-stu-id="3d03e-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="3d03e-126">Значение-Data заполняется до 4-байтовой границы, хотя размер заполнения не включается в значение.</span><span class="sxs-lookup"><span data-stu-id="3d03e-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="3d03e-127">Если свойство имеет тип ПТ_ОБЖЕКТ, за значением должно следовать идентификатор интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="3d03e-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="3d03e-128">Текущая реализация TNEF поддерживает только идентификаторы интерфейса Иид_имессаже, Иид_истораже и Иид_истреам.</span><span class="sxs-lookup"><span data-stu-id="3d03e-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="3d03e-129">Размер идентификатора интерфейса включается в значение size.</span><span class="sxs-lookup"><span data-stu-id="3d03e-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="3d03e-130">Если объект является внедренным сообщением (то есть у него есть тип свойства ПТ_ОБЖЕКТ и идентификатор интерфейса Иид_имессаже), то данные значения кодируются как внедренный поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="3d03e-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="3d03e-131">Фактическая кодировка внедренного сообщения в реализации TNEF выполняется путем открытия второго объекта TNEF для исходного потока и обработки встроенного потока.</span><span class="sxs-lookup"><span data-stu-id="3d03e-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

