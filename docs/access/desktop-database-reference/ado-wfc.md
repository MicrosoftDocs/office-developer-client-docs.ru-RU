---
title: ADO для классов Windows Foundation (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: da01d44e1e681a2de41741b11a9c412181c2fd9e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885082"
---
# <a name="adowfc"></a><span data-ttu-id="fdb1d-102">ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="fdb1d-102">ADO/WFC</span></span>


<span data-ttu-id="fdb1d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fdb1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fdb1d-104">ADO для Windows классов (ADO/WFC) основана на модели событий ADO и представляет упрощенный интерфейс программирования.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-104">ADO for Windows Foundation Classes (ADO/WFC) builds on the ADO event model and presents a simplified application programming interface.</span></span> <span data-ttu-id="fdb1d-105">В общем случае ADO/WFC перехватывает события ADO, объединяет параметры события в классе событий и затем вызывает обработчик события.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-105">In general, ADO/WFC intercepts ADO events, consolidates the event parameters into a single event class, and then calls your event handler.</span></span>

<span data-ttu-id="fdb1d-106">**Чтобы использовать события ADO в ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="fdb1d-106">**To use ADO events in ADO/WFC**</span></span>

1.  <span data-ttu-id="fdb1d-107">Определите обработчик событий для обработки события.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-107">Define your own event handler to process an event.</span></span> <span data-ttu-id="fdb1d-108">Например если вы хотите обрабатывать события **ConnectComplete** семейства **ConnectionEvent** , могут используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="fdb1d-108">For example, if you wanted to process the **ConnectComplete** event in the **ConnectionEvent** family, you might use this code:</span></span>
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  <span data-ttu-id="fdb1d-109">Определите объект обработчика для представления обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-109">Define a handler object to represent your event handler.</span></span> <span data-ttu-id="fdb1d-110">Объект обработчика должен иметь тип данных **ConnectEventHandler** для события типа **ConnectionEvent**или тип данных **RecordsetEventHandler** для события типа **RecordsetEvent**.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-110">The handler object should be of data type **ConnectEventHandler** for an event of type **ConnectionEvent**, or data type **RecordsetEventHandler** for an event of type **RecordsetEvent**.</span></span> <span data-ttu-id="fdb1d-111">Например код следующие параметры для обработчика событий **ConnectComplete** :</span><span class="sxs-lookup"><span data-stu-id="fdb1d-111">For example, code the following for your **ConnectComplete** event handler:</span></span>
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    <span data-ttu-id="fdb1d-112">Первый аргумент конструктора **ConnectionEventHandler** является ссылкой на класс, который содержит обработчик событий с именем в качестве второго аргумента.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-112">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument.</span></span> <span data-ttu-id="fdb1d-113">Компилятор Microsoft Visual J ++ также поддерживает эквивалентный синтаксис:</span><span class="sxs-lookup"><span data-stu-id="fdb1d-113">The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="fdb1d-114">Первый аргумент конструктора **ConnectionEventHandler** является ссылкой на класс, который содержит обработчик событий с именем в качестве второго аргумента.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-114">The first argument of the **ConnectionEventHandler** constructor is a reference to the class that contains the event handler named in the second argument.</span></span> <span data-ttu-id="fdb1d-115">Компилятор Microsoft Visual J ++ также поддерживает эквивалентный синтаксис:</span><span class="sxs-lookup"><span data-stu-id="fdb1d-115">The Microsoft Visual J++ compiler also supports an equivalent syntax:</span></span>
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    <span data-ttu-id="fdb1d-116">Один аргумент является ссылкой на нужный класс (**в этом**) и метода в класс (**onConnectComplete**).</span><span class="sxs-lookup"><span data-stu-id="fdb1d-116">The single argument is a reference to the desired class (**this**) and method within the class (**onConnectComplete**).</span></span>

3.  <span data-ttu-id="fdb1d-117">Добавление обработчика событий в список обработчиков, предназначенный для обработки конкретного типа событий.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-117">Add your event handler to a list of handlers designated to process a particular type of event.</span></span> <span data-ttu-id="fdb1d-118">Например, используйте метод с именем \**дополнительный компонент \*\*\* EventName*(*обработчик*).</span><span class="sxs-lookup"><span data-stu-id="fdb1d-118">Use the method with a name such as \**addOn\*\*\*EventName*(*handler*).</span></span>

4.  <span data-ttu-id="fdb1d-119">ADO/WFC во внутренней сети реализует все обработчики событий ADO.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-119">ADO/WFC internally implements all the ADO event handlers.</span></span> <span data-ttu-id="fdb1d-120">Таким образом с помощью обработчика событий ADO/WFC перехватывает события, вызванные операции **подключения** или **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="fdb1d-120">Therefore, an event caused by a **Connection** or **Recordset** operation is intercepted by an ADO/WFC event handler.</span></span> <span data-ttu-id="fdb1d-121">Обработчик событий ADO/WFC передает параметры ADO **ConnectionEvent** в экземпляр класса ADO/WFC **ConnectionEvent** или параметры ADO **RecordsetEvent** в экземпляр класса ADO/WFC **RecordsetEvent** .</span><span class="sxs-lookup"><span data-stu-id="fdb1d-121">The ADO/WFC event handler passes ADO **ConnectionEvent** parameters in an instance of the ADO/WFC **ConnectionEvent** class, or ADO **RecordsetEvent** parameters in an instance of the ADO/WFC **RecordsetEvent** class.</span></span> <span data-ttu-id="fdb1d-122">Эти классы ADO/WFC консолидировать параметры события ADO; то есть каждый класс ADO/WFC содержит один элемент данных для каждого уникального параметра в ADO **ConnectionEvent** или **RecordsetEvent** методов.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-122">These ADO/WFC classes consolidate the ADO event parameters; that is, each ADO/WFC class contains one data member for each unique parameter in all the ADO **ConnectionEvent** or **RecordsetEvent** methods.</span></span>

5.  <span data-ttu-id="fdb1d-123">ADO/WFC вызывает обработчик событий с помощью объекта ADO/WFC события.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-123">ADO/WFC then calls your event handler with the ADO/WFC event object.</span></span> <span data-ttu-id="fdb1d-124">Например обработчик **onConnectComplete** имеет подпись следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fdb1d-124">For example, your **onConnectComplete** handler has a signature like this:</span></span>
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    <span data-ttu-id="fdb1d-125">Первый аргумент — это тип объекта, отправляющий событие ([подключения](connection-object-ado.md) или [набора записей](recordset-object-ado.md)), а второй аргумент — это объект ADO/WFC событий (**ConnectionEvent** или **RecordsetEvent**).</span><span class="sxs-lookup"><span data-stu-id="fdb1d-125">The first argument is the type of object that sent the event ([Connection](connection-object-ado.md) or [Recordset](recordset-object-ado.md)), and the second argument is the ADO/WFC event object (**ConnectionEvent** or **RecordsetEvent**).</span></span> <span data-ttu-id="fdb1d-126">Подпись обработчика событий проще, чем событие ADO.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-126">The signature of your event handler is simpler than an ADO event.</span></span> <span data-ttu-id="fdb1d-127">Тем не менее по-прежнему необходимо понять модели событий ADO узнать параметры применяются к событию и о реагировании.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-127">However, you must still understand the ADO event model to know what parameters apply to an event and how to respond.</span></span>

6.  <span data-ttu-id="fdb1d-128">Возвращает из обработчика событий ADO/WFC обработчик для события ADO.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-128">Return from your event handler to the ADO/WFC handler for the ADO event.</span></span> <span data-ttu-id="fdb1d-129">ADO/WFC копирует соответствующие элементы данных ADO/WFC событие обратно в параметры события ADO и возвращает обработчик события ADO.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-129">ADO/WFC copies pertinent ADO/WFC event data members back to the ADO event parameters, and then the ADO event handler returns.</span></span>

7.  <span data-ttu-id="fdb1d-130">Завершении обработки, удалите обработчик из списка ADO/WFC обработчиков событий.</span><span class="sxs-lookup"><span data-stu-id="fdb1d-130">When you are finished processing, remove your handler from the list of ADO/WFC event handlers.</span></span> <span data-ttu-id="fdb1d-131">Например, используйте метод с именем \**removeOn \*\*\* EventName*(*обработчик*).</span><span class="sxs-lookup"><span data-stu-id="fdb1d-131">Use the method with a name such as \**removeOn\*\*\*EventName*(*handler*).</span></span>

