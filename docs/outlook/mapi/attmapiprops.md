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
ms.openlocfilehash: 72f252791e374ed4b9b2a40c9b151ef2b91fefe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588057"
---
# <a name="attmapiprops"></a><span data-ttu-id="26827-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="26827-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="26827-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26827-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26827-105">Атрибут **attMAPIProps** особые, в том, что они могут использоваться для кодирования любого свойства MAPI, для которого не аналога в наборе существующие атрибуты TNEF.</span><span class="sxs-lookup"><span data-stu-id="26827-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="26827-106">Атрибут данных является инвентаризации набор свойств MAPI расположения начала до конца.</span><span class="sxs-lookup"><span data-stu-id="26827-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="26827-107">Формат данной кодировки, что позволяет для любого набора свойств MAPI, выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="26827-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="26827-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="26827-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="26827-109">свойство count _Property_Value..._</span><span class="sxs-lookup"><span data-stu-id="26827-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="26827-110">Должно быть любое количество элементов _Property_Value_ указывает значение свойства count.</span><span class="sxs-lookup"><span data-stu-id="26827-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="26827-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="26827-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="26827-112">Свойство tag _Property_property тега _Proptag_Name свойство_</span><span class="sxs-lookup"><span data-stu-id="26827-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="26827-113">Тег свойства — это просто значение, связанное с идентификатором свойства, такие как 0x0037001F для **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="26827-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="26827-114">_Свойство:_</span><span class="sxs-lookup"><span data-stu-id="26827-114">_Property:_</span></span>
  
>  <span data-ttu-id="26827-115">Количество значений _значение_ , _значение..._</span><span class="sxs-lookup"><span data-stu-id="26827-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="26827-116">_Значение:_</span><span class="sxs-lookup"><span data-stu-id="26827-116">_Value:_</span></span>
  
> <span data-ttu-id="26827-117">данные значения значение данных размер значения отступов внутренние поля данных значение ИД размер значения значение интерфейса</span><span class="sxs-lookup"><span data-stu-id="26827-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="26827-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="26827-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="26827-119">Имя guid вида имя идентификатора имени имя guid имя типа длина строки имя строки с названием внутренние поля</span><span class="sxs-lookup"><span data-stu-id="26827-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="26827-120">Инкапсуляция каждое свойство в зависимости от идентификатор свойства и типа свойства.</span><span class="sxs-lookup"><span data-stu-id="26827-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="26827-121">Свойство теги, идентификаторы и типы определяются в файлах заголовка Mapitags.h и Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="26827-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="26827-122">Если свойство имеет именованного свойства, а затем свойство tag немедленно следуют имя свойства MAPI, состоящий из глобальный уникальный идентификатор (GUID), тип и идентификатор или строка Юникода.</span><span class="sxs-lookup"><span data-stu-id="26827-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="26827-123">Многозначные свойства и свойства с помощью переменной длины значения, такие как типы свойств PT_BINARY, PT_STRING8, PT_UNICODE или PT_OBJECT обрабатывается следующим образом.</span><span class="sxs-lookup"><span data-stu-id="26827-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="26827-124">Сначала количество значений, помеченные как неподписанные длинные, 32-разрядного переводится в поток TNEF, а затем отдельных значений.</span><span class="sxs-lookup"><span data-stu-id="26827-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="26827-125">Данные значения каждого свойства закодирован его размер в байтах, следуют значение данных самого.</span><span class="sxs-lookup"><span data-stu-id="26827-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="26827-126">Значение параметра дополняется выходной параметр на границе 4-байтных, несмотря на то, что отступ не включено в размер значения.</span><span class="sxs-lookup"><span data-stu-id="26827-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="26827-127">Если свойство имеет тип PT_OBJECT, размер значения следует интерфейс идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="26827-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="26827-128">Текущая реализация TNEF поддерживает только идентификаторы интерфейса IID_IMessage, IID_IStorage и IID_Istream.</span><span class="sxs-lookup"><span data-stu-id="26827-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="26827-129">Размер идентификатор интерфейса включается в размер значения.</span><span class="sxs-lookup"><span data-stu-id="26827-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="26827-130">Если объект является внедренных сообщений (то есть, он имеет тип свойства PT_OBJECT и идентификатор интерфейса IID_Imessage), данные значения кодировке внедренных поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="26827-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="26827-131">Фактическая кодировка внедренных сообщений в реализации TNEF выполняется, открыв второй объект TNEF для исходного потока и обработки встроенного потока.</span><span class="sxs-lookup"><span data-stu-id="26827-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

