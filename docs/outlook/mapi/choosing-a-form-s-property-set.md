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
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="2c787-103">Выбор набора свойств формы</span><span class="sxs-lookup"><span data-stu-id="2c787-103">Choosing a form's property set</span></span>

<span data-ttu-id="2c787-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c787-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c787-105">При реализации сервера форм необходимо иметь свойство для каждого фрагмента информации, необходимой классу сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c787-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="2c787-106">Эти свойства могут быть заранее определенными свойствами MAPI или настраиваемые свойства, которые вы определяете.</span><span class="sxs-lookup"><span data-stu-id="2c787-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="2c787-107">Дополнительные сведения о работе с свойствами см. в [обзоре свойств MAPI.](mapi-property-overview.md)</span><span class="sxs-lookup"><span data-stu-id="2c787-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="2c787-108">В файле конфигурации формы будет содержаться список свойств, которые сервер формы предоставляет для использования клиентских приложений, но это не должен быть весь список свойств, используемых на сервере форм.</span><span class="sxs-lookup"><span data-stu-id="2c787-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="2c787-109">Клиентские приложения обычно используют выставленные свойства, чтобы пользователи могли сортировать сообщения в папке или настраивать интерфейсы каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="2c787-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="2c787-110">MAPI имеет большой набор предопределяемых свойств, которые достаточно для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="2c787-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="2c787-111">Однако иногда настраиваемый класс сообщений нуждается в свойстве, которое MAPI не определяет.</span><span class="sxs-lookup"><span data-stu-id="2c787-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="2c787-112">Вы можете использовать настраиваемые свойства для расширения предопределяемого набора свойств MAPI для любых специальных сведений, которые необходимо поддерживать серверу форм.</span><span class="sxs-lookup"><span data-stu-id="2c787-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="2c787-113">Для определения настраиваемого свойства можно использовать любой из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="2c787-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="2c787-114">Выберите имя свойства и используйте метод [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства для него.</span><span class="sxs-lookup"><span data-stu-id="2c787-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="2c787-115">Интерфейс [IMAPIProp,](imapipropiunknown.md) с помощью которого вы называете этот метод, поступает из указателя [IMessage,](imessageimapiprop.md) который передается на сервер формы после создания сообщения.</span><span class="sxs-lookup"><span data-stu-id="2c787-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="2c787-116">Обратите внимание, что имя свойства должно быть строкой с широким характером.</span><span class="sxs-lookup"><span data-stu-id="2c787-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="2c787-117">Определите настраиваемый тег свойства самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="2c787-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="2c787-118">Пользовательские теги свойств должны быть в диапазоне 0x6800 через 0x7BFF.</span><span class="sxs-lookup"><span data-stu-id="2c787-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="2c787-119">Свойства в этом диапазоне являются специфическими для класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c787-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="2c787-120">Дополнительные сведения об определении настраиваемой свойства см. в [определении новых свойств MAPI.](defining-new-mapi-properties.md)</span><span class="sxs-lookup"><span data-stu-id="2c787-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="2c787-121">Серверы форм с текстом сообщения часто используют **свойство** [PR_RTF_COMPRESSED (PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)для хранения.</span><span class="sxs-lookup"><span data-stu-id="2c787-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="2c787-122">Если на сервере формы используется **PR_RTF_COMPRESSED,** оно также должно убедиться, что свойство **PR_BODY** [(PidTagBody)](pidtagbody-canonical-property.md)содержит только текстовую версию текста сообщения, если в результате сообщение будет прочитано клиентом, который не поддерживает текст сообщения Rich Text Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="2c787-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c787-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2c787-123">See also</span></span>

- [<span data-ttu-id="2c787-124">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="2c787-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

