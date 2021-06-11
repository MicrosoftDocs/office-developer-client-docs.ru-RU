---
title: Обзор поставщика транспорта MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404577"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="d6ce7-103">Обзор поставщика транспорта MAPI</span><span class="sxs-lookup"><span data-stu-id="d6ce7-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="d6ce7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6ce7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6ce7-105">Поставщики транспорта обрабатывают передачу и прием сообщений и реализуют безопасность при необходимости.</span><span class="sxs-lookup"><span data-stu-id="d6ce7-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="d6ce7-106">Они также заботятся о любых необходимых задачах по подготовке и постпроцессации.</span><span class="sxs-lookup"><span data-stu-id="d6ce7-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="d6ce7-107">Для каждой активной системы обмена сообщениями обычно используется один поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="d6ce7-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="d6ce7-108">Клиентские приложения взаимодействуют с поставщиком транспорта через поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6ce7-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="d6ce7-109">Поставщики транспорта регистрируются в MAPI для обработки одного или более определенных типов записей получателей.</span><span class="sxs-lookup"><span data-stu-id="d6ce7-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="d6ce7-110">Когда сообщение готово к отправлению, MAPI должен определить, какой поставщик транспорта должен обрабатывать передачу.</span><span class="sxs-lookup"><span data-stu-id="d6ce7-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="d6ce7-111">В зависимости от типа получателя MAPI может даже вызвать несколько поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="d6ce7-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="d6ce7-112">Если недоступный поставщик транспорта является единственным поставщиком транспорта, который может обрабатывать получателя, передача сообщений будет отложена до повторного подключения к этому поставщику.</span><span class="sxs-lookup"><span data-stu-id="d6ce7-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="d6ce7-113">Некоторые системы обмена сообщениями являются безопасными системами; все потенциальные пользователи должны ввести набор допустимых учетных данных, прежде чем будет разрешен доступ.</span><span class="sxs-lookup"><span data-stu-id="d6ce7-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="d6ce7-114">MAPI предотвращает несанкционированный доступ к таким защищенным системам обмена сообщениями с помощью проверки учетных данных поставщика транспорта во время логоса.</span><span class="sxs-lookup"><span data-stu-id="d6ce7-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

