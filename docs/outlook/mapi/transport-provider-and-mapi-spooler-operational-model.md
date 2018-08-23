---
title: Поставщик транспорта и операционная модель системы буферизации MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 26d9982248fde015a584eb79cc248bafc5afc6bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594035"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="d0f7f-103">Поставщик транспорта и операционная модель системы буферизации MAPI</span><span class="sxs-lookup"><span data-stu-id="d0f7f-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="d0f7f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0f7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0f7f-105">Инициализация поставщика транспорта, загрузки, обработки, завершение работы и deinitialization выполняются посредством ряда вызовов из очереди MAPI поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="d0f7f-106">Вызовы упорядочены следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d0f7f-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="d0f7f-107">Диспетчер очереди MAPI вызывает функцию [XPProviderInit](xpproviderinit.md) , передает объект поддержки, возвращает объект поставщика и проверяет, что поставщик транспорта и диспетчер очереди MAPI поддерживают номера версий совместимые диапазон MAPI.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="d0f7f-108">Диспетчер очереди MAPI вызывает метод [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) [IXPProvider: IUnknown](ixpprovideriunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="d0f7f-109">Установить сеанс связи между диспетчер очереди MAPI и поставщика транспорта с использованием учетных данных в разделе текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="d0f7f-110">Поставщика транспорта возвращает объект входа в систему.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="d0f7f-111">Диспетчер очереди MAPI вызывает метод [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="d0f7f-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="d0f7f-112">Поставщика транспорта возвращает список уникальных идентификаторов (UID) и типов адресов электронной почты, который будет принимать.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="d0f7f-113">Поставщика транспорта вызывает метод [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) , чтобы создать его строку в таблице состояния MAPI.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="d0f7f-114">Диспетчер очереди MAPI вызывает метод [IXPLogon::TransportNotify](ixplogon-transportnotify.md) для включения передачи сообщений и прием.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="d0f7f-115">По запросу поставщика транспорта возврата для вызова **TransportLogon** , диспетчер очереди MAPI периодически вызывает метод [IXPLogon::Idle](ixplogon-idle.md) .</span><span class="sxs-lookup"><span data-stu-id="d0f7f-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="d0f7f-116">Обработки бездействия полезна, если требуется, чтобы опроса системы обмена сообщениями для новых сообщений или выполнять другие задачи низким приоритетом поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="d0f7f-117">Диспетчер очереди MAPI и поставщика транспорта отправлять и получать сообщения.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="d0f7f-118">Для получения дополнительных сведений см [Модель отправки сообщений](message-submission-model.md) и [Модели приема сообщений](message-reception-model.md).</span><span class="sxs-lookup"><span data-stu-id="d0f7f-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="d0f7f-119">Диспетчер очереди MAPI включают следующие транспорта и вызывает на объекты поддержки, сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="d0f7f-120">Диспетчер очереди MAPI вызывает метод **TransportNotify** для отключения передачи сообщений и приема.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="d0f7f-121">Диспетчер очереди MAPI высвобождение объектов входа в систему и поставщика.</span><span class="sxs-lookup"><span data-stu-id="d0f7f-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="d0f7f-122">Для получения дополнительных сведений см [IXPProvider::Shutdown](ixpprovider-shutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="d0f7f-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

