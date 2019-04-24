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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327470"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="20887-103">Форматированный текст в MAPI</span><span class="sxs-lookup"><span data-stu-id="20887-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="20887-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20887-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20887-105">Текст сообщения можно сохранить и передать с помощью обычного текста или форматированного текста.</span><span class="sxs-lookup"><span data-stu-id="20887-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="20887-106">Форматированный текст расширяет текст сообщения, изменяя его внешний вид, например, один или несколько шрифтов, размеры шрифтов или цвета текста.</span><span class="sxs-lookup"><span data-stu-id="20887-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="20887-107">Рекомендуется, чтобы все клиенты и каждый поставщик хранилища сообщений поддерживал отформатированный текст.</span><span class="sxs-lookup"><span data-stu-id="20887-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="20887-108">Поддержка форматированного текста в сообщениях добавляет значение путем улучшения удобочитаемости сообщений и упрощения обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="20887-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="20887-109">ОтФорматированный текст можно реализовать различными способами.</span><span class="sxs-lookup"><span data-stu-id="20887-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="20887-110">Наиболее распространенным способом является формат RTF.</span><span class="sxs-lookup"><span data-stu-id="20887-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="20887-111">MAPI определяет три свойства для передачи для хранения сведений о тексте сообщения: **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)) для обычного текста, **ПР_ХТМЛ** ([PidTagHtml](pidtaghtml-canonical-property.md)) для HTML и **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) для текста в формате RTF, который был сжат.</span><span class="sxs-lookup"><span data-stu-id="20887-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="20887-112">Так как форматированная версия текста сообщения может быть в два раза больше, чем у версии без форматирования, текст RTF сжимается перед передачей вместе с сообщением и хранится в свойстве **пр_ртф_компрессед** .</span><span class="sxs-lookup"><span data-stu-id="20887-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="20887-113">Когда на экран выводится сообщение, оно не сжимается с помощью служебной функции, предоставляемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="20887-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="20887-114">MAPI определяет эти два свойства текста сообщения и механизмы для преобразования между ними, чтобы клиенты с поддержкой RTF могли взаимодействовать с клиентами и системами обмена сообщениями, которые не поддерживают форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="20887-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="20887-115">Синхронизация текста и форматирования</span><span class="sxs-lookup"><span data-stu-id="20887-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="20887-116">Сведения о том, как хранить текст сообщения в формате RTF с форматированием.</span><span class="sxs-lookup"><span data-stu-id="20887-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="20887-117">Поддержка форматированного текста в исХодящих сообщениях: обязанности клиентов</span><span class="sxs-lookup"><span data-stu-id="20887-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="20887-118">Описывает функциональные обязанности клиентского приложения для поддержки форматированного текста в исходящих сообщениях.</span><span class="sxs-lookup"><span data-stu-id="20887-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="20887-119">Поддержка форматированного текста во входящих сообщениях: обязанности клиентов</span><span class="sxs-lookup"><span data-stu-id="20887-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="20887-120">Описывает функциональные обязанности клиентского приложения для поддержки форматированного текста во входящих сообщениях.</span><span class="sxs-lookup"><span data-stu-id="20887-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="20887-121">Поддержка форматированного текста: обязанности хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="20887-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="20887-122">Описывает обязанности по хранению сообщений для поддержки форматированного текста.</span><span class="sxs-lookup"><span data-stu-id="20887-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="20887-123">Поддержка форматированного текста: отображение вложений</span><span class="sxs-lookup"><span data-stu-id="20887-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="20887-124">Сведения о том, как выбрать место отображения вложений.</span><span class="sxs-lookup"><span data-stu-id="20887-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="20887-125">Поддержка форматированного текста: обязанности шлюза</span><span class="sxs-lookup"><span data-stu-id="20887-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="20887-126">Описывает обязанности шлюза для исходящих и входящих форматированных текстовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="20887-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

