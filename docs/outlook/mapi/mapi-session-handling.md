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
ms.openlocfilehash: cdf3052175870287ff1a66d3745e90f8b8fff256
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809833"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="8cff1-103">��������� ������ MAPI</span><span class="sxs-lookup"><span data-stu-id="8cff1-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="8cff1-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8cff1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8cff1-105">Прежде чем можно общаться с поставщиками услуг и системы обмена сообщениями, необходимо установить сеанс.</span><span class="sxs-lookup"><span data-stu-id="8cff1-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="8cff1-106">Сеанс MAPI — это ссылка из клиента на другие компоненты MAPI.</span><span class="sxs-lookup"><span data-stu-id="8cff1-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="8cff1-107">В результате успешного запуска сеанса MAPI возвращает клиентам указатель на объект сеанса — это объект, реализующий интерфейс **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="8cff1-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="8cff1-108">Дополнительные сведения можно [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="8cff1-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="8cff1-109">Можно использовать методы интерфейса **IMAPISession** доступа к объектам поставщиков хранилища адресной книги и сообщения, доступ к несколько таблиц, отображение форм, свойства поставщика транспорта и выполнять администрирование службы профилей и сообщения.</span><span class="sxs-lookup"><span data-stu-id="8cff1-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="8cff1-110">В этой статье</span><span class="sxs-lookup"><span data-stu-id="8cff1-110">In this section</span></span>

[<span data-ttu-id="8cff1-111">Запуск сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="8cff1-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="8cff1-112">Описывается, как начать сеанс MAPI и содержит ссылки на разделы с более подробными сведениями.</span><span class="sxs-lookup"><span data-stu-id="8cff1-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="8cff1-113">Завершение сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="8cff1-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="8cff1-114">Описывается, как завершить сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="8cff1-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="8cff1-115">Доступ к объектам с помощью сеанса</span><span class="sxs-lookup"><span data-stu-id="8cff1-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="8cff1-116">Описывается, как использовать указатель сеанса для доступа к объектам сеанса.</span><span class="sxs-lookup"><span data-stu-id="8cff1-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="8cff1-117">Получение удостоверения поставщика и основного удостоверения</span><span class="sxs-lookup"><span data-stu-id="8cff1-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="8cff1-118">Описываются свойства, используемые для получения основной и поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="8cff1-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="8cff1-119">Таблица и объекты состояний</span><span class="sxs-lookup"><span data-stu-id="8cff1-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="8cff1-120">Описывается, как получить доступ к информации из таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="8cff1-120">Describes how to access information from the status table.</span></span>
    

