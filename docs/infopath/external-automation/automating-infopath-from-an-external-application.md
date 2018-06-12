---
title: Автоматизация InfoPath из внешнего приложения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath предоставляет автоматизации приложения из код, написанный с помощью COM и сценария с помощью методов объекта Application и коллекции XDocuments.
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807380"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="e3c0f-103">Автоматизация InfoPath из внешнего приложения</span><span class="sxs-lookup"><span data-stu-id="e3c0f-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="e3c0f-104">Microsoft InfoPath предоставляет автоматизации приложения из код, написанный с помощью COM и сценария с помощью методов объекта **Application** и коллекции **XDocuments** .</span><span class="sxs-lookup"><span data-stu-id="e3c0f-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="e3c0f-105">Общие сведения о приложении и объектами XDocument</span><span class="sxs-lookup"><span data-stu-id="e3c0f-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="e3c0f-106">Объект **приложения** содержит следующие методы, используемые для автоматизации:</span><span class="sxs-lookup"><span data-stu-id="e3c0f-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="e3c0f-107">**Способ**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-107">**Method**</span></span>|<span data-ttu-id="e3c0f-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3c0f-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="e3c0f-110">Проверяет в кэше и, при необходимости обновляет его из места опубликования шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="e3c0f-111">**Завершите работу**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-111">**Quit**</span></span> <br/> |<span data-ttu-id="e3c0f-112">Завершает работу приложения Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="e3c0f-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="e3c0f-114">Устанавливает указанный шаблон формы Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="e3c0f-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="e3c0f-116">Удаляет указанный шаблон формы Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="e3c0f-117">Коллекции **XDocuments** содержит следующие методы, которые могут быть использованы для внешней автоматизации.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="e3c0f-118">**Способ**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-118">**Method**</span></span>|<span data-ttu-id="e3c0f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3c0f-120">Метод **Close**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-120">**Close** method</span></span>  <br/> |<span data-ttu-id="e3c0f-121">Закрывает указанную форму Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="e3c0f-122">Метод **New**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-122">**New** method</span></span>  <br/> |<span data-ttu-id="e3c0f-123">Создает новую форму Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="e3c0f-124">Метод **NewFromSolution**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="e3c0f-125">Создает новую форму Microsoft Office InfoPath на основании указанного шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="e3c0f-126">Метод **NewFromSolutionWithData**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="e3c0f-127">Создает новую форму Microsoft Office InfoPath с помощью указанного шаблона формы и данные XML.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="e3c0f-128">Метод **Open**</span><span class="sxs-lookup"><span data-stu-id="e3c0f-128">**Open** method</span></span>  <br/> |<span data-ttu-id="e3c0f-129">Открывает указанную форму Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="e3c0f-130">Чтобы использовать объект **приложения** из внешнего приложения, используйте функции **CreateObject** с ProgID приложение InfoPath («InfoPath.Application») для создания переменной объекта, который представляет приложение InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="e3c0f-131">Затем можно использовать свойство **XDocuments** для доступа к коллекции **XDocuments** и использовать его методы для откройте или создайте форму InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="e3c0f-132">В следующем примере показано создание ссылки на объект **приложения** , с помощью Microsoft Visual Basic 6.0 или Visual Basic для приложений (VBA) языка программирования:</span><span class="sxs-lookup"><span data-stu-id="e3c0f-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="e3c0f-133">Так как функции **CreateObject** создает объектную переменную с помощью позднего связывания, автоматическом завершении не будут доступны в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="e3c0f-134">Обратитесь к ссылкам в таблицах выше сведения о правильный синтаксис вызова.</span><span class="sxs-lookup"><span data-stu-id="e3c0f-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

