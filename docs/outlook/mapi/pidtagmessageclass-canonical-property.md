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
ms.openlocfilehash: d4e478b053bc1aa81643a60899480ac2ad9d4265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811343"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="ca3a0-103">Каноническое свойство PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="ca3a0-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="ca3a0-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca3a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca3a0-105">Содержит текстовую строку, которая определяет класс отправителя определенное сообщение, такие как IPM. Примечание.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca3a0-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ca3a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca3a0-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="ca3a0-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="ca3a0-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ca3a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ca3a0-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="ca3a0-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="ca3a0-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ca3a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="ca3a0-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="ca3a0-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="ca3a0-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ca3a0-112">Area:</span></span>  <br/> |<span data-ttu-id="ca3a0-113">Common</span><span class="sxs-lookup"><span data-stu-id="ca3a0-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca3a0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ca3a0-114">Remarks</span></span>

<span data-ttu-id="ca3a0-115">Класс сообщения указывает тип сообщения.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="ca3a0-116">Определяет набор свойств, определенных в сообщении передает сведения сообщения и как обрабатывать сообщения.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="ca3a0-117">Эти свойства содержат строк, объединяется с периодов.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="ca3a0-118">Каждая строка представляет уровень подклассы.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="ca3a0-119">Например IPM. Примечание это подкласс IPM и суперклассом IPM. Note.Private.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="ca3a0-120">Эти свойства должны состоять из знаков ASCII 32 до 127 и не должно заканчиваться точкой (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="ca3a0-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="ca3a0-121">Сортировка и сравнение операций должен обрабатывать его как строка без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="ca3a0-122">Возможные Максимальная длина составляет 255 символов, но чтобы разрешить места MAPI для добавления классификаторы рекомендуется что исходное значение длины должны сохраняться в разделе 128 символов.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="ca3a0-123">Каждому сообщению требуется бесплатной этих свойств.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="ca3a0-124">Как правило клиентское приложение, создавать новые сообщения устанавливает его сразу после [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) пройдет успешно.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="ca3a0-125">Однако если свойство не задано, когда клиент вызывает [IMAPIProp::SaveChanges](imapiprop-savechanges.md), хранилища сообщений следует присвоить IPM.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="ca3a0-126">Поддерживаются следующие значения, определенные в MAPI:</span><span class="sxs-lookup"><span data-stu-id="ca3a0-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="ca3a0-127">IPM и производственных Издержек предназначенного для формирования только суперклассов и сообщения должен иметь по крайней мере один квалификатор подкласс добавляться перед хранимых или отправки.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="ca3a0-128">Дополнительные сведения об использовании класс сообщения можно [Классов сообщений](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="ca3a0-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="ca3a0-129">Списки необходимые и дополнительные свойства для классов сообщений содержатся в разделе [о](message-properties-overview.md)свойств сообщения.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="ca3a0-130">Пользовательский класс сообщения можно определить свойства в диапазоне зарезервировано для использования с только что класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="ca3a0-131">Дополнительные сведения [Об идентификаторах свойств](mapi-property-identifier-overview.md)см.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="ca3a0-132">Классы сообщений элемента управления, который получать папку входящих сообщений хранится в.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="ca3a0-133">Для получения дополнительных сведений см [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="ca3a0-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="ca3a0-134">Дополнительные сведения об использовании классов сообщений с помощью форм и форм серверы [Класс сообщения](choosing-a-message-class.md)см.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ca3a0-135">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ca3a0-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca3a0-136">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ca3a0-136">Protocol specifications</span></span>

<span data-ttu-id="ca3a0-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca3a0-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca3a0-138">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca3a0-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca3a0-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca3a0-140">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ca3a0-141">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca3a0-141">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca3a0-142">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="ca3a0-143">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca3a0-143">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca3a0-144">Задает свойства и операции, допустимые для представления сообщений голосовой почты и факсов.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca3a0-145">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ca3a0-145">Header files</span></span>

<span data-ttu-id="ca3a0-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca3a0-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca3a0-147">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="ca3a0-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ca3a0-148">Mapitags.h</span></span>
  
> <span data-ttu-id="ca3a0-149">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="ca3a0-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca3a0-150">См. также</span><span class="sxs-lookup"><span data-stu-id="ca3a0-150">See also</span></span>



[<span data-ttu-id="ca3a0-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ca3a0-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca3a0-152">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ca3a0-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca3a0-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ca3a0-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca3a0-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ca3a0-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

