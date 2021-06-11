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
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="a7346-103">Каноническое свойство PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="a7346-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="a7346-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7346-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7346-105">Содержит текстовую строку, идентифицирующую определяемый отправителем класс сообщений, например IPM.Note.</span><span class="sxs-lookup"><span data-stu-id="a7346-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7346-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a7346-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7346-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="a7346-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="a7346-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a7346-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7346-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="a7346-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="a7346-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a7346-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7346-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a7346-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a7346-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a7346-112">Area:</span></span>  <br/> |<span data-ttu-id="a7346-113">Распространенная</span><span class="sxs-lookup"><span data-stu-id="a7346-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7346-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7346-114">Remarks</span></span>

<span data-ttu-id="a7346-115">Класс сообщения указывает тип сообщения.</span><span class="sxs-lookup"><span data-stu-id="a7346-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="a7346-116">Он определяет набор свойств, определенных для сообщения, вид информации, которую передает сообщение, и обработку сообщения.</span><span class="sxs-lookup"><span data-stu-id="a7346-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="a7346-117">Эти свойства содержат строки, совмещенные с периодами.</span><span class="sxs-lookup"><span data-stu-id="a7346-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="a7346-118">Каждая строка представляет собой уровень подклассинга.</span><span class="sxs-lookup"><span data-stu-id="a7346-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="a7346-119">Например, IPM. Примечание — это подкласс IPM и суперкласс IPM. Примечание.Private.</span><span class="sxs-lookup"><span data-stu-id="a7346-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="a7346-120">Эти свойства должны состоять из символов ASCII от 32 до 127 и не должны закончиться периодом (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="a7346-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="a7346-121">Сортировка и сравнение операций должны рассматриваться как строка, нечувствительная к делу.</span><span class="sxs-lookup"><span data-stu-id="a7346-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="a7346-122">Максимальная возможная длина — 255 символов, но для того, чтобы позволить комнате MAPI использовать квалификаторы, рекомендуется сохранить исходную длину в 128 символов.</span><span class="sxs-lookup"><span data-stu-id="a7346-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="a7346-123">Каждое сообщение необходимо предоставить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="a7346-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="a7346-124">Обычно клиентские приложения, создав новое сообщение, устанавливают его, как только [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) возвращается успешно.</span><span class="sxs-lookup"><span data-stu-id="a7346-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="a7346-125">Но если свойство не установлено, когда клиент вызывает [IMAPIProp::SaveChanges,](imapiprop-savechanges.md)магазин сообщений должен установить его на IPM.</span><span class="sxs-lookup"><span data-stu-id="a7346-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="a7346-126">Значения, определенные MAPI:</span><span class="sxs-lookup"><span data-stu-id="a7346-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="a7346-127">IPM и IPC предназначены только для суперклассов, и перед хранением или отправкой сообщение должно иметь по крайней мере один квалификатор подкласса.</span><span class="sxs-lookup"><span data-stu-id="a7346-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="a7346-128">Дополнительные сведения об использовании класса сообщений см. в [сообщении Классов.](mapi-message-classes.md)</span><span class="sxs-lookup"><span data-stu-id="a7346-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="a7346-129">Списки необходимых и необязательных свойств для классов сообщений см. в подтопику [о свойствах сообщений.](message-properties-overview.md)</span><span class="sxs-lookup"><span data-stu-id="a7346-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="a7346-130">Настраиваемый класс сообщений может определять свойства в зарезервированном диапазоне только для этого класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="a7346-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="a7346-131">Дополнительные сведения см. [в дополнительных сведениях о идентификаторах свойств.](mapi-property-identifier-overview.md)</span><span class="sxs-lookup"><span data-stu-id="a7346-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="a7346-132">Управление классами сообщений, в которых хранится папка входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="a7346-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="a7346-133">Дополнительные сведения см. в [методе IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md)</span><span class="sxs-lookup"><span data-stu-id="a7346-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="a7346-134">Дополнительные сведения об использовании классов сообщений с формами и серверами форм см. в [подборе класса сообщений.](choosing-a-message-class.md)</span><span class="sxs-lookup"><span data-stu-id="a7346-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a7346-135">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a7346-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7346-136">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a7346-136">Protocol specifications</span></span>

<span data-ttu-id="a7346-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7346-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7346-138">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="a7346-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7346-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7346-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7346-140">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="a7346-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a7346-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7346-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7346-142">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a7346-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="a7346-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7346-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7346-144">Указывает свойства и операции, допустимые для представления голосовой почты и факсимили.</span><span class="sxs-lookup"><span data-stu-id="a7346-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7346-145">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="a7346-145">Header files</span></span>

<span data-ttu-id="a7346-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7346-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7346-147">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a7346-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7346-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a7346-148">Mapitags.h</span></span>
  
> <span data-ttu-id="a7346-149">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="a7346-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7346-150">См. также</span><span class="sxs-lookup"><span data-stu-id="a7346-150">See also</span></span>



[<span data-ttu-id="a7346-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a7346-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7346-152">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a7346-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7346-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a7346-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7346-154">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="a7346-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

