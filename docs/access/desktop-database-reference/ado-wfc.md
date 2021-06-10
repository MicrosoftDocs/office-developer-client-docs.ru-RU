---
title: ADO для Windows классов (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df9def320274df0eb4636aa237deb566dd5725b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281724"
---
# <a name="adowfc"></a><span data-ttu-id="16e3a-102">ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="16e3a-102">ADO/WFC</span></span>


<span data-ttu-id="16e3a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16e3a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16e3a-104">ADO для Windows классов Foundation (ADO/WFC) строится на модели событий ADO и представляет упрощенный интерфейс программирования приложений.</span><span class="sxs-lookup"><span data-stu-id="16e3a-104">ADO for Windows Foundation Classes (ADO/WFC) builds on the ADO event model and presents a simplified application programming interface.</span></span> <span data-ttu-id="16e3a-105">Как правило, ADO/WFC перехватывает события ADO, консолидирует параметры событий в один класс событий и вызывает обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="16e3a-105">In general, ADO/WFC intercepts ADO events, consolidates the event parameters into a single event class, and then calls your event handler.</span></span>

<span data-ttu-id="16e3a-106">**Использование событий ADO в ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="16e3a-106">**To use ADO events in ADO/WFC**</span></span>

1.  <span data-ttu-id="16e3a-107">Определите собственный обработник событий для обработки события.</span><span class="sxs-lookup"><span data-stu-id="16e3a-107">Define your own event handler to process an event.</span></span> <span data-ttu-id="16e3a-108">Например, если вы хотите обработать событие **ConnectComplete** в семейство **ConnectionEvent,** можно использовать этот код:</span><span class="sxs-lookup"><span data-stu-id="16e3a-108">For example, if you wanted to process the **ConnectComplete** event in the **ConnectionEvent** family, you might use this code:</span></span>
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  <span data-ttu-id="16e3a-109">Определите объект обработера, который будет представлять обработник событий.</span><span class="sxs-lookup"><span data-stu-id="16e3a-109">Define a handler object to represent your event handler.</span></span> <span data-ttu-id="16e3a-110">Объект обработки должен быть типа данных **ConnectEventHandler** для события типа **ConnectionEvent** или типа **данных RecordsetEventHandler** для события типа **RecordsetEvent**.</span><span class="sxs-lookup"><span data-stu-id="16e3a-110">The handler object should be of data type **ConnectEventHandler** for an event of type **ConnectionEvent**, or data type **RecordsetEventHandler** for an event of type **RecordsetEvent**.</span></span> <span data-ttu-id="16e3a-111">Например, закажете следующее для обработика событий **ConnectComplete:**</span><span class="sxs-lookup"><span data-stu-id="16e3a-111">For example, code the following for your **ConnectComplete** event handler:</span></span>
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    <span data-ttu-id="16e3a-112">Первый аргумент **конструктора ConnectionEventHandler** — это ссылка на класс, содержащий обработчик событий, названный во втором аргументе.</span><span class="sxs-lookup"><span data-stu-id="16e3a-112">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument.</span></span> <span data-ttu-id="16e3a-113">Компилятор Microsoft Visual J++ также поддерживает эквивалентный синтаксис:</span><span class="sxs-lookup"><span data-stu-id="16e3a-113">The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="16e3a-114">Первый аргумент **конструктора ConnectionEventHandler** — это ссылка на класс, содержащий обработчик событий, названный во втором аргументе.</span><span class="sxs-lookup"><span data-stu-id="16e3a-114">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument.</span></span> <span data-ttu-id="16e3a-115">Компилятор Microsoft Visual J++ также поддерживает эквивалентный синтаксис:</span><span class="sxs-lookup"><span data-stu-id="16e3a-115">The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="16e3a-116">Единственный аргумент — это ссылка на нужный класс **(это)** и метод в классе **(onConnectComplete).**</span><span class="sxs-lookup"><span data-stu-id="16e3a-116">The single argument is a reference to the desired class (**this**) and method within the class (**onConnectComplete**).</span></span>

3.  <span data-ttu-id="16e3a-117">Добавьте обработчик событий в список обработчиков, назначенных для обработки определенного типа события.</span><span class="sxs-lookup"><span data-stu-id="16e3a-117">Add your event handler to a list of handlers designated to process a particular type of event.</span></span> <span data-ttu-id="16e3a-118">Используйте метод с таким именем, как **addOn\*\*\*EventName**(обработник).\*</span><span class="sxs-lookup"><span data-stu-id="16e3a-118">Use the method with a name such as \**addOn\*\*\*EventName*(*handler*).</span></span>

4.  <span data-ttu-id="16e3a-119">ADO/WFC внутренне реализует все обработчики событий ADO.</span><span class="sxs-lookup"><span data-stu-id="16e3a-119">ADO/WFC internally implements all the ADO event handlers.</span></span> <span data-ttu-id="16e3a-120">Поэтому событие, вызванное операцией **Подключения** или **Recordset,** перехватывает обработчик событий ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="16e3a-120">Therefore, an event caused by a **Connection** or **Recordset** operation is intercepted by an ADO/WFC event handler.</span></span> <span data-ttu-id="16e3a-121">Обработник событий ADO/WFC передает параметры ADO **ConnectionEvent** в экземпляре класса ADO/WFC ConnectionEvent или параметры ADO **RecordsetEvent** в экземпляре класса ADO/WFC **RecordsetEvent.** </span><span class="sxs-lookup"><span data-stu-id="16e3a-121">The ADO/WFC event handler passes ADO **ConnectionEvent** parameters in an instance of the ADO/WFC **ConnectionEvent** class, or ADO **RecordsetEvent** parameters in an instance of the ADO/WFC **RecordsetEvent** class.</span></span> <span data-ttu-id="16e3a-122">Эти классы ADO/WFC консолидировать параметры событий ADO; то есть каждый класс ADO/WFC содержит по одному члену данных для каждого уникального параметра во всех методах ADO **ConnectionEvent** или **RecordsetEvent.**</span><span class="sxs-lookup"><span data-stu-id="16e3a-122">These ADO/WFC classes consolidate the ADO event parameters; that is, each ADO/WFC class contains one data member for each unique parameter in all the ADO **ConnectionEvent** or **RecordsetEvent** methods.</span></span>

5.  <span data-ttu-id="16e3a-123">Затем ADO/WFC вызывает обработник событий с объектом события ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="16e3a-123">ADO/WFC then calls your event handler with the ADO/WFC event object.</span></span> <span data-ttu-id="16e3a-124">Например, обработник **onConnectComplete** имеет подпись:</span><span class="sxs-lookup"><span data-stu-id="16e3a-124">For example, your **onConnectComplete** handler has a signature like this:</span></span>
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    <span data-ttu-id="16e3a-125">Первый аргумент — тип объекта, отправив событие [(Подключение](connection-object-ado.md) или Набор записей), [](recordset-object-ado.md)а второй аргумент — объект события ADO/WFC **(ConnectionEvent** или **RecordsetEvent).**</span><span class="sxs-lookup"><span data-stu-id="16e3a-125">The first argument is the type of object that sent the event ([Connection](connection-object-ado.md) or [Recordset](recordset-object-ado.md)), and the second argument is the ADO/WFC event object (**ConnectionEvent** or **RecordsetEvent**).</span></span> <span data-ttu-id="16e3a-126">Подпись обработера событий проще, чем событие ADO.</span><span class="sxs-lookup"><span data-stu-id="16e3a-126">The signature of your event handler is simpler than an ADO event.</span></span> <span data-ttu-id="16e3a-127">Однако для того, чтобы узнать, какие параметры применяются к событию и как реагировать, необходимо понять модель событий ADO.</span><span class="sxs-lookup"><span data-stu-id="16e3a-127">However, you must still understand the ADO event model to know what parameters apply to an event and how to respond.</span></span>

6.  <span data-ttu-id="16e3a-128">Вернись из обработки событий в обработник ADO/WFC для события ADO.</span><span class="sxs-lookup"><span data-stu-id="16e3a-128">Return from your event handler to the ADO/WFC handler for the ADO event.</span></span> <span data-ttu-id="16e3a-129">ADO/WFC копирует устроимые участники событий ADO/WFC обратно в параметры событий ADO, а затем обработник событий ADO возвращается.</span><span class="sxs-lookup"><span data-stu-id="16e3a-129">ADO/WFC copies pertinent ADO/WFC event data members back to the ADO event parameters, and then the ADO event handler returns.</span></span>

7.  <span data-ttu-id="16e3a-130">После завершения обработки удалите обработчик из списка обработчиков событий ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="16e3a-130">When you are finished processing, remove your handler from the list of ADO/WFC event handlers.</span></span> <span data-ttu-id="16e3a-131">Используйте метод с таким именем, как **removeOn\*\*\*EventName**(обработник).\*</span><span class="sxs-lookup"><span data-stu-id="16e3a-131">Use the method with a name such as \**removeOn\*\*\*EventName*(*handler*).</span></span>

