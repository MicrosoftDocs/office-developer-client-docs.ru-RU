---
title: Объекты формы MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0cece598d4ad337e29edb3bb98b302de900e056d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593468"
---
# <a name="mapi-form-objects"></a><span data-ttu-id="9b586-103">Объекты формы MAPI</span><span class="sxs-lookup"><span data-stu-id="9b586-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="9b586-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b586-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b586-105">Объекты формы создаются динамически серверами формы для правильного отображения конкретные сообщения и пользователи могли взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="9b586-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="9b586-106">Объект формы является, таким образом, экземпляр класса, производного от [IMAPIForm](imapiformiunknown.md) , которая реализована на сервере формы.</span><span class="sxs-lookup"><span data-stu-id="9b586-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="9b586-107">При открытии сообщения в клиентское приложение сервера форм для этого класса сообщений создает объект формы для обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="9b586-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="9b586-108">Объект формы затем создает его интерфейс и отображает свойства сообщения в нем.</span><span class="sxs-lookup"><span data-stu-id="9b586-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="9b586-109">Объект формы и интерфейс повторяется, пока пользователь не закроет его.</span><span class="sxs-lookup"><span data-stu-id="9b586-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="9b586-110">Объект формы обрабатывает любые изменения значений свойств сообщений.</span><span class="sxs-lookup"><span data-stu-id="9b586-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="9b586-111">Кроме того интерфейсы формы MAPI определяет механизм, с помощью которого можно загружать и отображать несколько сообщений один объект формы.</span><span class="sxs-lookup"><span data-stu-id="9b586-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="9b586-112">Это механизм эффективности, как она позволяет избежать ненужного уничтожения и создания объектов сообщений и их интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="9b586-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="9b586-113">При запросе клиентом обмена сообщениями для загрузки другое сообщение, объект формы должен сохранить все изменения для свойства текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="9b586-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="9b586-114">Подробную информацию об Перспектива клиентское приложение объектов формы см [MAPI настраиваемые формы](mapi-custom-form-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9b586-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b586-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9b586-115">See also</span></span>



[<span data-ttu-id="9b586-116">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="9b586-116">MAPI Forms</span></span>](mapi-forms.md)

