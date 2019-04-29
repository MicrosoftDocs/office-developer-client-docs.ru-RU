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
ms.openlocfilehash: d983b71c7c92c395740a8ae6f6d3666a8bc2c0c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407195"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="1f11d-103">Выбор набора свойств формы</span><span class="sxs-lookup"><span data-stu-id="1f11d-103">Choosing a form's property set</span></span>

<span data-ttu-id="1f11d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f11d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f11d-105">При внедрении сервера форм необходимо получить свойство для каждого элемента информации, необходимого классу сообщения.</span><span class="sxs-lookup"><span data-stu-id="1f11d-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="1f11d-106">Эти свойства могут быть предварительно определенными свойствами MAPI, а также пользовательскими свойствами, которые вы определяете.</span><span class="sxs-lookup"><span data-stu-id="1f11d-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="1f11d-107">Дополнительные сведения о работе с свойствами содержатся в разделе [Обзор свойств MAPI](mapi-property-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1f11d-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="1f11d-108">Файл конфигурации формы будет содержать список свойств, которые сервер форм предоставляет для клиентских приложений, но это не обязательно должен быть весь список свойств, используемых сервером форм.</span><span class="sxs-lookup"><span data-stu-id="1f11d-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="1f11d-109">Клиентские приложения обычно используют предоставляемые свойства, чтобы позволить пользователям сортировать сообщения в папке или настраивать их интерфейсы каким бы то ни было.</span><span class="sxs-lookup"><span data-stu-id="1f11d-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="1f11d-110">MAPI содержит большой набор предварительно определенных свойств, достаточных для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="1f11d-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="1f11d-111">Однако бывают случаи, когда настраиваемому классу сообщений требуется свойство, которое не определено MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f11d-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="1f11d-112">Вы можете использовать настраиваемые свойства для расширения предопределенного набора свойств MAPI для любых специальных сведений, которые должны поддерживаться сервером форм.</span><span class="sxs-lookup"><span data-stu-id="1f11d-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="1f11d-113">Для определения настраиваемых свойств можно использовать любой из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="1f11d-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="1f11d-114">Выберите имя для свойства и используйте метод [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить тег свойства для него.</span><span class="sxs-lookup"><span data-stu-id="1f11d-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="1f11d-115">Интерфейс [IMAPIProp](imapipropiunknown.md) , через который вызывается этот метод, берется из указателя [iMessage](imessageimapiprop.md) , который передается серверу формы при создании сообщения.</span><span class="sxs-lookup"><span data-stu-id="1f11d-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="1f11d-116">Обратите внимание, что имя свойства должно быть строкой с широким символом.</span><span class="sxs-lookup"><span data-stu-id="1f11d-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="1f11d-117">Самостоятельно определите тег настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="1f11d-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="1f11d-118">Настраиваемые теги свойств должны находиться в диапазоне от 0x6800 до 0x7BFF.</span><span class="sxs-lookup"><span data-stu-id="1f11d-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="1f11d-119">Свойства в этом диапазоне относятся к определенному классу Message.</span><span class="sxs-lookup"><span data-stu-id="1f11d-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="1f11d-120">Дополнительные сведения об определении настраиваемых свойств приведены в статье [Определение новых свойств MAPI](defining-new-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1f11d-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="1f11d-121">Серверы форм с текстом сообщения часто используют свойство **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) для его хранения.</span><span class="sxs-lookup"><span data-stu-id="1f11d-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="1f11d-122">Если сервер форм использует **пр_ртф_компрессед**, необходимо также убедиться, что свойство **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)) содержит только текстовую версию текста сообщения, на тот случай, если полученное сообщение прочитано клиентом, не поддерживающим форматированный текст. Текст сообщения в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="1f11d-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f11d-123">См. также</span><span class="sxs-lookup"><span data-stu-id="1f11d-123">See also</span></span>

- [<span data-ttu-id="1f11d-124">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="1f11d-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

