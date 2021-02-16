---
title: Форматированный текст в MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7f37d65e4beb328c2c92cf0c2ab28586af6bee45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408091"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="6bd71-103">Форматированный текст в MAPI</span><span class="sxs-lookup"><span data-stu-id="6bd71-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="6bd71-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bd71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bd71-105">Текст сообщения можно хранить и передавать с помощью обычного текста или формата.</span><span class="sxs-lookup"><span data-stu-id="6bd71-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="6bd71-106">Форматированный текст улучшает текст сообщения, изменяя его внешний вид, например один или несколько шрифтов, размеров шрифтов или текстовых цветов.</span><span class="sxs-lookup"><span data-stu-id="6bd71-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="6bd71-107">Рекомендуется, чтобы все клиенты и, когда это возможно, все поставщики хранимых сообщений, поддерживают форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="6bd71-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="6bd71-108">Поддержка форматируемого текста в сообщениях повышает эффективность благодаря повышению читаемости сообщений и упростить и повысить эффективность обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="6bd71-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="6bd71-109">Форматированный текст можно реализовать различными способами.</span><span class="sxs-lookup"><span data-stu-id="6bd71-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="6bd71-110">Наиболее распространенный способ — формат RTF.</span><span class="sxs-lookup"><span data-stu-id="6bd71-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="6bd71-111">MAPI определяет три передаваемых свойства для удержания сведений о тексте сообщения: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) для обычного текста, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) для HTML и **PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)для сжатого текста RTF.</span><span class="sxs-lookup"><span data-stu-id="6bd71-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="6bd71-112">Поскольку форматированная версия текста сообщения может быть в два раза больше, чем версия без форматирования, текст RTF сжимается перед его переносом вместе с сообщением и сохраняется в свойстве PR_RTF_COMPRESSED. </span><span class="sxs-lookup"><span data-stu-id="6bd71-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="6bd71-113">Когда пора отобразить сообщение на экране, оно несмещение с помощью функции, предоставляемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="6bd71-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="6bd71-114">MAPI определяет эти два свойства текста сообщения и механизмы преобразования между ними, чтобы клиенты с поддержкой RTF могли работать с клиентами и системами обмена сообщениями, которые не поддерживают форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="6bd71-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="6bd71-115">Синхронизация текста и форматирования</span><span class="sxs-lookup"><span data-stu-id="6bd71-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="6bd71-116">Описывается, как синхронизировать текст сообщения RTF с форматированием.</span><span class="sxs-lookup"><span data-stu-id="6bd71-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="6bd71-117">Поддержка форматированный текст в исходящих сообщениях: обязанности клиента</span><span class="sxs-lookup"><span data-stu-id="6bd71-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="6bd71-118">Описывает обязанности клиентского приложения по поддержке форматированный текст в исходящих сообщениях.</span><span class="sxs-lookup"><span data-stu-id="6bd71-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="6bd71-119">Поддержка форматированный текст во входящих сообщениях: обязанности клиента</span><span class="sxs-lookup"><span data-stu-id="6bd71-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="6bd71-120">Описывает обязанности клиентского приложения по поддержке форматированный текст во входящих сообщениях.</span><span class="sxs-lookup"><span data-stu-id="6bd71-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="6bd71-121">Поддержка форматированный текст: обязанности хранения сообщений</span><span class="sxs-lookup"><span data-stu-id="6bd71-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="6bd71-122">Описание обязанностей по хранию сообщений для поддержки форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="6bd71-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="6bd71-123">Поддержка форматированный текст: отрисовка вложений</span><span class="sxs-lookup"><span data-stu-id="6bd71-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="6bd71-124">Описывает, как выбрать место отображения вложений.</span><span class="sxs-lookup"><span data-stu-id="6bd71-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="6bd71-125">Поддержка форматированный текст: обязанности шлюза</span><span class="sxs-lookup"><span data-stu-id="6bd71-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="6bd71-126">Описывает обязанности шлюза для исходяющих и входящих текстовых сообщений в формате.</span><span class="sxs-lookup"><span data-stu-id="6bd71-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

