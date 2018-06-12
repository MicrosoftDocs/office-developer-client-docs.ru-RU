---
title: Диспетчер формы MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: d12d879ea5a82c5e0e3978d90694b3851aaac5cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809737"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="2c022-103">Диспетчер формы MAPI</span><span class="sxs-lookup"><span data-stu-id="2c022-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="2c022-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c022-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c022-105">Диспетчер форм — это объект, реализующий интерфейс [IMAPIFormMgr](imapiformmgriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="2c022-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="2c022-106">Большинство организаций будет использовать диспетчер форм, поставляемых вместе с MAPI, называется Диспетчер форм по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c022-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="2c022-107">Тем не менее организации можно заменить диспетчер форм по умолчанию диспетчер настраиваемой формы при желании.</span><span class="sxs-lookup"><span data-stu-id="2c022-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="2c022-108">Диспетчер форм отвечает за размещение форм в рамках библиотеки форм, загрузке формы в ответ на запросы пользователей и установке форм в библиотеки форм локального пользователя, библиотека форм папки или Библиотека личных форм.</span><span class="sxs-lookup"><span data-stu-id="2c022-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="2c022-109">Пользователь может взаимодействовать с сообщением экземпляр сервера форм для класса сообщений сообщения должны созданы и активированы для отображения сообщения и выполнить запрошенную операцию в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="2c022-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="2c022-110">Как описано в разделе [Библиотеки форм MAPI](mapi-form-libraries.md), реализации формы могут существовать в различных местах (библиотеки форм) и не гарантируется, что формы или его сервер будут доступны локально или в текущее состояние, если пользователю для взаимодействия с ним.</span><span class="sxs-lookup"><span data-stu-id="2c022-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="2c022-111">Диспетчер форм отвечает за сведения о размещение и активация формы.</span><span class="sxs-lookup"><span data-stu-id="2c022-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="2c022-112">Клиенты используют службы, предоставляемые диспетчер форм для поиска и активация форм.</span><span class="sxs-lookup"><span data-stu-id="2c022-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="2c022-113">Интерфейс **IMAPIFormMgr** реализуется диспетчер форм и вызывается клиентами для доступа к его службам.</span><span class="sxs-lookup"><span data-stu-id="2c022-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="2c022-114">Диспетчер форм является основным компонентом, так как он скрывает почти все сведения о поиске и активация форм из сообщений (en).</span><span class="sxs-lookup"><span data-stu-id="2c022-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="2c022-115">При загрузке формы серверы, диспетчер форм по умолчанию загружает форму из первой библиотеки форм, в которой находится реализация класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="2c022-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="2c022-116">Диспетчер форм по умолчанию выполняет поиск библиотек форм в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="2c022-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="2c022-117">Библиотека форм локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c022-117">The user's local form library.</span></span> <span data-ttu-id="2c022-118">Эта библиотека форм поиск сначала, поскольку обеспечивает быстрый доступ к реализации формы, если реализация устанавливается из локальной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="2c022-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="2c022-119">Библиотека форм папки контейнера сообщение — папка, в которой хранятся сообщения, загрузка.</span><span class="sxs-lookup"><span data-stu-id="2c022-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="2c022-120">Библиотека личных форм пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c022-120">The user's personal form library.</span></span>
    
<span data-ttu-id="2c022-121">Диспетчер настраиваемой формы можно найти библиотеки форм доступен в любом порядке, или можно реализовать другие библиотеки форм, таких как библиотеки форм всей организации.</span><span class="sxs-lookup"><span data-stu-id="2c022-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="2c022-122">Для получения дополнительных сведений о библиотеки форм см. [Библиотеки форм MAPI](mapi-form-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="2c022-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c022-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2c022-123">See also</span></span>



[<span data-ttu-id="2c022-124">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="2c022-124">MAPI Forms</span></span>](mapi-forms.md)

