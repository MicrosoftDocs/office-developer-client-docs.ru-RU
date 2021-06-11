---
title: Поставщик транспорта и операционная модель MAPI Spooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426627"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="8d0a3-103">Поставщик транспорта и операционная модель MAPI Spooler</span><span class="sxs-lookup"><span data-stu-id="8d0a3-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="8d0a3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d0a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d0a3-105">Инициализация, запуск, обработка, отключение и деинитиализация поставщика транспорта выполняются серией вызовов от пулера MAPI к поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="8d0a3-106">Вызовы последовательно следуют следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8d0a3-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="8d0a3-107">Spooler MAPI вызывает [функцию XPProviderInit,](xpproviderinit.md) передает объект поддержки, получает объект поставщика и проверяет, что поставщик транспорта и spooler MAPI поддерживают совместимый диапазон номеров версий MAPI.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="8d0a3-108">Spooler MAPI вызывает [метод IXPProvider::TransportLogon](ixpprovider-transportlogon.md) [интерфейса IXPProvider: IUnknown.](ixpprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="8d0a3-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="8d0a3-109">Сеанс устанавливается между пулером MAPI и поставщиком транспорта с учетными данными в текущем разделе профиля.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="8d0a3-110">Поставщик транспорта возвращает объект logon.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="8d0a3-111">Шпалер MAPI вызывает [метод IXPLogon::AddressTypes.](ixplogon-addresstypes.md)</span><span class="sxs-lookup"><span data-stu-id="8d0a3-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="8d0a3-112">Поставщик транспорта возвращает список уникальных идентификаторов (UID) и типов адресов электронной почты, которые он примет.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="8d0a3-113">Поставщик транспорта вызывает [метод IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) для создания строки в таблице состояния MAPI.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="8d0a3-114">Spooler MAPI вызывает [метод IXPLogon::TransportNotify,](ixplogon-transportnotify.md) чтобы включить передачу и прием сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="8d0a3-115">Если поставщик транспорта запрашивает его в ответ на вызов **TransportLogon,** шпалер MAPI периодически вызывает [метод IXPLogon::Idle.](ixplogon-idle.md)</span><span class="sxs-lookup"><span data-stu-id="8d0a3-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="8d0a3-116">Простая обработка полезна, если поставщику транспорта необходимо оповещение системы обмена сообщениями для новых сообщений или выполнение других задач с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="8d0a3-117">Spooler MAPI и поставщик транспорта отправляют и получают сообщения.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="8d0a3-118">Дополнительные сведения см. в [примере модели отправки сообщений и](message-submission-model.md) [модели приема сообщений.](message-reception-model.md)</span><span class="sxs-lookup"><span data-stu-id="8d0a3-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="8d0a3-119">Пулер MAPI передает запросы и звонки на объекты поддержки, сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="8d0a3-120">Spooler MAPI вызывает метод **TransportNotify,** чтобы отключить передачу и прием сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="8d0a3-121">Spooler MAPI выпускает объекты logon и provider.</span><span class="sxs-lookup"><span data-stu-id="8d0a3-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="8d0a3-122">Дополнительные сведения см. в [методе IXPProvider::Shutdown.](ixpprovider-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="8d0a3-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

