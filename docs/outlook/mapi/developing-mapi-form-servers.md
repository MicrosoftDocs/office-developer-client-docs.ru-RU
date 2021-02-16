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
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="f48bf-103">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="f48bf-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="f48bf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f48bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f48bf-105">В этом разделе описывается процесс создания исполняемых файлов сервера форм и файлов конфигурации форм для создания настраиваемых форм MAPI.</span><span class="sxs-lookup"><span data-stu-id="f48bf-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="f48bf-106">Прежде чем читать этот раздел, ознакомьтесь с информацией в [формах MAPI.](mapi-forms.md)</span><span class="sxs-lookup"><span data-stu-id="f48bf-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="f48bf-107">Разработка сервера форм включает следующие этапы:</span><span class="sxs-lookup"><span data-stu-id="f48bf-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="f48bf-108">Выбор сведений, которые будут содержаться в форме, и выбор набора свойств для их размещения.</span><span class="sxs-lookup"><span data-stu-id="f48bf-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="f48bf-109">Дополнительные сведения [см. в выборе набора свойств формы.](choosing-a-form-s-property-set.md)</span><span class="sxs-lookup"><span data-stu-id="f48bf-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="f48bf-110">Проектирование пользовательского интерфейса, с которым пользователи могут взаимодействовать со свойствами формы.</span><span class="sxs-lookup"><span data-stu-id="f48bf-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="f48bf-111">Выбор класса сообщения и создание уникального идентификатора класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="f48bf-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="f48bf-112">Обзор классов сообщений см. в сведениях [о классах сообщений MAPI.](mapi-message-classes.md)</span><span class="sxs-lookup"><span data-stu-id="f48bf-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="f48bf-113">Дополнительные сведения о классах и формах сообщений см. в [подклассе "Выбор класса сообщений".](choosing-a-message-class.md)</span><span class="sxs-lookup"><span data-stu-id="f48bf-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="f48bf-114">Реализация необходимых интерфейсов форм MAPI, а также дополнительных интерфейсов, необходимых конкретному серверу форм.</span><span class="sxs-lookup"><span data-stu-id="f48bf-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="f48bf-115">Дополнительные сведения см. в [записи кода сервера форм.](writing-form-server-code.md)</span><span class="sxs-lookup"><span data-stu-id="f48bf-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="f48bf-116">Написание кода пользовательского интерфейса для обработки взаимодействия пользователя с объектом формы и свойствами, которые использует форма.</span><span class="sxs-lookup"><span data-stu-id="f48bf-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="f48bf-117">Создание файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="f48bf-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="f48bf-118">Дополнительные сведения [см. в формате файлов конфигурации форм.](file-format-of-form-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="f48bf-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="f48bf-119">Установка формы на компьютерах пользователей.</span><span class="sxs-lookup"><span data-stu-id="f48bf-119">Installing the form on users' computers.</span></span> <span data-ttu-id="f48bf-120">Дополнительные сведения см. [в установке формы в библиотеку.](installing-a-form-into-a-library.md)</span><span class="sxs-lookup"><span data-stu-id="f48bf-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="f48bf-121">Скорее всего, вы будете выполнять шаги с 1 по 5 одновременно, а не последовательно.</span><span class="sxs-lookup"><span data-stu-id="f48bf-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="f48bf-122">Процесс разработки сервера форм, как и многих проектов программирования, не является процессом, в котором имеется особенно четко определяемая последовательность.</span><span class="sxs-lookup"><span data-stu-id="f48bf-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="f48bf-123">Например, создание файла конфигурации формы отображается как шаг от второго до последнего выше, но, вероятно, файл конфигурации формы будет создаваться постепенно, и он станет более полным по мере добавления компонентов на сервер форм.</span><span class="sxs-lookup"><span data-stu-id="f48bf-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f48bf-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f48bf-124">See also</span></span>



[<span data-ttu-id="f48bf-125">Понятия MAPI</span><span class="sxs-lookup"><span data-stu-id="f48bf-125">MAPI Concepts</span></span>](mapi-concepts.md)

