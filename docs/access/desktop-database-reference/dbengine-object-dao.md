---
title: Объект DBEngine (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 479eff80d25279a1c5e918a3b639443ad3b25c6c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703687"
---
# <a name="dbengine-object-dao"></a><span data-ttu-id="b0208-102">Объект DBEngine (DAO)</span><span class="sxs-lookup"><span data-stu-id="b0208-102">DBEngine Object (DAO)</span></span>

<span data-ttu-id="b0208-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0208-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0208-104">Объект **DBEngine** — это объект верхнего уровня объектной модели DAO.</span><span class="sxs-lookup"><span data-stu-id="b0208-104">The **DBEngine** object is the top level object in the DAO object model.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0208-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0208-105">Remarks</span></span>

<span data-ttu-id="b0208-106">Объект **DBEngine** содержит и определяет все прочие объекты в иерархии объектов DAO.</span><span class="sxs-lookup"><span data-stu-id="b0208-106">The **DBEngine** object contains and controls all other objects in the hierarchy of DAO objects.</span></span> <span data-ttu-id="b0208-107">Вы не можете создавать дополнительные объекты **DBEngine** и объект **DBEngine** не является частью какой-либо коллекции.</span><span class="sxs-lookup"><span data-stu-id="b0208-107">You can't create additional **DBEngine** objects, and the **DBEngine** object isn't an element of any collection.</span></span>

<span data-ttu-id="b0208-108">С помощью любого типа базы данных или подключения вы можете:</span><span class="sxs-lookup"><span data-stu-id="b0208-108">With any type of database or connection, you can:</span></span>

  - <span data-ttu-id="b0208-109">Использовать свойство **Version**для получения номера версии DAO.</span><span class="sxs-lookup"><span data-stu-id="b0208-109">Use the **Version** property to obtain the DAO version number.</span></span>

  - <span data-ttu-id="b0208-110">Используйте свойство **LoginTimeout**, чтобы получить или задать время ожидания входа ODBC, и метод **RegisterDatabase**, чтобы предоставить информацию ODBC ядру СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b0208-110">Use the **LoginTimeout** property to obtain or set the ODBC login timeout, and the **RegisterDatabase** method to provide ODBC information to the Microsoft Access database engine.</span></span>

  - <span data-ttu-id="b0208-111">Используйте свойства **DefaultPassword** и **DefaultUser**, чтобы настроить идентификация и пароль пользователя для используемого по умолчанию объекта **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="b0208-111">Use the **DefaultPassword** and **DefaultUser** properties to set the user identification and password for the default **Workspace** object.</span></span>

  - <span data-ttu-id="b0208-112">Используйте метод **CreateWorkspace**, чтобы создать новый объект **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="b0208-112">Use the **CreateWorkspace** method to create a new **Workspace** object.</span></span> <span data-ttu-id="b0208-113">Вы можете использовать необязательные аргументы, чтобы переопределять свойства **DefaultType**, **DefaultPassword** и **DefaultUser**.</span><span class="sxs-lookup"><span data-stu-id="b0208-113">You can use optional arguments to override the settings of the **DefaultType**, **DefaultPassword**, and **DefaultUser** properties.</span></span>

  - <span data-ttu-id="b0208-114">Используйте метод **OpenDatabase**, чтобы открыть базу данных в используемом по умолчанию объекте **Workspace**, и методы **BeginTrans**, **Commit** и **Rollback** для управления транзакциями в используемом по умолчанию объекте **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="b0208-114">Use the **OpenDatabase** method to open a database in the default **Workspace**, and use the **BeginTrans**, **Commit**, and **Rollback** methods to control transactions on the default **Workspace**.</span></span>

  - <span data-ttu-id="b0208-115">Используйте коллекцию **Workspaces** для ссылки на конкретные объекты **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="b0208-115">Use the **Workspaces** collection to reference specific **Workspace** objects.</span></span>

  - <span data-ttu-id="b0208-116">Используйте коллекцию **Errors**, чтобы проверить сведения об ошибке доступа данных.</span><span class="sxs-lookup"><span data-stu-id="b0208-116">Use the **Errors** collection to examine data access error details.</span></span>

<span data-ttu-id="b0208-117">Другие свойства и методы доступны только при использовании DAO с ядром СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b0208-117">Other properties and methods are only available when you use DAO with the Microsoft Access database engine.</span></span> <span data-ttu-id="b0208-118">Можно использовать их для управления ядром СУБД Microsoft Access и его свойствами и выполнения задач на временных объектах, которые не являются элементами коллекции.</span><span class="sxs-lookup"><span data-stu-id="b0208-118">You can use them to control the Microsoft Access database engine, manipulate its properties, and perform tasks on temporary objects that aren't elements of collections.</span></span> <span data-ttu-id="b0208-119">Например, вы можете:</span><span class="sxs-lookup"><span data-stu-id="b0208-119">For example, you can use:</span></span>

  - <span data-ttu-id="b0208-120">Использовать метод **CreateDatabase**, чтобы создать новый объект **Database** ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b0208-120">Use the **CreateDatabase** method to create a new Microsoft Access database engine **Database** object.</span></span>

  - <span data-ttu-id="b0208-121">Используйте метод **Idle** для выполнения любой незавершенной задачи с помощью ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b0208-121">Use the **Idle** method to enable the Microsoft Access database engine to complete any pending tasks.</span></span>

  - <span data-ttu-id="b0208-122">Используйте методы **CompactDatabase** и **RepairDatabase** для сохранения файлов баз данных.</span><span class="sxs-lookup"><span data-stu-id="b0208-122">Use the **CompactDatabase** and **RepairDatabase** methods to maintain database files.</span></span>

  - <span data-ttu-id="b0208-123">Используйте свойства **IniPath** и **SystemDB**, чтобы указать расположение сведений реестра Windows для ядра СУБД Microsoft Access и файла с информацией о рабочей группы Microsoft Access соответственно.</span><span class="sxs-lookup"><span data-stu-id="b0208-123">Use the **IniPath** and **SystemDB** properties to specify the location of Microsoft Access database engine Windows Registry information and the Microsoft Access workgroup information file, respectively.</span></span> <span data-ttu-id="b0208-124">Метод **SetOption** позволяет перенастраивать параметры реестра Windows для ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b0208-124">The **SetOption** method allows you override windows registry settings for the Microsoft Access database engine.</span></span>

<span data-ttu-id="b0208-125">После изменения настроек свойств **DefaultType** и **IniPath** только последующие объекты **Workspace** отразят эти изменения.</span><span class="sxs-lookup"><span data-stu-id="b0208-125">After you change the **DefaultType** and **IniPath** property settings, only subsequent **Workspace** objects will reflect these changes.</span></span>

<span data-ttu-id="b0208-126">Чтобы сослаться на коллекцию, которая принадлежит к объекту **DBEngine** или чтобы сослаться на метод или свойство, которое относится к этому объекту, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="b0208-126">To refer to a collection that belongs to the **DBEngine** object, or to refer to a method or property that applies to this object, use this syntax:</span></span>

<span data-ttu-id="b0208-127">\[**DBEngine**.\]\[collection | method | property\]</span><span class="sxs-lookup"><span data-stu-id="b0208-127">\[**DBEngine**.\]\[collection | method | property\]</span></span>

## <a name="example"></a><span data-ttu-id="b0208-128">Пример</span><span class="sxs-lookup"><span data-stu-id="b0208-128">Example</span></span>

<span data-ttu-id="b0208-129">В этом примере перечисляется коллекция объекта **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="b0208-129">This example enumerates the collections of the **DBEngine** object.</span></span>

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
