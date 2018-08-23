---
title: Текст сообщения с тегами TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1d514dc8b50183e5d07d71b421a441487e933580
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588862"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="f2b42-103">Текст сообщения с тегами TNEF</span><span class="sxs-lookup"><span data-stu-id="f2b42-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="f2b42-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2b42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2b42-105">Текст с тегами сообщения используется TNEF для устранения положения вложения в сообщении родительского.</span><span class="sxs-lookup"><span data-stu-id="f2b42-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="f2b42-106">Это делается путем добавления заполнителя в качестве текста сообщения в позиции вложения.</span><span class="sxs-lookup"><span data-stu-id="f2b42-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="f2b42-107">Заполнителя или вложения тег описывает вложение таким образом, что TNEF знает о разрешении вложение и положение.</span><span class="sxs-lookup"><span data-stu-id="f2b42-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="f2b42-108">Теги форматируются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f2b42-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="f2b42-109">** \<Название объекта\> ** и ** \<имя файла\> ** являются переменными, содержащий значения, которые берутся из самого вложение.</span><span class="sxs-lookup"><span data-stu-id="f2b42-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="f2b42-110">В тех случаях, где эти значения недоступны название по умолчанию в зависимости от типа вложения TNEF.</span><span class="sxs-lookup"><span data-stu-id="f2b42-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="f2b42-111">** \<KeyNum\> ** переменная содержит текстовое представление ключа вложения, назначенный вложения с TNEF.</span><span class="sxs-lookup"><span data-stu-id="f2b42-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="f2b42-112">Базовое значение ключа передается в вызов [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="f2b42-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="f2b42-113">Базовое значение не должно быть равно нулю и не должны быть одинаковыми для каждого вызова **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="f2b42-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="f2b42-114">Должно быть достаточно для использования псевдо на основе системы времени из любой генератор случайных чисел, библиотека времени выполнения предоставляет, при условии, что гарантирует, что они не могут быть нулевой случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="f2b42-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="f2b42-115">** \<Передачи имя\> ** переменная содержит либо потока имя передано [OpenTnefStreamEx](opentnefstreamex.md) звонок или значение свойства **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f2b42-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f2b42-116">Свойство **PR_ATTACH_TRANSPORT_NAME** и ** \<передачи имя\> ** переменной в теге текста сообщения не работают с именем реализации поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="f2b42-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="f2b42-117">Эти элементы представляют имя вложения для поставщика транспорта и системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f2b42-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="f2b42-118">Текст сообщения является меткой при поставщика транспорта запрашивает текст с тегами сообщения путем вызова метода [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="f2b42-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="f2b42-119">При чтении из потока текст с тегами TNEF заменяет один символ, который был в качестве текста сообщения по индексу, представленные в свойстве **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) с помощью соответствующего тега.</span><span class="sxs-lookup"><span data-stu-id="f2b42-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="f2b42-120">При записи в поток текста с тегами TNEF проверяет входные данные для тегов, находит связанное вложение и заменяет тега одним пробелом.</span><span class="sxs-lookup"><span data-stu-id="f2b42-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="f2b42-121">Обратите внимание на то, что с помощью текст с тегами сообщения, поставщика транспорта можно сохранить размещение вложения независимо от того, большинство изменений, внесенных в текст сообщения систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f2b42-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

