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
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="f9810-103">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="f9810-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="f9810-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9810-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9810-105">В этом разделе описывается процесс создания файлов конфигурации исполняемых файлов и форм сервера форм для создания настраиваемых форм MAPI.</span><span class="sxs-lookup"><span data-stu-id="f9810-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="f9810-106">Перед прочтением этого раздела необходимо ознакомиться со сведениями в [формах MAPI](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="f9810-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="f9810-107">Разработка сервера форм состоит из следующих этапов:</span><span class="sxs-lookup"><span data-stu-id="f9810-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="f9810-108">Выбор сведений, которые будут храниться в форме, и выбор набора свойств для хранения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="f9810-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="f9810-109">Дополнительную информацию можно узнать [в статье Выбор набора свойств формы](choosing-a-form-s-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="f9810-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="f9810-110">Разработка пользовательского интерфейса, с помощью которого пользователи могут взаимодействовать со свойствами формы.</span><span class="sxs-lookup"><span data-stu-id="f9810-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="f9810-111">Выбор класса сообщения и создание уникального идентификатора класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="f9810-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="f9810-112">Общие сведения о классах сообщений содержатся в разделе [классы сообщений MAPI](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="f9810-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="f9810-113">Дополнительные сведения о классах сообщений и формах приведены [в разделе Выбор класса сообщений](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="f9810-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="f9810-114">Реализация обязательных интерфейсов форм MAPI, а также любых необязательных интерфейсов, необходимых для конкретного сервера форм.</span><span class="sxs-lookup"><span data-stu-id="f9810-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="f9810-115">Дополнительную информацию можно узнать в статье [Создание серверного кода формы](writing-form-server-code.md).</span><span class="sxs-lookup"><span data-stu-id="f9810-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="f9810-116">Написание кода пользовательского интерфейса для обработки взаимодействия пользователя с объектом Form и свойств, которые использует форма.</span><span class="sxs-lookup"><span data-stu-id="f9810-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="f9810-117">Создание файла конфигурации формы для формы.</span><span class="sxs-lookup"><span data-stu-id="f9810-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="f9810-118">Дополнительные сведения см. в разделе [Формат файлов конфигурации форм](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="f9810-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="f9810-119">Установка формы на компьютерах пользователей.</span><span class="sxs-lookup"><span data-stu-id="f9810-119">Installing the form on users' computers.</span></span> <span data-ttu-id="f9810-120">Дополнительную информацию можно узнать [в статье Установка формы в библиотеку](installing-a-form-into-a-library.md).</span><span class="sxs-lookup"><span data-stu-id="f9810-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="f9810-121">Действия 1 – 5, скорее всего, будут выполняться одновременно, а не последовательно.</span><span class="sxs-lookup"><span data-stu-id="f9810-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="f9810-122">Процесс разработки сервера форм, как и во многих проектах программирования, не является таковым, в котором есть определенная строго определенная последовательность.</span><span class="sxs-lookup"><span data-stu-id="f9810-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="f9810-123">Например, при создании файла конфигурации формы, как описано выше, необходимо создать файл конфигурации формы, который будет более полным при добавлении компонентов на сервер форм, но это будет более полным.</span><span class="sxs-lookup"><span data-stu-id="f9810-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9810-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f9810-124">See also</span></span>



[<span data-ttu-id="f9810-125">Понятия MAPI</span><span class="sxs-lookup"><span data-stu-id="f9810-125">MAPI Concepts</span></span>](mapi-concepts.md)

