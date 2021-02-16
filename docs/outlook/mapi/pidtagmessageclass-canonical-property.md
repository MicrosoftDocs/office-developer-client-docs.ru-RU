---
title: Каноническое свойство PidTagMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359266"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="69fd9-103">Каноническое свойство PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="69fd9-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="69fd9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69fd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69fd9-105">Содержит текстовую строку, идентифицирующую определяемый отправителем класс сообщений, например IPM.Note.</span><span class="sxs-lookup"><span data-stu-id="69fd9-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69fd9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="69fd9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69fd9-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="69fd9-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="69fd9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="69fd9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69fd9-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="69fd9-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="69fd9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="69fd9-110">Data type:</span></span>  <br/> |<span data-ttu-id="69fd9-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="69fd9-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="69fd9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="69fd9-112">Area:</span></span>  <br/> |<span data-ttu-id="69fd9-113">Распространенная</span><span class="sxs-lookup"><span data-stu-id="69fd9-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69fd9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="69fd9-114">Remarks</span></span>

<span data-ttu-id="69fd9-115">Класс сообщения указывает тип сообщения.</span><span class="sxs-lookup"><span data-stu-id="69fd9-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="69fd9-116">Он определяет набор свойств, определенных для сообщения, тип передаемой в сообщении информации и обработку сообщения.</span><span class="sxs-lookup"><span data-stu-id="69fd9-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="69fd9-117">Эти свойства содержат строки, совмещенные с точкими.</span><span class="sxs-lookup"><span data-stu-id="69fd9-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="69fd9-118">Каждая строка представляет уровень подклассов.</span><span class="sxs-lookup"><span data-stu-id="69fd9-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="69fd9-119">Например, IPM. Примечание. Это подкласс IPM и суперкласс IPM. Note.Private.</span><span class="sxs-lookup"><span data-stu-id="69fd9-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="69fd9-120">Эти свойства должны состоять из символов ASCII от 32 до 127 и не должны заканчиваются точками (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="69fd9-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="69fd9-121">Операции сортировки и сравнения должны рассматриваться как строка без сноски.</span><span class="sxs-lookup"><span data-stu-id="69fd9-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="69fd9-122">Максимальная возможная длина — 255 символов, но чтобы разрешить квалификаторы MAPI, рекомендуется сохранить исходную длину до 128 символов.</span><span class="sxs-lookup"><span data-stu-id="69fd9-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="69fd9-123">Каждое сообщение необходимо предоставить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="69fd9-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="69fd9-124">Обычно клиентские приложения, создав новое сообщение, устанавливают его, как только [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) возвращается успешно.</span><span class="sxs-lookup"><span data-stu-id="69fd9-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="69fd9-125">Но если свойство не было установлено, когда клиент вызывает [IMAPIProp::SaveChanges,](imapiprop-savechanges.md)хранилище сообщений должно установить для него IPM.</span><span class="sxs-lookup"><span data-stu-id="69fd9-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="69fd9-126">MapI определяет значения:</span><span class="sxs-lookup"><span data-stu-id="69fd9-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="69fd9-127">IPM и IPC предназначены только для использования в качестве суперклассов, а перед хранением или отправкой сообщения должен быть по крайней мере один квалификатор подкласса.</span><span class="sxs-lookup"><span data-stu-id="69fd9-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="69fd9-128">Дополнительные сведения об использовании класса сообщений см. [в сведениях о классах сообщений.](mapi-message-classes.md)</span><span class="sxs-lookup"><span data-stu-id="69fd9-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="69fd9-129">Список необходимых и необязательных свойств для классов сообщений см. в подзаголовках ["Свойства сообщения".](message-properties-overview.md)</span><span class="sxs-lookup"><span data-stu-id="69fd9-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="69fd9-130">Настраиваемый класс сообщений может определять свойства в зарезервированном диапазоне для использования только с этим классом сообщений.</span><span class="sxs-lookup"><span data-stu-id="69fd9-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="69fd9-131">Дополнительные сведения см. [в документе "Идентификаторы свойств".](mapi-property-identifier-overview.md)</span><span class="sxs-lookup"><span data-stu-id="69fd9-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="69fd9-132">Классы сообщений контролируют, в какой папке будет храниться входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="69fd9-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="69fd9-133">Дополнительные сведения см. в [методе IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md)</span><span class="sxs-lookup"><span data-stu-id="69fd9-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="69fd9-134">Дополнительные сведения об использовании классов сообщений с формами и серверами форм см. в подклассе ["Выбор класса сообщений".](choosing-a-message-class.md)</span><span class="sxs-lookup"><span data-stu-id="69fd9-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="69fd9-135">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="69fd9-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69fd9-136">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="69fd9-136">Protocol specifications</span></span>

<span data-ttu-id="69fd9-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69fd9-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69fd9-138">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="69fd9-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69fd9-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69fd9-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69fd9-140">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="69fd9-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="69fd9-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69fd9-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69fd9-142">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="69fd9-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="69fd9-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69fd9-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69fd9-144">Указывает свойства и операции, которые разрешены для представления голосовой почты и факсимили.</span><span class="sxs-lookup"><span data-stu-id="69fd9-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69fd9-145">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="69fd9-145">Header files</span></span>

<span data-ttu-id="69fd9-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69fd9-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="69fd9-147">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="69fd9-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="69fd9-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69fd9-148">Mapitags.h</span></span>
  
> <span data-ttu-id="69fd9-149">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="69fd9-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69fd9-150">См. также</span><span class="sxs-lookup"><span data-stu-id="69fd9-150">See also</span></span>



[<span data-ttu-id="69fd9-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="69fd9-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69fd9-152">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="69fd9-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69fd9-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="69fd9-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69fd9-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="69fd9-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

