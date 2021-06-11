---
title: Интеграция кода форм-сервера MAPI с Windows кодом
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332181"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="bafda-103">Интеграция кода форм-сервера MAPI с Windows кодом</span><span class="sxs-lookup"><span data-stu-id="bafda-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="bafda-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bafda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bafda-105">Помните, что сервер формы — это приложение Win32.</span><span class="sxs-lookup"><span data-stu-id="bafda-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="bafda-106">Таким образом, существует ряд задач, связанных с загрузкой сервера форм в память и чистой очисткой.</span><span class="sxs-lookup"><span data-stu-id="bafda-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="bafda-107">Как и Windows приложения, точкой входа для сервера форм является **функция WinMain.**</span><span class="sxs-lookup"><span data-stu-id="bafda-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="bafda-108">Эта функция является подходящим местом для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="bafda-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="bafda-109">Создание и регистрация класса окна, чтобы ваш сервер формы взаимодействовал с другими компонентами OLE.</span><span class="sxs-lookup"><span data-stu-id="bafda-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="bafda-110">Создание и регистрация класса окна или классов для пользовательских интерфейсов объектов формы.</span><span class="sxs-lookup"><span data-stu-id="bafda-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="bafda-111">Вызов [функции MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="bafda-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="bafda-112">**MAPIInitialize** также обрабатывает требуемую инициализацию OLE.</span><span class="sxs-lookup"><span data-stu-id="bafda-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="bafda-113">Это должно быть сделано один раз в экземпляре сервера форм.</span><span class="sxs-lookup"><span data-stu-id="bafda-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="bafda-114">Регистрация глобального атома с помощью строки представления идентификатора класса сервера форм (CLSID).</span><span class="sxs-lookup"><span data-stu-id="bafda-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="bafda-115">Этот атом должен существовать в течение всего срока службы сервера форм.</span><span class="sxs-lookup"><span data-stu-id="bafda-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="bafda-116">Вызов функции OLE [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) для регистрации фабрики классов вашего сервера форм с помощью OLE.</span><span class="sxs-lookup"><span data-stu-id="bafda-116">Calling the OLE function [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="bafda-117">Создание основного окна для получения сообщений.</span><span class="sxs-lookup"><span data-stu-id="bafda-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="bafda-118">Возможно, это окно не должно быть видимым, так как пользователь будет взаимодействовать с определенными окнами, связанными с отдельными объектами формы.</span><span class="sxs-lookup"><span data-stu-id="bafda-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="bafda-119">Однако во время разработки главное окно может быть удобным местом для отладки выходных данных или управления сервером форм.</span><span class="sxs-lookup"><span data-stu-id="bafda-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="bafda-120">Создание цикла сообщений, который выполняется в течение всего срока службы сервера форм, перевод и отправка windows-сообщений на объекты активной формы.</span><span class="sxs-lookup"><span data-stu-id="bafda-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="bafda-121">Когда сервер формы выходит, он должен выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="bafda-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="bafda-122">Вызов функции OLE [CoRevokeClassObject,](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) чтобы отозвать регистрацию OLE класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="bafda-122">Call the OLE function [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="bafda-123">Вызов **MAPIUninitialize,** чтобы правильно закрыть подключение сервера форм к MAPI.</span><span class="sxs-lookup"><span data-stu-id="bafda-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="bafda-124">Удалите глобальный атом, содержащий строковую репрезентативность идентификатора класса.</span><span class="sxs-lookup"><span data-stu-id="bafda-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bafda-125">См. также</span><span class="sxs-lookup"><span data-stu-id="bafda-125">See also</span></span>



[<span data-ttu-id="bafda-126">Написание кода сервера форм</span><span class="sxs-lookup"><span data-stu-id="bafda-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

