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
ms.openlocfilehash: bfaa4fd5f561c8138461db6ce8b9033c2a75b96b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580630"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="ab6bf-103">Форматированный текст в MAPI</span><span class="sxs-lookup"><span data-stu-id="ab6bf-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="ab6bf-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab6bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab6bf-105">Текст сообщения, можно хранить и передаваемые сведения с помощью обычного текста или форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="ab6bf-106">Форматированный текст путем изменения внешнего вида в организации, например, один или несколько шрифтов, размеры шрифтов или цвета текста улучшает текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="ab6bf-107">Рекомендуется все клиенты и по возможности все поставщики хранилища сообщений, поддерживают форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="ab6bf-108">Поддержка форматированный текст в сообщениях добавляется значение, улучшение читаемости сообщения и внеся обработки сообщений и удобнее.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="ab6bf-109">Форматированный текст можно реализовать в различными способами.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="ab6bf-110">Чаще всего используется с форматированный текст (RTF).</span><span class="sxs-lookup"><span data-stu-id="ab6bf-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="ab6bf-111">MAPI определяет три передаваемого свойства для хранения сведений текст сообщения: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) для обычного текста, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) для HTML и **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) для текст RTF, которая была свернута.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="ab6bf-112">Так как версию форматированный текст сообщения может быть дважды мере версия без форматирования, текст RTF сжимается до перемещать его с сообщением и хранится в свойстве **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="ab6bf-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="ab6bf-113">После отображения сообщения на экране несжатую с помощью служебной программы функции, предоставляемые MAPI.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="ab6bf-114">MAPI определяет эти два свойства: текстовое сообщение и механизмы для преобразования между ними, чтобы принять во внимание RTF клиенты могут взаимодействовать с клиентами и систем обмена сообщениями, которые не поддерживают форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="ab6bf-115">Синхронизация текста и форматирования</span><span class="sxs-lookup"><span data-stu-id="ab6bf-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="ab6bf-116">Описывается, как синхронизировать с форматированием текст сообщения RTF.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="ab6bf-117">Поддержка форматированного текста в исходящих сообщениях: обязанности клиентов</span><span class="sxs-lookup"><span data-stu-id="ab6bf-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="ab6bf-118">Описывает обязанности клиентского приложения для поддержки форматированный текст в исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="ab6bf-119">Поддержка форматированного текста во входящих сообщениях: обязанности клиентов</span><span class="sxs-lookup"><span data-stu-id="ab6bf-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="ab6bf-120">Описывает обязанности клиентского приложения для поддержки форматированный текст в входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="ab6bf-121">Поддержка форматированного текста: обязанности хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="ab6bf-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="ab6bf-122">Описывает обязанности хранилища сообщений для поддержки форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="ab6bf-123">Поддержка форматированного текста: отображение вложений</span><span class="sxs-lookup"><span data-stu-id="ab6bf-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="ab6bf-124">Описывает способ выбора, где отображаются вложения.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="ab6bf-125">Поддержка форматированного текста: обязанности шлюза</span><span class="sxs-lookup"><span data-stu-id="ab6bf-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="ab6bf-126">Описывает обязанности шлюза для входящих и исходящих сообщений форматированный текст.</span><span class="sxs-lookup"><span data-stu-id="ab6bf-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

