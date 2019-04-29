---
title: Автоматизация InfoPath из внешнего приложения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath обеспечивает автоматизацию приложений из кода, написанного с помощью COM и сценариев, с помощью методов объекта Application и коллекции XDocument.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412669"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="56671-103">Автоматизация InfoPath из внешнего приложения</span><span class="sxs-lookup"><span data-stu-id="56671-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="56671-104">Microsoft InfoPath обеспечивает автоматизацию приложений из кода, написанного с помощью COM и сценариев, с помощью методов объекта **Application** и коллекции **XDocument** .</span><span class="sxs-lookup"><span data-stu-id="56671-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="56671-105">Общие сведения об объектах Application и XDocument</span><span class="sxs-lookup"><span data-stu-id="56671-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="56671-106">Объект **Application** содержит следующие методы, используемые для автоматизации:</span><span class="sxs-lookup"><span data-stu-id="56671-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="56671-107">**Метод**</span><span class="sxs-lookup"><span data-stu-id="56671-107">**Method**</span></span>|<span data-ttu-id="56671-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="56671-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56671-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="56671-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="56671-110">Проверяет в кэше и при необходимости обновляет его из расположения, в котором опубликован шаблон формы.</span><span class="sxs-lookup"><span data-stu-id="56671-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="56671-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="56671-111">**Quit**</span></span> <br/> |<span data-ttu-id="56671-112">Завершает работу приложения Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="56671-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="56671-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="56671-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="56671-114">Устанавливает указанный шаблон формы Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="56671-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="56671-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="56671-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="56671-116">Удаляет указанный шаблон формы Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="56671-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="56671-117">Коллекция **XDocuments** содержит следующие методы, которые можно использовать для внешней автоматизации:</span><span class="sxs-lookup"><span data-stu-id="56671-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="56671-118">**Метод**</span><span class="sxs-lookup"><span data-stu-id="56671-118">**Method**</span></span>|<span data-ttu-id="56671-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="56671-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56671-120">Метод **Close**</span><span class="sxs-lookup"><span data-stu-id="56671-120">**Close** method</span></span>  <br/> |<span data-ttu-id="56671-121">ЗаКрывает указанную форму Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="56671-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="56671-122">Метод **New**</span><span class="sxs-lookup"><span data-stu-id="56671-122">**New** method</span></span>  <br/> |<span data-ttu-id="56671-123">Создает новую форму Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="56671-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="56671-124">Метод **NewFromSolution**</span><span class="sxs-lookup"><span data-stu-id="56671-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="56671-125">Создает новую форму Microsoft Office InfoPath на основе указанного шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="56671-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="56671-126">Метод **невфромсолутионвисдата**</span><span class="sxs-lookup"><span data-stu-id="56671-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="56671-127">Создает новую форму Microsoft Office InfoPath с помощью указанных XML-данных и шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="56671-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="56671-128">Метод **Open**</span><span class="sxs-lookup"><span data-stu-id="56671-128">**Open** method</span></span>  <br/> |<span data-ttu-id="56671-129">Открывает указанную форму Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="56671-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="56671-130">Чтобы использовать объект **Application** из внешнего приложения, используйте функцию **CreateObject** с ProgID приложения InfoPath ("InfoPath. Application"), чтобы создать объектную переменную, представляющую приложение InfoPath.</span><span class="sxs-lookup"><span data-stu-id="56671-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="56671-131">Затем можно использовать свойство **XDocuments** для доступа к коллекции **XDocument** и использовать его методы для открытия или создания формы InfoPath.</span><span class="sxs-lookup"><span data-stu-id="56671-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="56671-132">В приведенном ниже примере показано создание ссылки на объект **Application** с помощью языка программирования Microsoft Visual Basic 6,0 или Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="56671-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="56671-133">Так как функция **CreateObject** создает объектную переменную с помощью позднего связывания, автоматическое завершение операторов будет недоступно в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="56671-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="56671-134">Чтобы получить сведения о правильном синтаксисе вызова, ознакомьтесь со ссылками, приведенными в предыдущих таблицах.</span><span class="sxs-lookup"><span data-stu-id="56671-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

