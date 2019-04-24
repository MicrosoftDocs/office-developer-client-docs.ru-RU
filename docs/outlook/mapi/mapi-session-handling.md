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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328226"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="7940d-103">��������� ������ MAPI</span><span class="sxs-lookup"><span data-stu-id="7940d-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="7940d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7940d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7940d-105">Прежде чем вы сможете общаться с поставщиками услуг и базовой системой обмена сообщениями, необходимо установить сеанс.</span><span class="sxs-lookup"><span data-stu-id="7940d-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="7940d-106">Сеанс MAPI представляет собой ссылку от клиента к другим компонентам MAPI.</span><span class="sxs-lookup"><span data-stu-id="7940d-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="7940d-107">В результате успешного запуска сеанса MAPI возвращает на клиентские указатели на объект Session — объект, который реализует интерфейс **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="7940d-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="7940d-108">Дополнительные сведения см. в статье [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7940d-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="7940d-109">Вы можете использовать методы интерфейса **IMAPISession** для доступа к объектам адресной книги и поставщиков хранилищ сообщений, доступа к нескольким таблицам, формам отображения, настройкам свойств поставщика транспорта, а также для выполнения администрирования службы профилей и сообщений.</span><span class="sxs-lookup"><span data-stu-id="7940d-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="7940d-110">Содержание</span><span class="sxs-lookup"><span data-stu-id="7940d-110">In this section</span></span>

[<span data-ttu-id="7940d-111">Запуск сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="7940d-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="7940d-112">Описывается запуск сеанса MAPI и ссылки на разделы с более подробными сведениями.</span><span class="sxs-lookup"><span data-stu-id="7940d-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="7940d-113">Завершение сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="7940d-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="7940d-114">Описание завершения сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="7940d-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="7940d-115">Доступ к объектам с помощью сеанса</span><span class="sxs-lookup"><span data-stu-id="7940d-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="7940d-116">Сведения об использовании указателя сеансов для доступа к объектам Session.</span><span class="sxs-lookup"><span data-stu-id="7940d-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="7940d-117">Получение основного удостоверения и удостоверения поставщика</span><span class="sxs-lookup"><span data-stu-id="7940d-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="7940d-118">Описывает свойства, используемые для извлечения основного удостоверения и удостоверения поставщика.</span><span class="sxs-lookup"><span data-stu-id="7940d-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="7940d-119">Объекты "таблица состояния" и "состояние"</span><span class="sxs-lookup"><span data-stu-id="7940d-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="7940d-120">Сведения о том, как получить доступ к сведениям из таблицы "состояние".</span><span class="sxs-lookup"><span data-stu-id="7940d-120">Describes how to access information from the status table.</span></span>
    

