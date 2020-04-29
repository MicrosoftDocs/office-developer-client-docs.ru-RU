---
title: Интеграция кода сервера форм MAPI с кодом Windows
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
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="bcde4-103">Интеграция кода сервера форм MAPI с кодом Windows</span><span class="sxs-lookup"><span data-stu-id="bcde4-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="bcde4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcde4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcde4-105">Вспомним, что сервер формы является приложением Win32.</span><span class="sxs-lookup"><span data-stu-id="bcde4-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="bcde4-106">Таким образом, существует ряд задач, связанных с загрузкой сервера форм в память и выходом из чистого режима.</span><span class="sxs-lookup"><span data-stu-id="bcde4-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="bcde4-107">Как и для всех приложений Windows, точка входа для сервера формы является функцией **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="bcde4-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="bcde4-108">Эта функция является соответствующим местом для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="bcde4-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="bcde4-109">Создание и регистрация класса окна, чтобы сервер форм мог взаимодействовать с другими компонентами OLE.</span><span class="sxs-lookup"><span data-stu-id="bcde4-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="bcde4-110">Создание и регистрация класса или классов окна для пользовательских интерфейсов объектов формы.</span><span class="sxs-lookup"><span data-stu-id="bcde4-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="bcde4-111">Вызов функции [мапиинитиализе](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="bcde4-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="bcde4-112">Кроме того, **мапиинитиализе** обрабатывает необходимую инициализацию OLE.</span><span class="sxs-lookup"><span data-stu-id="bcde4-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="bcde4-113">Это необходимо сделать один раз для каждого экземпляра сервера форм.</span><span class="sxs-lookup"><span data-stu-id="bcde4-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="bcde4-114">Регистрация глобального атома с строковым представлением идентификатора класса сервера форм (CLSID).</span><span class="sxs-lookup"><span data-stu-id="bcde4-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="bcde4-115">Этот атом должен существовать в течение всего времени существования сервера форм.</span><span class="sxs-lookup"><span data-stu-id="bcde4-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="bcde4-116">Вызов функции OLE [корегистерклассобжект](https://msdn.microsoft.com/library/ms693407.aspx) для регистрации фабрики классов сервера форм с помощью OLE.</span><span class="sxs-lookup"><span data-stu-id="bcde4-116">Calling the OLE function [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="bcde4-117">Создание основного окна для получения сообщений.</span><span class="sxs-lookup"><span data-stu-id="bcde4-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="bcde4-118">Это окно, вероятно, не обязательно должно быть видимым, так как пользователь будет взаимодействовать с определенными окнами, связанными с отдельными объектами формы.</span><span class="sxs-lookup"><span data-stu-id="bcde4-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="bcde4-119">Однако во время разработки главное окно может быть удобным для отладки выходных данных или управления сервером формы.</span><span class="sxs-lookup"><span data-stu-id="bcde4-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="bcde4-120">Создание цикла обработки сообщений, выполняемого в течение всего времени существования сервера форм, перевод и отправка сообщений Windows в активные объекты формы.</span><span class="sxs-lookup"><span data-stu-id="bcde4-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="bcde4-121">При завершении работы сервера форм необходимо выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="bcde4-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="bcde4-122">Вызовите функцию [КОРЕВОКЕКЛАССОБЖЕКТ](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) OLE, чтобы отозвать регистрацию OLE своего класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="bcde4-122">Call the OLE function [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="bcde4-123">Вызов **мапиунинитиализе** для правильного закрытия подключения сервера форм к MAPI.</span><span class="sxs-lookup"><span data-stu-id="bcde4-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="bcde4-124">Удалите глобальный атом, содержащий строковое представление идентификатора класса.</span><span class="sxs-lookup"><span data-stu-id="bcde4-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcde4-125">См. также</span><span class="sxs-lookup"><span data-stu-id="bcde4-125">See also</span></span>



[<span data-ttu-id="bcde4-126">Написание кода на сервере формы</span><span class="sxs-lookup"><span data-stu-id="bcde4-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

