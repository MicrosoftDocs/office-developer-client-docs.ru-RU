---
title: ��������� ������ MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422063"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="9e642-103">��������� ������ MAPI</span><span class="sxs-lookup"><span data-stu-id="9e642-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="9e642-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e642-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e642-105">Прежде чем вы сможете общаться с поставщиками услуг и системой обмена сообщениями, необходимо установить сеанс.</span><span class="sxs-lookup"><span data-stu-id="9e642-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="9e642-106">Сеанс MAPI — это ссылка клиента на другие компоненты MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e642-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="9e642-107">В результате успешного запуска сеанса MAPI возвращает клиентам указатель на объект сеанса — объект, реализуя **интерфейс IMAPISession.**</span><span class="sxs-lookup"><span data-stu-id="9e642-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="9e642-108">Дополнительные сведения см. [в iMAPISession : IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="9e642-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="9e642-109">С помощью методов **интерфейса IMAPISession** можно получить доступ к объектам поставщиков адресной книги и магазина сообщений, получить доступ к нескольким таблицам, формам отображения, заказать свойства поставщика транспорта, а также выполнить администрирование службы профилей и сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e642-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="9e642-110">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="9e642-110">In this section</span></span>

[<span data-ttu-id="9e642-111">Запуск сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="9e642-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="9e642-112">Описывает, как начать сеанс MAPI и включает ссылки на разделы с более подробными сведениями.</span><span class="sxs-lookup"><span data-stu-id="9e642-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="9e642-113">Окончание сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="9e642-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="9e642-114">Описывает завершение сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e642-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="9e642-115">Доступ к объектам с помощью сеанса</span><span class="sxs-lookup"><span data-stu-id="9e642-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="9e642-116">Описывает, как использовать указатель сеанса для доступа к объектам сеанса.</span><span class="sxs-lookup"><span data-stu-id="9e642-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="9e642-117">Повторное иждивение удостоверения основного поставщика и поставщика</span><span class="sxs-lookup"><span data-stu-id="9e642-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="9e642-118">Описывает свойства, используемые для получения удостоверения основного поставщика и поставщика.</span><span class="sxs-lookup"><span data-stu-id="9e642-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="9e642-119">Объекты таблицы состояния и состояния</span><span class="sxs-lookup"><span data-stu-id="9e642-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="9e642-120">Описывает, как получить доступ к данным из таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="9e642-120">Describes how to access information from the status table.</span></span>
    

