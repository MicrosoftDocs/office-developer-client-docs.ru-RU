---
title: Сопоставление атрибутов интернет-почты с свойствами MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355820"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="3b09f-103">Сопоставление атрибутов интернет-почты с свойствами MAPI</span><span class="sxs-lookup"><span data-stu-id="3b09f-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="3b09f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b09f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b09f-105">В этом приложении описывается, как поставщик транспорта MAPI или шлюз MAPI, который подключается к Интернету, должен переводить между свойствами сообщений MAPI и атрибутами сообщения Simple Mail Transport Protocol (SMTP).</span><span class="sxs-lookup"><span data-stu-id="3b09f-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="3b09f-106">SMTP — это протокол обмена сообщениями, используемый на большей части Интернета.</span><span class="sxs-lookup"><span data-stu-id="3b09f-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="3b09f-107">SMTP определяет набор заглавных заглавных сообщений — конверт сообщений — и формат контента сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b09f-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="3b09f-108">SMTP полностью задокументирован в наборе двух документов RFC 821 и RFC 822, которые можно найти на нескольких сайтах FTP и WWW в Интернете.</span><span class="sxs-lookup"><span data-stu-id="3b09f-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="3b09f-109">Сведения о протоколе SMTP, используемом для связи с почтовыми агентами на основе SMTP, см. в рубрике RFC 821, "Простой протокол передачи почты". [https://www.rfc-editor.org](https://www.rfc-editor.org)</span><span class="sxs-lookup"><span data-stu-id="3b09f-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="3b09f-110">Для адресов и стандартных заглавных заглавных сообщений см. в тексте RFC 822", "Стандарт для формата текстовых сообщений в Интернете [https://www.rfc-editor.org](https://www.rfc-editor.org) ARPA".</span><span class="sxs-lookup"><span data-stu-id="3b09f-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="3b09f-111">Для MIME см. в рубрике RFC 1521", "MIME (многоцелевые расширения интернет-почты) Часть 1: механизмы указания и описания формата органов интернет-сообщений". [https://www.rfc-editor.org](https://www.rfc-editor.org)</span><span class="sxs-lookup"><span data-stu-id="3b09f-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="3b09f-112">Цель сопоставления атрибутов SMTP-сообщений со свойствами MAPI (и наоборот) заключается в том, чтобы обеспечить надежное обмен полным контентом сообщений MAPI, которые могут быть закодированы с использованием атрибутов сообщений SMTP, между различными компонентами MAPI, которые должны общаться через Интернет.</span><span class="sxs-lookup"><span data-stu-id="3b09f-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="3b09f-113">Этот документ основан на уже проделаной работе по таким компонентам в Корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3b09f-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="3b09f-114">В этом документе предполагается знакомство с транспортами MAPI, TNEF и SMTP-почтой.</span><span class="sxs-lookup"><span data-stu-id="3b09f-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="3b09f-115">Он стремится быть кратким, а не предельно понятным.</span><span class="sxs-lookup"><span data-stu-id="3b09f-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="3b09f-116">Как конвенция, "исходящие" относится к почте, перемещающейся из UA или MTA, совместимого с MAPI, в Интернет, а "входящие" — к почте, перемещающейся из Интернета в компонент MAPI.</span><span class="sxs-lookup"><span data-stu-id="3b09f-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

