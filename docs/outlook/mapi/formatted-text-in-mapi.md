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
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="e42f6-103">Форматированный текст в MAPI</span><span class="sxs-lookup"><span data-stu-id="e42f6-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="e42f6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e42f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e42f6-105">Текст сообщения можно хранить и передавать с помощью обычного текста или форматного текста.</span><span class="sxs-lookup"><span data-stu-id="e42f6-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="e42f6-106">Форматированный текст улучшает текст сообщения, изменяя его внешний вид с помощью, например, одного или более шрифтов, размеров шрифтов или цветов текста.</span><span class="sxs-lookup"><span data-stu-id="e42f6-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="e42f6-107">Рекомендуется, чтобы все клиенты и по возможности все поставщики магазинов сообщений поддержали форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="e42f6-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="e42f6-108">Поддержка форматируемого текста в сообщениях повышает ценность за счет повышения читаемости сообщений и упростить и повысить эффективность обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="e42f6-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="e42f6-109">Форматированный текст можно реализовать различными способами.</span><span class="sxs-lookup"><span data-stu-id="e42f6-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="e42f6-110">Наиболее распространенным способом является формат "Богатый текст" (RTF).</span><span class="sxs-lookup"><span data-stu-id="e42f6-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="e42f6-111">MAPI определяет три передающихся свойства для размещения текстовых данных сообщений: **PR_BODY** [(PidTagBody)](pidtagbody-canonical-property.md)для обычного текста, **PR_HTML** [(PidTagHtml)](pidtaghtml-canonical-property.md)для HTML и **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)для сжатого текста RTF.</span><span class="sxs-lookup"><span data-stu-id="e42f6-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="e42f6-112">Так как форматированная версия текста сообщения может быть в два раза больше, чем версия без форматирования, текст RTF сжимается перед его переносом с сообщением и хранением в **свойстве** PR_RTF_COMPRESSED.</span><span class="sxs-lookup"><span data-stu-id="e42f6-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="e42f6-113">Когда пришло время отображать сообщение на экране, оно отпечаток с помощью функции утилиты, предоставляемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="e42f6-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="e42f6-114">MAPI определяет эти два свойства текста сообщения и механизмы преобразования между ними, чтобы клиенты, осведомленные о RTF, могли работать с клиентами и системами обмена сообщениями, которые не поддерживают форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="e42f6-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="e42f6-115">Синхронизация текста и форматирования</span><span class="sxs-lookup"><span data-stu-id="e42f6-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="e42f6-116">Описывает, как синхронизировать текст сообщения RTF с форматированием.</span><span class="sxs-lookup"><span data-stu-id="e42f6-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="e42f6-117">Поддержка форматного текста в исходящих сообщениях: клиентские обязанности</span><span class="sxs-lookup"><span data-stu-id="e42f6-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="e42f6-118">Описывает обязанности клиентского приложения по поддержке форматного текста в исходящих сообщениях.</span><span class="sxs-lookup"><span data-stu-id="e42f6-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="e42f6-119">Поддержка форматного текста в входящих сообщениях: клиентские обязанности</span><span class="sxs-lookup"><span data-stu-id="e42f6-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="e42f6-120">Описывает обязанности клиентского приложения для поддержки форматного текста в входящих сообщениях.</span><span class="sxs-lookup"><span data-stu-id="e42f6-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="e42f6-121">Поддержка форматного текста: обязанности магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="e42f6-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="e42f6-122">Описывает обязанности хранения сообщений для поддержки форматного текста.</span><span class="sxs-lookup"><span data-stu-id="e42f6-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="e42f6-123">Поддержка форматного текста: отрисовка вложений</span><span class="sxs-lookup"><span data-stu-id="e42f6-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="e42f6-124">Описывает, как выбрать, где отрисовка вложений.</span><span class="sxs-lookup"><span data-stu-id="e42f6-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="e42f6-125">Поддержка форматного текста: обязанности шлюза</span><span class="sxs-lookup"><span data-stu-id="e42f6-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="e42f6-126">Описывает обязанности шлюза для исходяющих и входящих текстовых сообщений в формате.</span><span class="sxs-lookup"><span data-stu-id="e42f6-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

