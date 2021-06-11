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
# <a name="attmapiprops"></a><span data-ttu-id="1cee2-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="1cee2-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="1cee2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cee2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cee2-105">Атрибут **attMAPIProps** является особенным в том, что его можно использовать для кодирования любого свойства MAPI, которое не имеет аналога в наборе существующих атрибутов, определенных TNEF.</span><span class="sxs-lookup"><span data-stu-id="1cee2-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="1cee2-106">Данные атрибута — это подсчитываемая набор свойств MAPI, заложенных в конце.</span><span class="sxs-lookup"><span data-stu-id="1cee2-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="1cee2-107">Формат этого кодинга, который позволяет использовать любой набор свойств MAPI, является следующим:</span><span class="sxs-lookup"><span data-stu-id="1cee2-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="1cee2-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="1cee2-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="1cee2-109">количество  _свойств Property_Value,..._</span><span class="sxs-lookup"><span data-stu-id="1cee2-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="1cee2-110">Должно быть столько  _Property_Value_ элементов, сколько указано в значении "количество свойств".</span><span class="sxs-lookup"><span data-stu-id="1cee2-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="1cee2-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="1cee2-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="1cee2-112">свойство тег _Property_property-тег  _Proptag_Name свойства_</span><span class="sxs-lookup"><span data-stu-id="1cee2-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="1cee2-113">Тег свойства — это просто значение, связанное с идентификатором свойства, например 0x0037001F для **PR_SUBJECT** [(PidTagSubject).](pidtagsubject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1cee2-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="1cee2-114">_Свойство:_</span><span class="sxs-lookup"><span data-stu-id="1cee2-114">_Property:_</span></span>
  
>  <span data-ttu-id="1cee2-115">_Значение_  _значение-значение,..._</span><span class="sxs-lookup"><span data-stu-id="1cee2-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="1cee2-116">_Значение:_</span><span class="sxs-lookup"><span data-stu-id="1cee2-116">_Value:_</span></span>
  
> <span data-ttu-id="1cee2-117">обивка значения-данные значения-данные для заполнения значения-размера value-IID-данных</span><span class="sxs-lookup"><span data-stu-id="1cee2-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="1cee2-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="1cee2-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="1cee2-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span><span class="sxs-lookup"><span data-stu-id="1cee2-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="1cee2-120">Инкапсуляция каждого свойства зависит от идентификатора свойства и типа свойства.</span><span class="sxs-lookup"><span data-stu-id="1cee2-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="1cee2-121">Теги свойств, идентификаторы и типы определяются в файлах заголовок Mapitags.h и Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="1cee2-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="1cee2-122">Если свойство является свойством с именем, за тегом свойства немедленно следует имя свойства MAPI, состоящее из глобально уникального идентификатора (GUID), типа и идентификатора или строки Юникод.</span><span class="sxs-lookup"><span data-stu-id="1cee2-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="1cee2-123">Многоценные свойства и свойства с переменными значениями длины, такими как PT_BINARY, PT_STRING8, PT_UNICODE или PT_OBJECT свойств, рассматриваются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="1cee2-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="1cee2-124">Сначала количество значений, закодированное как 32-битная неподписаная длинная, помещается в поток TNEF, а затем отдельные значения.</span><span class="sxs-lookup"><span data-stu-id="1cee2-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="1cee2-125">Данные о значении каждого свойства кодируются как его размер в битах, за которыми следуют сами значения-данные.</span><span class="sxs-lookup"><span data-stu-id="1cee2-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="1cee2-126">Значение-данные примыкает к границе 4 байта, хотя количество обивки не включено в размер значения.</span><span class="sxs-lookup"><span data-stu-id="1cee2-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="1cee2-127">Если свойство имеет тип PT_OBJECT, за ним следует идентификатор интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="1cee2-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="1cee2-128">Текущая реализация TNEF поддерживает только идентификаторы IID_IMessage, IID_IStorage и IID_Istream интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1cee2-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="1cee2-129">Размер идентификатора интерфейса включен в размер значения.</span><span class="sxs-lookup"><span data-stu-id="1cee2-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="1cee2-130">Если объект является встроенным сообщением (то есть имеет тип свойства PT_OBJECT и идентификатор интерфейса IID_Imessage), данные значения закодируются как встроенный поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="1cee2-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="1cee2-131">Фактическое кодивка встроенного сообщения в реализации TNEF делается путем открытия второго объекта TNEF для исходного потока и обработки встроенного потока.</span><span class="sxs-lookup"><span data-stu-id="1cee2-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

