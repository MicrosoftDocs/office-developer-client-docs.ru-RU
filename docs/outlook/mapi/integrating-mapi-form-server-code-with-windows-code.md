---
title: Интеграция серверного кода форм MAPI с кодом Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 31f09b1c2f7b23d63e17f59c28b7bcf377b769d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809445"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="265f2-103">Интеграция серверного кода форм MAPI с кодом Windows</span><span class="sxs-lookup"><span data-stu-id="265f2-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="265f2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="265f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="265f2-105">Помните, что сервер формы — это приложение Win32.</span><span class="sxs-lookup"><span data-stu-id="265f2-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="265f2-106">Таким образом существуют некоторые задачи, связанные с загрузки сервера формы в памяти и завершение работы приложения без ошибок.</span><span class="sxs-lookup"><span data-stu-id="265f2-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="265f2-107">Как и все приложения Windows точка входа для сервера формы является функции **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="265f2-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="265f2-108">Эта функция является соответствующее место для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="265f2-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="265f2-109">Создание и регистрация класса окна, чтобы сервер форм могут взаимодействовать с другими компонентами OLE.</span><span class="sxs-lookup"><span data-stu-id="265f2-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="265f2-110">Создание и регистрация класса окна или классы для пользовательских интерфейсов объектам формы.</span><span class="sxs-lookup"><span data-stu-id="265f2-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="265f2-111">Вызов функции [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="265f2-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="265f2-112">**MAPIInitialize** обрабатывает необходимые OLE инициализации, а также.</span><span class="sxs-lookup"><span data-stu-id="265f2-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="265f2-113">Это необходимо выполнить один раз на каждый экземпляр сервера формы.</span><span class="sxs-lookup"><span data-stu-id="265f2-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="265f2-114">Регистрация глобального atom с строковое представление формы server идентификатор класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="265f2-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="265f2-115">В этом atom должна существовать для жизненным циклом сервера форм.</span><span class="sxs-lookup"><span data-stu-id="265f2-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="265f2-116">Вызов функции OLE [CoRegisterClassObject](http://msdn.microsoft.com/en-us/library/ms693407.aspx) для регистрации фабрики классов сервера форм с OLE.</span><span class="sxs-lookup"><span data-stu-id="265f2-116">Calling the OLE function [CoRegisterClassObject](http://msdn.microsoft.com/en-us/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="265f2-117">Создание главного окна для получения сообщений.</span><span class="sxs-lookup"><span data-stu-id="265f2-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="265f2-118">Это окно, вероятно, не нужно быть видны, так как пользователь будет взаимодействует с определенным windows, связанные с объектами объединяемой формы.</span><span class="sxs-lookup"><span data-stu-id="265f2-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="265f2-119">Тем не менее во время разработки, главного окна может быть удобно для отладки элемента управления сервера формы или вывода.</span><span class="sxs-lookup"><span data-stu-id="265f2-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="265f2-120">Создание цикл обработки сообщений, на котором выполняется в течение времени жизни сервера формы, преобразования и отправки сообщений windows для активной формы объектов.</span><span class="sxs-lookup"><span data-stu-id="265f2-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="265f2-121">При выходе из сервера формы, его следует выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="265f2-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="265f2-122">Вызовите функцию OLE [CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx) для отмены регистрации OLE класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="265f2-122">Call the OLE function [CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="265f2-123">Вызовите **MAPIUninitialize** , чтобы должным образом закрыть подключения к серверу формы к MAPI.</span><span class="sxs-lookup"><span data-stu-id="265f2-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="265f2-124">Удаление глобального atom, содержащий строковое представление идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="265f2-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="265f2-125">См. также</span><span class="sxs-lookup"><span data-stu-id="265f2-125">See also</span></span>



[<span data-ttu-id="265f2-126">Написание серверного кода формы</span><span class="sxs-lookup"><span data-stu-id="265f2-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

