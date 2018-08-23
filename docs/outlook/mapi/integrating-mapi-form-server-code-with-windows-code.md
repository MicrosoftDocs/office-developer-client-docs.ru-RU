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
ms.openlocfilehash: b37ae47e40906342aeecf179848311556a7d4ba4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573994"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="ff505-103">Интеграция серверного кода форм MAPI с кодом Windows</span><span class="sxs-lookup"><span data-stu-id="ff505-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="ff505-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff505-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff505-105">Помните, что сервер формы — это приложение Win32.</span><span class="sxs-lookup"><span data-stu-id="ff505-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="ff505-106">Таким образом существуют некоторые задачи, связанные с загрузки сервера формы в памяти и завершение работы приложения без ошибок.</span><span class="sxs-lookup"><span data-stu-id="ff505-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="ff505-107">Как и все приложения Windows точка входа для сервера формы является функции **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="ff505-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="ff505-108">Эта функция является соответствующее место для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="ff505-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="ff505-109">Создание и регистрация класса окна, чтобы сервер форм могут взаимодействовать с другими компонентами OLE.</span><span class="sxs-lookup"><span data-stu-id="ff505-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="ff505-110">Создание и регистрация класса окна или классы для пользовательских интерфейсов объектам формы.</span><span class="sxs-lookup"><span data-stu-id="ff505-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="ff505-111">Вызов функции [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="ff505-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="ff505-112">**MAPIInitialize** обрабатывает необходимые OLE инициализации, а также.</span><span class="sxs-lookup"><span data-stu-id="ff505-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="ff505-113">Это необходимо выполнить один раз на каждый экземпляр сервера формы.</span><span class="sxs-lookup"><span data-stu-id="ff505-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="ff505-114">Регистрация глобального atom с строковое представление формы server идентификатор класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="ff505-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="ff505-115">В этом atom должна существовать для жизненным циклом сервера форм.</span><span class="sxs-lookup"><span data-stu-id="ff505-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="ff505-116">Вызов функции OLE [CoRegisterClassObject](http://msdn.microsoft.com/en-us/library/ms693407.aspx) для регистрации фабрики классов сервера форм с OLE.</span><span class="sxs-lookup"><span data-stu-id="ff505-116">Calling the OLE function [CoRegisterClassObject](http://msdn.microsoft.com/en-us/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="ff505-117">Создание главного окна для получения сообщений.</span><span class="sxs-lookup"><span data-stu-id="ff505-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="ff505-118">Это окно, вероятно, не нужно быть видны, так как пользователь будет взаимодействует с определенным windows, связанные с объектами объединяемой формы.</span><span class="sxs-lookup"><span data-stu-id="ff505-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="ff505-119">Тем не менее во время разработки, главного окна может быть удобно для отладки элемента управления сервера формы или вывода.</span><span class="sxs-lookup"><span data-stu-id="ff505-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="ff505-120">Создание цикл обработки сообщений, на котором выполняется в течение времени жизни сервера формы, преобразования и отправки сообщений windows для активной формы объектов.</span><span class="sxs-lookup"><span data-stu-id="ff505-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="ff505-121">При выходе из сервера формы, его следует выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="ff505-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="ff505-122">Вызовите функцию OLE [CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx) для отмены регистрации OLE класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="ff505-122">Call the OLE function [CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="ff505-123">Вызовите **MAPIUninitialize** , чтобы должным образом закрыть подключения к серверу формы к MAPI.</span><span class="sxs-lookup"><span data-stu-id="ff505-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="ff505-124">Удаление глобального atom, содержащий строковое представление идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="ff505-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff505-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ff505-125">See also</span></span>



[<span data-ttu-id="ff505-126">Написание серверного кода формы</span><span class="sxs-lookup"><span data-stu-id="ff505-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

