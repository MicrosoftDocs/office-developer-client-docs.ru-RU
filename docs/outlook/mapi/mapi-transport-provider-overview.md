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
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="88f12-103">Обзор поставщика транспорта MAPI</span><span class="sxs-lookup"><span data-stu-id="88f12-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="88f12-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88f12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88f12-105">Поставщики транспорта обрабатывают передачу и прием сообщений и реализуют безопасность, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="88f12-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="88f12-106">Они также позаботится о необходимых задачах предварительной обработки и обработки.</span><span class="sxs-lookup"><span data-stu-id="88f12-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="88f12-107">Для каждой активной системы обмена сообщениями обычно существует один поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="88f12-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="88f12-108">Клиентские приложения взаимодействуют с поставщиком транспорта через поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="88f12-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="88f12-109">Поставщики транспорта регистрируются с помощью MAPI для обработки одного или нескольких определенных типов записей получателей.</span><span class="sxs-lookup"><span data-stu-id="88f12-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="88f12-110">Когда сообщение готово к отправке, MAPI должен определить, какой поставщик транспорта должен обрабатывать передачу.</span><span class="sxs-lookup"><span data-stu-id="88f12-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="88f12-111">В зависимости от типа получателя MAPI может даже вызывать более одного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="88f12-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="88f12-112">Если недоступный поставщик транспорта является единственным, который может обработать получателя, передача сообщений будет отложена до тех пор, пока подключение с этим поставщиком невозможно будет повторно установить.</span><span class="sxs-lookup"><span data-stu-id="88f12-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="88f12-113">Некоторые системы обмена сообщениями являются безопасными системами; всем потенциальным пользователям необходимо ввести набор действительных учетных данных, прежде чем разрешить доступ.</span><span class="sxs-lookup"><span data-stu-id="88f12-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="88f12-114">MAPI предотвращает несанкционированный доступ к таким безопасным системам обмена сообщениями, используя поставщик транспорта для проверки учетных данных во время входа.</span><span class="sxs-lookup"><span data-stu-id="88f12-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

