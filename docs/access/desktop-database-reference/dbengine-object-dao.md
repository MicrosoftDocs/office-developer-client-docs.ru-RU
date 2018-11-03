---
title: Объект DBEngine (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d0ebafc885e02d0098c67bb55e56a1744557973
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923604"
---
# <a name="dbengine-object-dao"></a><span data-ttu-id="5d65b-102">Объект DBEngine (DAO)</span><span class="sxs-lookup"><span data-stu-id="5d65b-102">DBEngine object (DAO)</span></span>

<span data-ttu-id="5d65b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d65b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d65b-104">Объект **DBEngine** — это объект верхнего уровня в объектной модели DAO.</span><span class="sxs-lookup"><span data-stu-id="5d65b-104">The **DBEngine** object is the top level object in the DAO object model.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d65b-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d65b-105">Remarks</span></span>

<span data-ttu-id="5d65b-106">Объект **DBEngine** содержит и управляет все объекты в иерархии объектов DAO.</span><span class="sxs-lookup"><span data-stu-id="5d65b-106">The **DBEngine** object contains and controls all other objects in the hierarchy of DAO objects.</span></span> <span data-ttu-id="5d65b-107">Не удается создать дополнительные объекты **DBEngine** и **DBEngine** объект не является элемент все семейства сайтов.</span><span class="sxs-lookup"><span data-stu-id="5d65b-107">You can't create additional **DBEngine** objects, and the **DBEngine** object isn't an element of any collection.</span></span>

<span data-ttu-id="5d65b-108">Любой тип базы данных или подключения можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5d65b-108">With any type of database or connection, you can:</span></span>

  - <span data-ttu-id="5d65b-109">Используйте свойство **Version** для получения номера версии DAO.</span><span class="sxs-lookup"><span data-stu-id="5d65b-109">Use the **Version** property to obtain the DAO version number.</span></span>

  - <span data-ttu-id="5d65b-110">Используйте свойство **LoginTimeout** получить или задать время ожидания входа ODBC, а метод **RegisterDatabase** для предоставления сведений ODBC к ядру базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5d65b-110">Use the **LoginTimeout** property to obtain or set the ODBC login timeout, and the **RegisterDatabase** method to provide ODBC information to the Microsoft Access database engine.</span></span>

  - <span data-ttu-id="5d65b-111">Используйте **DefaultPassword** и **DefaultUser** свойства, чтобы задать идентификатор пользователя и пароль для объекта **рабочей области** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5d65b-111">Use the **DefaultPassword** and **DefaultUser** properties to set the user identification and password for the default **Workspace** object.</span></span>

  - <span data-ttu-id="5d65b-112">Используйте метод **CreateWorkspace** для создания нового объекта **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="5d65b-112">Use the **CreateWorkspace** method to create a new **Workspace** object.</span></span> <span data-ttu-id="5d65b-113">Дополнительные аргументы, которые можно использовать для переопределения параметров свойства **DefaultType**, **DefaultPassword**и **DefaultUser** .</span><span class="sxs-lookup"><span data-stu-id="5d65b-113">You can use optional arguments to override the settings of the **DefaultType**, **DefaultPassword**, and **DefaultUser** properties.</span></span>

  - <span data-ttu-id="5d65b-114">Метод **OpenDatabase** используется для открытия базы данных в **рабочей области**по умолчанию и использовать **BeginTrans**, **завершения**и **отката** методы для управления транзакции в **рабочую область**по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5d65b-114">Use the **OpenDatabase** method to open a database in the default **Workspace**, and use the **BeginTrans**, **Commit**, and **Rollback** methods to control transactions on the default **Workspace**.</span></span>

  - <span data-ttu-id="5d65b-115">Используйте коллекцию **рабочих областей** для ссылок на объекты, определенные **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="5d65b-115">Use the **Workspaces** collection to reference specific **Workspace** objects.</span></span>

  - <span data-ttu-id="5d65b-116">Используйте коллекцию **ошибок** для просмотра сведений об ошибках доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="5d65b-116">Use the **Errors** collection to examine data access error details.</span></span>

<span data-ttu-id="5d65b-117">Другие свойства и методы доступны только при использовании DAO ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5d65b-117">Other properties and methods are only available when you use DAO with the Microsoft Access database engine.</span></span> <span data-ttu-id="5d65b-118">Можно использовать их для управления ядро базы данных Microsoft Access, изменить его свойства и выполнять задачи с временные объекты, не являющиеся частью коллекции.</span><span class="sxs-lookup"><span data-stu-id="5d65b-118">You can use them to control the Microsoft Access database engine, manipulate its properties, and perform tasks on temporary objects that aren't elements of collections.</span></span> <span data-ttu-id="5d65b-119">Например можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5d65b-119">For example, you can:</span></span>

  - <span data-ttu-id="5d65b-120">Метод **CreateDatabase** используется для создания нового объекта **базы данных** ядра базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5d65b-120">Use the **CreateDatabase** method to create a new Microsoft Access database engine **Database** object.</span></span>

  - <span data-ttu-id="5d65b-121">Используйте метод **Idle** для включения ядро базы данных Microsoft Access завершить все ожидающие задачи.</span><span class="sxs-lookup"><span data-stu-id="5d65b-121">Use the **Idle** method to enable the Microsoft Access database engine to complete any pending tasks.</span></span>

  - <span data-ttu-id="5d65b-122">Используйте методы **CompactDatabase** и **RepairDatabase** для сохранения файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="5d65b-122">Use the **CompactDatabase** and **RepairDatabase** methods to maintain database files.</span></span>

  - <span data-ttu-id="5d65b-123">Используйте **IniPath** и **SystemDB** свойства, чтобы указать расположение ядро СУБД Microsoft Access сведений реестра Windows и файл рабочей группы Microsoft Access, соответственно.</span><span class="sxs-lookup"><span data-stu-id="5d65b-123">Use the **IniPath** and **SystemDB** properties to specify the location of Microsoft Access database engine Windows Registry information and the Microsoft Access workgroup information file, respectively.</span></span> <span data-ttu-id="5d65b-124">Метод **SetOption** позволяет переопределить параметры реестра windows для ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5d65b-124">The **SetOption** method allows you override windows registry settings for the Microsoft Access database engine.</span></span>

<span data-ttu-id="5d65b-125">После изменения параметров свойства **DefaultType** и **IniPath** эти изменения будут отражены в последующих объектов **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="5d65b-125">After you change the **DefaultType** and **IniPath** property settings, only subsequent **Workspace** objects will reflect these changes.</span></span>

<span data-ttu-id="5d65b-126">Чтобы указать коллекцию параметров, к которой принадлежит объект **DBEngine** или ссылаться на метод или свойство, которое применяется для данного объекта, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="5d65b-126">To refer to a collection that belongs to the **DBEngine** object, or to refer to a method or property that applies to this object, use this syntax:</span></span>

<span data-ttu-id="5d65b-127">\[**DBEngine**. \] \[коллекции | метод | Свойство\]</span><span class="sxs-lookup"><span data-stu-id="5d65b-127">\[**DBEngine**.\]\[collection | method | property\]</span></span>

## <a name="example"></a><span data-ttu-id="5d65b-128">Пример</span><span class="sxs-lookup"><span data-stu-id="5d65b-128">Example</span></span>

<span data-ttu-id="5d65b-129">В этом примере перечисляются коллекций объектов **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="5d65b-129">This example enumerates the collections of the **DBEngine** object.</span></span>

```vb
    Sub DBEngineX() 
     
     Dim wrkLoop As Workspace 
     Dim prpLoop As Property 
     
     With DBEngine 
     Debug.Print "DBEngine Properties" 
     
     ' Enumerate Properties collection of DBEngine, 
     ' trapping for properties whose values are 
     ' invalid in this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " _ 
     & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Debug.Print "Workspaces collection of DBEngine" 
     
     ' Enumerate Workspaces collection of DBEngine. 
     For Each wrkLoop In .Workspaces 
     Debug.Print " " & wrkLoop.Name 
     
     ' Enumerate Properties collection of each 
     ' Workspace object, trapping for properties 
     ' whose values are invalid in this context. 
     For Each prpLoop In wrkLoop.Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Next wrkLoop 
     
     End With 
     
    End Sub
```
