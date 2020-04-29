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
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="6da3d-103">Каноническое свойство PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="6da3d-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="6da3d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6da3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6da3d-105">Содержит текстовую строку, определяющую класс сообщений, определенный отправителем, например IPM. Ноте.</span><span class="sxs-lookup"><span data-stu-id="6da3d-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6da3d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6da3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6da3d-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="6da3d-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="6da3d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6da3d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6da3d-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="6da3d-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="6da3d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6da3d-110">Data type:</span></span>  <br/> |<span data-ttu-id="6da3d-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="6da3d-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="6da3d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6da3d-112">Area:</span></span>  <br/> |<span data-ttu-id="6da3d-113">Распространенная</span><span class="sxs-lookup"><span data-stu-id="6da3d-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6da3d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6da3d-114">Remarks</span></span>

<span data-ttu-id="6da3d-115">Класс Message указывает тип сообщения.</span><span class="sxs-lookup"><span data-stu-id="6da3d-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="6da3d-116">Он определяет набор свойств, определенных для сообщения, тип данных, которые передает сообщение, и способ обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="6da3d-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="6da3d-117">Эти свойства содержат строки, Объединенные с точками.</span><span class="sxs-lookup"><span data-stu-id="6da3d-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="6da3d-118">Каждая строка представляет уровень подклассов.</span><span class="sxs-lookup"><span data-stu-id="6da3d-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="6da3d-119">Например, IPM. Note является подклассом IPM и суперклассом IPM. Note. Private.</span><span class="sxs-lookup"><span data-stu-id="6da3d-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="6da3d-120">Эти свойства должны состоять из символов ASCII от 32 до 127 и не должны заканчиваться точкой (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="6da3d-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="6da3d-121">Операции сортировки и сравнения должны рассматривать его как строку без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="6da3d-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="6da3d-122">Максимально допустимая длина составляет 255 символов, но чтобы разрешить комнате MAPI добавлять квалификаторы, рекомендуется хранить исходную длину в 128 символов.</span><span class="sxs-lookup"><span data-stu-id="6da3d-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="6da3d-123">Для этих свойств требуется каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="6da3d-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="6da3d-124">Как правило, клиентское приложение, создающее новое сообщение, задает его как можно быстрее, чем [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) возвращает успешно.</span><span class="sxs-lookup"><span data-stu-id="6da3d-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="6da3d-125">Но если свойство не было задано, когда клиент вызывает [IMAPIProp:: SaveChanges](imapiprop-savechanges.md), в хранилище сообщений должно быть задано значение IPM.</span><span class="sxs-lookup"><span data-stu-id="6da3d-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="6da3d-126">Для MAPI определены следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6da3d-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="6da3d-127">IPM и IPC предназначены только для подклассов, а в сообщении должен быть по крайней мере один квалификатор подкласса, добавленный перед сохранением или отправкой.</span><span class="sxs-lookup"><span data-stu-id="6da3d-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="6da3d-128">Более подробную информацию об использовании класса сообщений можно узнать в статье [классы сообщений](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="6da3d-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="6da3d-129">Список обязательных и необязательных свойств для классов сообщений приведен в подразделах [о свойствах сообщений](message-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6da3d-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="6da3d-130">Настраиваемый класс сообщения может определять свойства в зарезервированном диапазоне для использования только с этим классом сообщения.</span><span class="sxs-lookup"><span data-stu-id="6da3d-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="6da3d-131">Более подробную информацию можно узнать в статье [об идентификаторах свойств](mapi-property-identifier-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6da3d-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="6da3d-132">Классы сообщений — это контроль над папкой, в которой хранится входящее сообщение.</span><span class="sxs-lookup"><span data-stu-id="6da3d-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="6da3d-133">Дополнительные сведения см. в методе [IMsgStore:: жетрецеивефолдертабле](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="6da3d-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="6da3d-134">Для получения дополнительных сведений об использовании классов сообщений с формами и серверами форм, ознакомьтесь со статьей [Выбор класса сообщений](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="6da3d-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6da3d-135">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6da3d-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6da3d-136">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6da3d-136">Protocol specifications</span></span>

<span data-ttu-id="6da3d-137">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6da3d-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6da3d-138">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6da3d-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6da3d-139">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6da3d-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6da3d-140">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="6da3d-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6da3d-141">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6da3d-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6da3d-142">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6da3d-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="6da3d-143">[[MS — ОКСАУМ]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6da3d-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6da3d-144">Задает свойства и операции, допустимые для представления голосовой почты и факсимильных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6da3d-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6da3d-145">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6da3d-145">Header files</span></span>

<span data-ttu-id="6da3d-146">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6da3d-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="6da3d-147">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6da3d-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="6da3d-148">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="6da3d-148">Mapitags.h</span></span>
  
> <span data-ttu-id="6da3d-149">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="6da3d-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6da3d-150">См. также</span><span class="sxs-lookup"><span data-stu-id="6da3d-150">See also</span></span>



[<span data-ttu-id="6da3d-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6da3d-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6da3d-152">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="6da3d-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6da3d-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6da3d-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6da3d-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6da3d-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

