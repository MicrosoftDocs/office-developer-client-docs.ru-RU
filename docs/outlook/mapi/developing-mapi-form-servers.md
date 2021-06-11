---
title: Разработка серверов форм MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420768"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="e1709-103">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="e1709-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="e1709-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1709-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1709-105">В этом разделе описывается процесс создания файлов конфигурации форм-сервера и конфигурации форм для создания настраиваемых форм MAPI.</span><span class="sxs-lookup"><span data-stu-id="e1709-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="e1709-106">Перед чтением этого раздела необходимо ознакомиться с информацией в [mapi Forms.](mapi-forms.md)</span><span class="sxs-lookup"><span data-stu-id="e1709-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="e1709-107">Разработка сервера форм включает в себя следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e1709-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="e1709-108">Определение сведений, содержащихся в форме, и выбор набора свойств для удержания этих сведений.</span><span class="sxs-lookup"><span data-stu-id="e1709-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="e1709-109">Дополнительные сведения см. в подборе набора [свойств формы.](choosing-a-form-s-property-set.md)</span><span class="sxs-lookup"><span data-stu-id="e1709-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="e1709-110">Разработка пользовательского интерфейса, с помощью которого пользователи могут взаимодействовать со свойствами формы.</span><span class="sxs-lookup"><span data-stu-id="e1709-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="e1709-111">Выбор класса сообщений и создание уникального идентификатора класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="e1709-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="e1709-112">Обзор классов сообщений см. в [примере MAPI Message Classes.](mapi-message-classes.md)</span><span class="sxs-lookup"><span data-stu-id="e1709-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="e1709-113">Дополнительные сведения о классах и формах сообщений см. в [подборе класса сообщений.](choosing-a-message-class.md)</span><span class="sxs-lookup"><span data-stu-id="e1709-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="e1709-114">Реализация необходимых интерфейсов форм MAPI, а также любых необязательных интерфейсов, необходимых вашему определенному серверу форм.</span><span class="sxs-lookup"><span data-stu-id="e1709-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="e1709-115">Дополнительные сведения см. в [статьи Writing Form Server Code](writing-form-server-code.md).</span><span class="sxs-lookup"><span data-stu-id="e1709-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="e1709-116">Написание кода пользовательского интерфейса для обработки взаимодействия пользователя с объектом формы и свойствами, которые использует форма.</span><span class="sxs-lookup"><span data-stu-id="e1709-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="e1709-117">Создание файла конфигурации формы для формы.</span><span class="sxs-lookup"><span data-stu-id="e1709-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="e1709-118">Дополнительные сведения см. в [файловом формате файлов конфигурации форм.](file-format-of-form-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="e1709-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="e1709-119">Установка формы на компьютерах пользователей.</span><span class="sxs-lookup"><span data-stu-id="e1709-119">Installing the form on users' computers.</span></span> <span data-ttu-id="e1709-120">Дополнительные сведения см. [в дополнительных сведениях об](installing-a-form-into-a-library.md)установке формы в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="e1709-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="e1709-121">Скорее всего, вы будете выполнять шаги от 1 до 5 одновременно, а не завершать их последовательно.</span><span class="sxs-lookup"><span data-stu-id="e1709-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="e1709-122">Процесс разработки сервера форм, как и многих проектов программирования, не имеет определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="e1709-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="e1709-123">Например, создание файла конфигурации формы показано в качестве второго по последнему шагу выше, но вы, вероятно, будете создавать файл конфигурации формы постепенно, и он станет более полным по мере добавления функций на сервер формы.</span><span class="sxs-lookup"><span data-stu-id="e1709-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1709-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e1709-124">See also</span></span>



[<span data-ttu-id="e1709-125">Понятия MAPI</span><span class="sxs-lookup"><span data-stu-id="e1709-125">MAPI Concepts</span></span>](mapi-concepts.md)

