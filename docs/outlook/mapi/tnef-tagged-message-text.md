---
title: TNEF-Tagged сообщения
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
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="483b3-103">TNEF-Tagged сообщения</span><span class="sxs-lookup"><span data-stu-id="483b3-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="483b3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="483b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="483b3-105">Помеченный текст сообщения используется TNEF для решения позиций вложений в родительском сообщении.</span><span class="sxs-lookup"><span data-stu-id="483b3-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="483b3-106">Это делается путем добавления держателя места в текст сообщения в положении вложения.</span><span class="sxs-lookup"><span data-stu-id="483b3-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="483b3-107">Этот держатель места или тег вложения описывает вложение таким образом, чтобы TNEF знал, как разрешить вложение и его положение.</span><span class="sxs-lookup"><span data-stu-id="483b3-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="483b3-108">Теги отформатированы следующим образом:</span><span class="sxs-lookup"><span data-stu-id="483b3-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="483b3-109">**\< Название \> объекта** и **\< имя файла \>** — это переменные, содержащие значения, взятые из самого вложения.</span><span class="sxs-lookup"><span data-stu-id="483b3-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="483b3-110">В случаях, когда эти значения недоступны, название по умолчанию является TNEF на основе типа вложения.</span><span class="sxs-lookup"><span data-stu-id="483b3-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="483b3-111">Переменная **\< KeyNum \>** содержит текстовое представление ключа вложения, назначенного Вложением TNEF.</span><span class="sxs-lookup"><span data-stu-id="483b3-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="483b3-112">Базовое значение ключа передается в [вызов OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="483b3-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="483b3-113">Базовое значение не должно быть нулевым и не должно быть одинаковым для каждого звонка **в OpenTnefStreamEx.**</span><span class="sxs-lookup"><span data-stu-id="483b3-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="483b3-114">Должно быть достаточно использовать псевдо случайные числа в зависимости от системного времени от любого генератора случайных чисел, которые предоставляет библиотека run-time, до тех пор, пока вы гарантируете, что они никогда не будут нулем.</span><span class="sxs-lookup"><span data-stu-id="483b3-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="483b3-115">Переменная **\< \> "Имя** транспорта" содержит имя потока, переданное в вызов [OpenTnefStreamEx,](opentnefstreamex.md) или значение свойства **PR_ATTACH_TRANSPORT_NAME** [(PidTagAttachTransportName).](pidtagattachtransportname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="483b3-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="483b3-116">Свойство **PR_ATTACH_TRANSPORT_NAME** и переменная **\< "Имя \>** транспорта" в текстовом теге сообщения не имеют ничего общего с именем реализуемого поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="483b3-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="483b3-117">Эти элементы представляют имя вложения для поставщика транспорта и системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="483b3-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="483b3-118">Текст сообщения помечен, когда поставщик транспорта просит помеченный текст сообщения, позвонив по методу [ITnef::OpenTaggedBody.](itnef-opentaggedbody.md)</span><span class="sxs-lookup"><span data-stu-id="483b3-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="483b3-119">При чтении из помеченного текстового потока TNEF заменяет один символ, который был в тексте сообщения в индексе, предоставленном в свойстве **PR_RENDERING_POSITION** [(PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)соответствующим тегом.</span><span class="sxs-lookup"><span data-stu-id="483b3-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="483b3-120">При записи в текстовый поток с тегами TNEF проверяет входящие данные для тегов, находит связанное вложение и заменяет тег одним пробелом.</span><span class="sxs-lookup"><span data-stu-id="483b3-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="483b3-121">Обратите внимание, что с помощью помеченного текста сообщения поставщик транспорта может сохранять расположение вложений независимо от большинства изменений, внесенных в текст сообщения системами обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="483b3-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

