---
title: Общие сведения о поставщике транспорта MAPI
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
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="afa8a-103">Общие сведения о поставщике транспорта MAPI</span><span class="sxs-lookup"><span data-stu-id="afa8a-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="afa8a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="afa8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="afa8a-105">Поставщики транспорта обрабатывают передачу и прием сообщений и реализуют безопасность при необходимости.</span><span class="sxs-lookup"><span data-stu-id="afa8a-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="afa8a-106">Они также принимают на себя все необходимые задачи предварительной и постобуссации.</span><span class="sxs-lookup"><span data-stu-id="afa8a-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="afa8a-107">Обычно для каждой активной системы обмена сообщениями существует один поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="afa8a-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="afa8a-108">Клиентские приложения взаимодействуют с поставщиком транспорта через поставщика хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="afa8a-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="afa8a-109">Поставщики транспорта регистрируются в MAPI для обработки одного или более определенных типов записей получателей.</span><span class="sxs-lookup"><span data-stu-id="afa8a-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="afa8a-110">Когда сообщение будет готово к передаче, MAPI должен определить, какой поставщик транспорта должен обрабатывать передачу.</span><span class="sxs-lookup"><span data-stu-id="afa8a-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="afa8a-111">В зависимости от типа получателя MAPI может вызывать несколько поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="afa8a-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="afa8a-112">Если единственным поставщиком транспорта, который может обработать получателя, является недоступный поставщик транспорта, передача сообщений будет отложена до тех пор, пока подключение с этим поставщиком не будет восстановиться.</span><span class="sxs-lookup"><span data-stu-id="afa8a-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="afa8a-113">Некоторые системы обмена сообщениями являются защищенными системами; все потенциальные пользователи должны ввести набор действительных учетных данных, прежде чем будет разрешен доступ.</span><span class="sxs-lookup"><span data-stu-id="afa8a-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="afa8a-114">MAPI предотвращает несанкционированный доступ к таким защищенным системам обмена сообщениями за счет того, что поставщик транспорта проверяет учетные данные во время входа.</span><span class="sxs-lookup"><span data-stu-id="afa8a-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

