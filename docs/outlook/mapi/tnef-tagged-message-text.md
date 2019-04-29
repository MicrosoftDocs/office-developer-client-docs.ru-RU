---
title: Текст сообщения с тегами в формате TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419921"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="cd1b1-103">Текст сообщения с тегами в формате TNEF</span><span class="sxs-lookup"><span data-stu-id="cd1b1-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="cd1b1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd1b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd1b1-105">ФОРМАТ TNEF использует текст сообщения с тегами для разрешения положений вложений в родительском сообщении.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="cd1b1-106">Это делается путем добавления заполнителя места в тексте сообщения в позиции вложения.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="cd1b1-107">Этот держатель или тег вложений описывает вложение таким образом, что формат TNEF знает, как Разрешить вложение и его положение.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="cd1b1-108">Теги форматируются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cd1b1-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="cd1b1-109">\*\* \<Заголовок\> объекта\*\* **и \<имя\> файла** — это переменные, содержащие значения, которые берутся из самого вложения.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="cd1b1-110">В случаях, когда эти значения недоступны, заголовок по умолчанию задается в формате TNEF на основе типа вложения.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="cd1b1-111">Переменная \*\* \<кэйнум\> \*\* содержит текстовое представление ключа вложения, назначенного вложению, в формате TNEF.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="cd1b1-112">Базовое значение ключа передается в вызов [опентнефстреамекс](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="cd1b1-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="cd1b1-113">Базовое значение не должно быть нулевым и не должно быть одинаковым для каждого вызова **опентнефстреамекс**.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="cd1b1-114">Должно быть достаточно использовать псевдослучайных случайных чисел на основе системного времени из любого генератора случайных чисел, предоставляемого библиотекой времени выполнения, если гарантируется, что они никогда не равны нулю.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="cd1b1-115">Переменная \*\* \<имени\> транспорта\*\* содержит либо имя потока, переданное в вызов [опентнефстреамекс](opentnefstreamex.md) , либо значение свойства **пр_аттач_транспорт_наме** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cd1b1-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cd1b1-116">Свойство **пр_аттач_транспорт_наме** и переменная \*\* \<имени\> транспорта\*\* в теге Text сообщения не имеют отношения к имени реализуемого поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="cd1b1-117">Эти элементы представляют имя вложения для поставщика транспорта и системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="cd1b1-118">Текст сообщения помечается, когда поставщик транспорта запрашивает текст сообщения с тегами, вызывая метод [итнеф:: опентагжедбоди](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="cd1b1-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="cd1b1-119">При чтении из потока текста с тегами в формате TNEF заменяется один символ, который был в тексте сообщения в индексе, указанном в свойстве **пр_рендеринг_поситион** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) с соответствующим тегом.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="cd1b1-120">При записи в поток текста с тегами TNEF проверяет входящие данные для тегов, находит связанное вложение и заменяет тег на один символ пробела.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="cd1b1-121">Обратите внимание, что с помощью текста сообщения с тегами поставщик транспорта может сохранить расположение вложений независимо от большинства изменений, внесенных в текст сообщения системами обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="cd1b1-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

