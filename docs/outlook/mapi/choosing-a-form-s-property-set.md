---
title: Выбор набора свойств формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0ff8d9f1ae25c55d66847b8c0e5e66c406dfdfba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586153"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="a1040-103">Выбор набора свойств формы</span><span class="sxs-lookup"><span data-stu-id="a1040-103">Choosing a form's property set</span></span>

<span data-ttu-id="a1040-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1040-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1040-105">При реализации вашего сервера форм необходимо иметь свойства для каждого элемента данных, которое должно класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1040-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="a1040-106">Эти свойства могут быть предварительно определенные свойства MAPI, или они могут быть настраиваемые свойства, которые можно определить.</span><span class="sxs-lookup"><span data-stu-id="a1040-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="a1040-107">Дополнительные сведения о работе со свойствами можно [Обзор свойств MAPI](mapi-property-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a1040-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="a1040-108">Файл конфигурации формы будет содержать список свойств, которые сервер форма предоставляет доступ для клиентских приложений, для использования, но это не должен быть полный список свойств, используемых сервером формы.</span><span class="sxs-lookup"><span data-stu-id="a1040-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="a1040-109">Клиентские приложения обычно используется этим свойствам чтобы позволить пользователям сортировки сообщений в папке или настроить их интерфейсы каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="a1040-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="a1040-110">MAPI имеет большой набор предварительно определенные свойства, достаточно для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="a1040-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="a1040-111">Тем не менее бывают ситуации, когда пользовательский класс сообщения требуется свойство, которое MAPI не определен.</span><span class="sxs-lookup"><span data-stu-id="a1040-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="a1040-112">Настраиваемые свойства можно использовать для расширения MAPI предопределенное набор свойств для сервера форма должна поддерживать особые сведения.</span><span class="sxs-lookup"><span data-stu-id="a1040-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="a1040-113">Можно использовать один из указанных ниже способов для определения пользовательских свойств:</span><span class="sxs-lookup"><span data-stu-id="a1040-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="a1040-114">Выберите имя свойства и использовать метод [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения свойства тега.</span><span class="sxs-lookup"><span data-stu-id="a1040-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="a1040-115">Интерфейс [IMAPIProp](imapipropiunknown.md) , через который вызове этого метода извлекаются из указателя [IMessage](imessageimapiprop.md) , которое передается на сервер формы при создании сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1040-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="a1040-116">Обратите внимание на то, что имя свойства должна быть строка Юникода.</span><span class="sxs-lookup"><span data-stu-id="a1040-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="a1040-117">Определение настраиваемого свойства tag самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="a1040-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="a1040-118">Теги настраиваемого свойства должны находиться в диапазоне 0x6800 через 0x7BFF.</span><span class="sxs-lookup"><span data-stu-id="a1040-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="a1040-119">Свойства в этот диапазон — это класс сообщения определенного.</span><span class="sxs-lookup"><span data-stu-id="a1040-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="a1040-120">Дополнительные сведения об определении настраиваемые свойства в разделе [Определение нового свойства MAPI](defining-new-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a1040-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="a1040-121">Форма серверов, на которых текста сообщения часто свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) сохраните ее.</span><span class="sxs-lookup"><span data-stu-id="a1040-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="a1040-122">Если на сервере формы используется **PR_RTF_COMPRESSED**, его необходимо убедиться, что свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) содержит текстовой версии текста сообщения в случае, если чтение итогового сообщения с клиента, который не поддерживает формат RTF Текст сообщения в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="a1040-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1040-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a1040-123">See also</span></span>

- [<span data-ttu-id="a1040-124">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="a1040-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

