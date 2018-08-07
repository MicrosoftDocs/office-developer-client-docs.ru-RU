---
title: Сопоставление атрибутов почты Интернета со свойствами MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4d1bc5fc5a5e304d81ab4252a527d0e52b0d6e3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19809921"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="2295f-103">Сопоставление атрибутов почты Интернета со свойствами MAPI</span><span class="sxs-lookup"><span data-stu-id="2295f-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="2295f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2295f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2295f-105">В этом разделе описываются как поставщика транспорта MAPI или принять во внимание MAPI шлюз, который подключается к Интернету следует использовать во всем свойства сообщения MAPI и атрибуты сообщений транспортный протокол SMTP (Simple Mail).</span><span class="sxs-lookup"><span data-stu-id="2295f-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="2295f-106">SMTP применяется протокол обмена сообщениями на большую часть Интернета.</span><span class="sxs-lookup"><span data-stu-id="2295f-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="2295f-107">Определяет набор заголовков сообщений SMTP — конверт сообщения и содержимое сообщения в формате.</span><span class="sxs-lookup"><span data-stu-id="2295f-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="2295f-108">SMTP полностью описан в набор из двух документов, согласно документу RFC 821 и RFC 822, которые можно найти по номеру FTP и веб-сайтов в Интернете.</span><span class="sxs-lookup"><span data-stu-id="2295f-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="2295f-109">Сведения о протокола SMTP, используемый для связи с SMTP-based почты агенты видеть RFC 821 «Протокол SMTP,» [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="2295f-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="2295f-110">Для адресации и стандартных заголовков сообщений, видеть RFC 822, «Standard для формата из ARPA текста сообщений Интернета» [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="2295f-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="2295f-111">MIME, в разделе RFC 1521 «часть MIME (Multipurpose Internet Mail Extensions) один: механизмы задание и описания формата текстов сообщений Интернета» в [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="2295f-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="2295f-112">Задача сопоставления атрибуты сообщений SMTP для свойства MAPI (и наоборот) — чтобы убедиться, что все содержимое сообщения MAPI, который может быть закодированы с помощью собственного атрибуты сообщений SMTP, надежно обмена между различных MAPI компоненты, которые должны взаимодействовать в Интернете.</span><span class="sxs-lookup"><span data-stu-id="2295f-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="2295f-113">В этом документе основано на уже выполненные работы по таких компонентов в корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2295f-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="2295f-114">В этом документе предполагается Знакомство с транспортов MAPI, TNEF и SMTP почты.</span><span class="sxs-lookup"><span data-stu-id="2295f-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="2295f-115">Он стремится четкое, а не ясен.</span><span class="sxs-lookup"><span data-stu-id="2295f-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="2295f-116">Соглашение «исходящие» относится к почте, которые отправляются из MAPI-совместимое UA или агента передачи сообщений в Интернет и «входящие» ссылается на почтовые сообщения, передаваемые из Интернета в компонент MAPI.</span><span class="sxs-lookup"><span data-stu-id="2295f-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

