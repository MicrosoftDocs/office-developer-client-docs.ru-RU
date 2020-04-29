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
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355820"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="1eb19-103">Сопоставление атрибутов почты Интернета со свойствами MAPI</span><span class="sxs-lookup"><span data-stu-id="1eb19-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="1eb19-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1eb19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1eb19-105">В этом приложении описывается, как поставщик транспорта MAPI или шлюз, поддерживающий MAPI, который подключается к Интернету, должен переключаться между свойствами сообщений MAPI и атрибутами SMTP-сообщений.</span><span class="sxs-lookup"><span data-stu-id="1eb19-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="1eb19-106">SMTP — это протокол обмена сообщениями, используемый в большей части Интернета.</span><span class="sxs-lookup"><span data-stu-id="1eb19-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="1eb19-107">SMTP определяет набор заголовков сообщений — конверт сообщения и формат содержимого сообщения.</span><span class="sxs-lookup"><span data-stu-id="1eb19-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="1eb19-108">Протокол SMTP полностью задокументирован в наборе из двух документов, RFC 821 и RFC 822, которые можно найти на веб-сайте с несколькими FTP-и веб-сайтами.</span><span class="sxs-lookup"><span data-stu-id="1eb19-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="1eb19-109">Сведения о протоколе SMTP, используемом для подключения к агентам почтовых ящиков SMTP, приведены в [https://www.rfc-editor.org](https://www.rfc-editor.org)статье RFC 821, "Simple Mail Transfer Protocol".</span><span class="sxs-lookup"><span data-stu-id="1eb19-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="1eb19-110">Для адресации и стандартных заголовков сообщений ознакомьтесь со статьей RFC 822, "Standard for Format Text Text messages [https://www.rfc-editor.org](https://www.rfc-editor.org)" в Интернете.</span><span class="sxs-lookup"><span data-stu-id="1eb19-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="1eb19-111">Сведения о MIME: RFC 1521, "MIME (многоцелевые расширения электронной почты в Интернете)" — это механизмы для указания и описания формата основных текстов сообщений Интернета [https://www.rfc-editor.org](https://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="1eb19-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="1eb19-112">Для сопоставления атрибутов сообщений SMTP со свойствами MAPI (и наоборот) необходимо обеспечить надежное обмен содержимым всех сообщений MAPI, которые могут быть закодированы с помощью встроенных атрибутов SMTP-сообщений, между различными компонентами MAPI, которые должны поддерживать связь через Интернет.</span><span class="sxs-lookup"><span data-stu-id="1eb19-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="1eb19-113">Этот документ основан на работе, уже выполненной в таких компонентах корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1eb19-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="1eb19-114">В этом документе предполагается познакомиться с транспортами MAPI, TNEF и SMTP-почтой.</span><span class="sxs-lookup"><span data-stu-id="1eb19-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="1eb19-115">Он должен быть кратким, а не абундантли ясно.</span><span class="sxs-lookup"><span data-stu-id="1eb19-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="1eb19-116">Как правило, "Исходящие" относится к сообщениям, переходящим из MAPI, совместимым с MAPI или через Интернет, а "входящий" — к почте, переданной из Интернета в компонент MAPI.</span><span class="sxs-lookup"><span data-stu-id="1eb19-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

