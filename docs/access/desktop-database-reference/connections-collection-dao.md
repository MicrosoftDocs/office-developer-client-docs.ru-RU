---
title: Подключения к коллекции (DAO)
TOCTitle: Connections collection
ms:assetid: 65d073be-a84b-e3f2-cb43-b87ffa60e497
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195178(v=office.15)
ms:contentKeyID: 48545330
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca6acbea99dd2a6dcb434cf4c4d18a0a065af133
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026017"
---
# <a name="connections-collection-dao"></a><span data-ttu-id="1914f-102">Подключения к коллекции (DAO)</span><span class="sxs-lookup"><span data-stu-id="1914f-102">Connections collection (DAO)</span></span>

<span data-ttu-id="1914f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1914f-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="1914f-104">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="1914f-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="1914f-105">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1914f-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="1914f-106">**Подключения к** коллекции содержит текущий объекты **подключения** объекта **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="1914f-106">A **Connections** collection contains the current **Connection** objects of a **Workspace** object.</span></span> <span data-ttu-id="1914f-107">(Технология ODBCDirect рабочие области только).</span><span class="sxs-lookup"><span data-stu-id="1914f-107">(ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="1914f-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="1914f-108">Remarks</span></span>

<span data-ttu-id="1914f-109">При открытии объект **подключения** , автоматически добавляется в коллекцию **подключения** **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="1914f-109">When you open a **Connection** object, it is automatically appended to the **Connections** collection of the **Workspace**.</span></span> <span data-ttu-id="1914f-110">При закрытии объекта **подключения** с помощью метода **[Закрыть](connection-close-method-dao.md)** , она удаляется из коллекции **подключений** .</span><span class="sxs-lookup"><span data-stu-id="1914f-110">When you close a **Connection** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Connections** collection.</span></span> <span data-ttu-id="1914f-111">Закройте все открытые объекты **[набора записей](recordset-object-dao.md)** в рамках **подключения** перед закрытием.</span><span class="sxs-lookup"><span data-stu-id="1914f-111">You should close all open **[Recordset](recordset-object-dao.md)** objects within the **Connection** before closing it.</span></span>

<span data-ttu-id="1914f-112">В то же время, откройте объект **подключения** , создается и добавляется в конец коллекции **[баз данных](databases-collection-dao.md)** в одной **рабочей области для**соответствующего объекта **[базы данных](database-object-dao.md)** и наоборот.</span><span class="sxs-lookup"><span data-stu-id="1914f-112">At the same time you open a **Connection** object, a corresponding **[Database](database-object-dao.md)** object is created and appended to the **[Databases](databases-collection-dao.md)** collection in the same **Workspace**, and vice versa.</span></span> <span data-ttu-id="1914f-113">Аналогичным образом при закрытии **подключения к**базе соответствующих **баз данных** удаляется из коллекции **баз данных** и т. д.</span><span class="sxs-lookup"><span data-stu-id="1914f-113">Similarly, when you close the **Connection**, the corresponding **Database** is deleted from the **Databases** collection, and so on.</span></span>

<span data-ttu-id="1914f-114">\*\*Свойства Name **подключения** \*\* — это строка, которая указывает путь к файлу базы данных.</span><span class="sxs-lookup"><span data-stu-id="1914f-114">The **Name** property setting of a **Connection** is a string that specifies the path of the database file.</span></span> <span data-ttu-id="1914f-115">Для ссылки на объект **подключения** в семействе сайтов, с его порядковый номер или **его свойства Name** , можно используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="1914f-115">To refer to a **Connection** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="1914f-116">**Подключения** (0)</span><span class="sxs-lookup"><span data-stu-id="1914f-116">**Connections**(0)</span></span>

- <span data-ttu-id="1914f-117">**Подключения** («*имя*»)</span><span class="sxs-lookup"><span data-stu-id="1914f-117">**Connections**("*name*")</span></span>

- <span data-ttu-id="1914f-118">**Подключения к**\!\[*имя*\]</span><span class="sxs-lookup"><span data-stu-id="1914f-118">**Connections**\!\[*name*\]</span></span>


> [!NOTE]
> <span data-ttu-id="1914f-119">Можно открыть один и тот же источник данных более одного раза, Создание повторяющихся имен в коллекции **Connections** .</span><span class="sxs-lookup"><span data-stu-id="1914f-119">You can open the same data source more than once, creating duplicate names in the **Connections** collection.</span></span> <span data-ttu-id="1914f-120">Следует назначить объекты **подключения** объектных переменных и обращаться к ним с именем переменной.</span><span class="sxs-lookup"><span data-stu-id="1914f-120">You should assign **Connection** objects to object variables and refer to them by variable name.</span></span>


## <a name="example"></a><span data-ttu-id="1914f-121">Пример</span><span class="sxs-lookup"><span data-stu-id="1914f-121">Example</span></span>

<span data-ttu-id="1914f-122">В этом примере демонстрируется объект **подключения** и **подключения к** коллекции, открыв объекта **базы данных** и два объекта технология ODBCDirect **подключения** и список свойств, доступных для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="1914f-122">This example demonstrates the **Connection** object and **Connections** collection by opening a **Database** object and two ODBCDirect **Connection** objects and listing the properties available to each object.</span></span>

```vb 
Sub ConnectionObjectX() 
 
   Dim wrkAcc as Workspace 
   Dim dbsNorthwind As Database 
   Dim wrkODBC As Workspace 
   Dim conPubs As Connection 
   Dim conPubs2 As Connection 
   Dim conLoop As Connection 
   Dim prpLoop As Property 
 
   ' Open a Database object. 
   Set wrkAcc = CreateWorkspace("NewWorkspace", _ 
      "admin", "", dbUseJet) 
   Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
   ' Create ODBCDirect Workspace object and open Connection 
   ' objects. 
   Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
      "admin", "", dbUseODBC) 
       
   ' Note: The DSNs referenced below must be configured to  
   '       use Microsoft Windows NT Authentication Mode to  
   '       authorize user access to the Microsoft SQL Server. 
   Set conPubs = wrkODBC.OpenConnection("Connection1", , , _ 
      "ODBC;DATABASE=pubs;DSN=Publishers") 
       
   Set conPubs2 = wrkODBC.OpenConnection("Connection2", , _ 
      True, "ODBC;DATABASE=pubs;DSN=Publishers") 
 
   Debug.Print "Database properties:" 
 
   With dbsNorthwind 
      ' Enumerate Properties collection of Database object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         Debug.Print "  " & prpLoop.Name & " = " & _ 
            prpLoop.Value 
         On Error GoTo 0 
      Next prpLoop 
   End With 
 
   ' Enumerate the Connections collection. 
   For Each conLoop In wrkODBC.Connections 
      Debug.Print "Connection properties for " & _ 
         conLoop.Name & ":" 
 
      With conLoop 
         ' Print property values by explicitly calling each 
         ' Property object; the Connection object does not 
         ' support a Properties collection. 
         Debug.Print "  Connect = " & .Connect 
         ' Property actually returns a Database object. 
         Debug.Print "  Database[.Name] = " & _ 
            .Database.Name 
         Debug.Print "  Name = " & .Name 
         Debug.Print "  QueryTimeout = " & .QueryTimeout 
         Debug.Print "  RecordsAffected = " & _ 
            .RecordsAffected 
         Debug.Print "  StillExecuting = " & _ 
            .StillExecuting 
         Debug.Print "  Transactions = " & .Transactions 
         Debug.Print "  Updatable = " & .Updatable 
      End With 
 
   Next conLoop 
 
   dbsNorthwind.Close 
   conPubs.Close 
   conPubs2.Close 
   wrkAcc.Close 
   wrkODBC.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="1914f-123">В этом примере используется метод **OpenConnection** с другими параметрами для открытия трех разных объектов **подключения** .</span><span class="sxs-lookup"><span data-stu-id="1914f-123">This example uses the **OpenConnection** method with different parameters to open three different **Connection** objects.</span></span>

```vb 
Sub OpenConnectionX() 
 
   Dim wrkODBC As Workspace 
   Dim conPubs As Connection 
   Dim conPubs2 As Connection 
   Dim conPubs3 As Connection 
   Dim conLoop As Connection 
 
   ' Create ODBCDirect Workspace object. 
   Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
      "admin", "", dbUseODBC) 
 
   ' Open Connection object using supplied information in  
   ' the connect string. If this information were  
   ' insufficient, you could trap for an error rather than  
   ' go to an ODBC Driver Manager dialog box. 
   MsgBox "Opening Connection1..." 
       
    ' Note: The DSN referenced below must be set to  
    '       use Microsoft Windows NT Authentication Mode to  
    '       authorize user access to the Microsoft SQL Server. 
    Set conPubs = wrkODBC.OpenConnection("Connection1", _ 
       dbDriverNoPrompt, , _ 
       "ODBC;DATABASE=pubs;DSN=Publishers") 
 
   ' Open read-only Connection object based on information  
   ' you enter in the ODBC Driver Manager dialog box. 
   MsgBox "Opening Connection2..." 
   Set conPubs2 = wrkODBC.OpenConnection("Connection2", _ 
      dbDriverPrompt, True, "ODBC;DSN=Publishers;") 
 
   ' Open read-only Connection object by entering only the  
   ' missing information in the ODBC Driver Manager dialog  
   ' box. 
   MsgBox "Opening Connection3..." 
   Set conPubs3 = wrkODBC.OpenConnection("Connection3", _ 
      dbDriverCompleteRequired, True, _ 
      "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
   ' Enumerate the Connections collection. 
   For Each conLoop In wrkODBC.Connections 
      Debug.Print "Connection properties for " & _ 
         conLoop.Name & ":" 
 
      With conLoop 
         ' Print property values by explicitly calling each 
         ' Property object; the Connection object does not 
         ' support a Properties collection. 
         Debug.Print "  Connect = " & .Connect 
         ' Property actually returns a Database object. 
         Debug.Print "  Database[.Name] = " & _ 
            .Database.Name 
         Debug.Print "  Name = " & .Name 
         Debug.Print "  QueryTimeout = " & .QueryTimeout 
         Debug.Print "  RecordsAffected = " & _ 
            .RecordsAffected 
         Debug.Print "  StillExecuting = " & _ 
            .StillExecuting 
         Debug.Print "  Transactions = " & .Transactions 
         Debug.Print "  Updatable = " & .Updatable 
      End With 
 
   Next conLoop 
 
   conPubs.Close 
   conPubs2.Close 
   conPubs3.Close 
   wrkODBC.Close 
 
End Sub 
 
```

