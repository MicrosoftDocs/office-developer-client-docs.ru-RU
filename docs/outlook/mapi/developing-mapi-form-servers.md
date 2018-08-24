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
ms.openlocfilehash: d55134cf5181ebbba0108c228d9afc3a494e75ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576241"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="df6ac-103">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="df6ac-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="df6ac-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df6ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df6ac-105">В этом разделе описывается процесс создания исполняемый файл сервера форм и файлах конфигурации формы для создания пользовательских форм MAPI.</span><span class="sxs-lookup"><span data-stu-id="df6ac-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="df6ac-106">Прежде чем читать этот раздел, следует ознакомиться со сведениями в [Формах MAPI](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="df6ac-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="df6ac-107">Разработка формы server состоит из следующих этапов:</span><span class="sxs-lookup"><span data-stu-id="df6ac-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="df6ac-108">Решить, какие сведения будут содержаться формы с выбором набор свойств для хранения эти сведения.</span><span class="sxs-lookup"><span data-stu-id="df6ac-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="df6ac-109">Для получения дополнительных сведений см [Формы Property Set](choosing-a-form-s-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="df6ac-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="df6ac-110">Создание пользовательского интерфейса с помощью которой пользователи могут работать со свойствами формы.</span><span class="sxs-lookup"><span data-stu-id="df6ac-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="df6ac-111">Выбор класса сообщения и создания уникальный идентификатор класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="df6ac-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="df6ac-112">Обзор классов сообщений содержатся в разделе [Классы сообщений MAPI](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="df6ac-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="df6ac-113">Дополнительные сведения о формы и классы сообщений [Класс сообщения](choosing-a-message-class.md)см.</span><span class="sxs-lookup"><span data-stu-id="df6ac-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="df6ac-114">Реализация необходимых интерфейсов формы MAPI, а также дополнительные интерфейсы, необходимые серверу определенной формы.</span><span class="sxs-lookup"><span data-stu-id="df6ac-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="df6ac-115">Для получения дополнительных сведений см [Написание кода формы сервера](writing-form-server-code.md).</span><span class="sxs-lookup"><span data-stu-id="df6ac-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="df6ac-116">Написание кода интерфейса пользователя для обработки взаимодействия с пользователем с помощью объекта формы и свойства используется форма.</span><span class="sxs-lookup"><span data-stu-id="df6ac-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="df6ac-117">Создание файла конфигурации формы для формы.</span><span class="sxs-lookup"><span data-stu-id="df6ac-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="df6ac-118">Для получения дополнительных сведений см [файл формата из формы](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="df6ac-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="df6ac-119">Установка формы на компьютерах пользователей.</span><span class="sxs-lookup"><span data-stu-id="df6ac-119">Installing the form on users' computers.</span></span> <span data-ttu-id="df6ac-120">Для получения дополнительных сведений см [формы в библиотеку](installing-a-form-into-a-library.md).</span><span class="sxs-lookup"><span data-stu-id="df6ac-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="df6ac-121">Вероятнее всего, будет выполнять действия с 1 по 5 вместо завершения их в последовательности.</span><span class="sxs-lookup"><span data-stu-id="df6ac-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="df6ac-122">Процесс разработки форм сервера, как количество проектов программирования, не в котором имеется особенно строго определенную последовательность.</span><span class="sxs-lookup"><span data-stu-id="df6ac-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="df6ac-123">Например создание файла конфигурации формы отображается как второй к последний шаг выше, но, вероятно, создайте постепенного файла конфигурации формы и станет более полную как добавление компонентов к серверу формы.</span><span class="sxs-lookup"><span data-stu-id="df6ac-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df6ac-124">См. также</span><span class="sxs-lookup"><span data-stu-id="df6ac-124">See also</span></span>



[<span data-ttu-id="df6ac-125">Понятия MAPI</span><span class="sxs-lookup"><span data-stu-id="df6ac-125">MAPI Concepts</span></span>](mapi-concepts.md)

