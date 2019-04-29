---
title: Модель поставщика транспорта и очереди печати MAPI
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
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="104a9-103">Модель поставщика транспорта и очереди печати MAPI</span><span class="sxs-lookup"><span data-stu-id="104a9-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="104a9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="104a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="104a9-105">Инициализация, запуск, обработка, завершение работы и деинициализация поставщика транспорта выполняются с помощью ряда вызовов от диспетчера очереди MAPI к поставщику транспорта.</span><span class="sxs-lookup"><span data-stu-id="104a9-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="104a9-106">Звонки упорядочены следующим образом:</span><span class="sxs-lookup"><span data-stu-id="104a9-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="104a9-107">Диспетчер очереди MAPI вызывает функцию [ксппровидеринит](xpproviderinit.md) , передает объект поддержки, получает объект поставщика и проверяет, поддерживает ли поставщик транспорта и Диспетчер очереди MAPI совместимый диапазон номеров версий MAPI.</span><span class="sxs-lookup"><span data-stu-id="104a9-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="104a9-108">Диспетчер очереди MAPI вызывает метод [иксппровидер:: транспортлогон](ixpprovider-transportlogon.md) интерфейса [иксппровидер: IUnknown](ixpprovideriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="104a9-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="104a9-109">Между диспетчером очереди MAPI и поставщиком транспорта устанавливается сеанс с учетными данными из текущего раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="104a9-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="104a9-110">Поставщик транспорта возвращает объект logon.</span><span class="sxs-lookup"><span data-stu-id="104a9-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="104a9-111">Диспетчер очереди MAPI вызывает метод [иксплогон:: аддресстипес](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="104a9-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="104a9-112">Поставщик транспорта возвращает список уникальных идентификаторов (UID) и типов электронных адресов, которые он будет принимать.</span><span class="sxs-lookup"><span data-stu-id="104a9-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="104a9-113">Поставщик транспорта вызывает метод [имаписуппорт:: модифистатусров](imapisupport-modifystatusrow.md) для создания строки в таблице состояния MAPI.</span><span class="sxs-lookup"><span data-stu-id="104a9-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="104a9-114">Диспетчер очереди MAPI вызывает метод [иксплогон:: транспортнотифи](ixplogon-transportnotify.md) для включения передачи и приема сообщений.</span><span class="sxs-lookup"><span data-stu-id="104a9-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="104a9-115">Если поставщик транспорта запрашивается в результате возврата для вызова **транспортлогон** , то диспетчер очереди MAPI периодически вызывает метод [Иксплогон:: Idle](ixplogon-idle.md) .</span><span class="sxs-lookup"><span data-stu-id="104a9-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="104a9-116">Обработка в режиме простоя полезна, если поставщик транспорта должен опросить базовую систему обмена сообщениями для новых сообщений или выполнить другие задачи с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="104a9-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="104a9-117">Диспетчер очереди MAPI и поставщик транспорта отправляют и получают сообщения.</span><span class="sxs-lookup"><span data-stu-id="104a9-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="104a9-118">Для получения дополнительных сведений см [модель отправки сообщений](message-submission-model.md) и [модель приема сообщений](message-reception-model.md).</span><span class="sxs-lookup"><span data-stu-id="104a9-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="104a9-119">Службы диспетчера очереди MAPI относят запросы и вызовы для объектов support, Message и вложения.</span><span class="sxs-lookup"><span data-stu-id="104a9-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="104a9-120">Диспетчер очереди MAPI вызывает метод **транспортнотифи** , чтобы отключить передачу и прием сообщений.</span><span class="sxs-lookup"><span data-stu-id="104a9-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="104a9-121">Диспетчер очереди MAPI освобождает объекты входа и поставщика.</span><span class="sxs-lookup"><span data-stu-id="104a9-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="104a9-122">Дополнительные сведения см. в методе [иксппровидер:: Shutdown](ixpprovider-shutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="104a9-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

