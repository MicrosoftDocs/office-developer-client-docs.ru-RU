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
ms.openlocfilehash: 11cd1040bb228d789248a89184572b87cd1688ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809859"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="feb57-103">Обзор поставщика транспорта MAPI</span><span class="sxs-lookup"><span data-stu-id="feb57-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="feb57-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="feb57-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="feb57-105">Поставщики транспорта обработки передачи сообщений и прием и обеспечения безопасности, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="feb57-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="feb57-106">Они также взяла на себя любые необходимые предварительной обработки и постобработки задачи.</span><span class="sxs-lookup"><span data-stu-id="feb57-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="feb57-107">Отсутствует поставщик обычно один транспорта для каждой активной системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="feb57-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="feb57-108">Клиентские приложения общаться с помощью поставщика транспорта через поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="feb57-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="feb57-109">Зарегистрируйте поставщиками транспорта MAPI для обработки одного или нескольких отдельных типов получателей.</span><span class="sxs-lookup"><span data-stu-id="feb57-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="feb57-110">Если сообщение не готово к отправке, MAPI необходимо определить, какие поставщика транспорта должен обрабатывать передачи.</span><span class="sxs-lookup"><span data-stu-id="feb57-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="feb57-111">В зависимости от типа получателя MAPI даже могут использовать более одного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="feb57-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="feb57-112">Если поставщик недоступен транспорта — единственный, который может обрабатывать получателя, передачи сообщений будет отложено до можно заново установить соединение с этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="feb57-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="feb57-113">Некоторые системы обмена сообщениями, безопасных систем; все потенциальные клиенты придется ввести набор допустимые учетные данные перед разрешением доступа.</span><span class="sxs-lookup"><span data-stu-id="feb57-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="feb57-114">MAPI не позволяет несанкционированного доступа для таких безопасных систем обмена сообщениями благодаря использованию поставщика транспорта проверки учетных данных во время входа в систему.</span><span class="sxs-lookup"><span data-stu-id="feb57-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

