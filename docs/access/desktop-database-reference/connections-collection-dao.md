---
title: Коллекция Connections (DAO)
TOCTitle: Connections collection
ms:assetid: 65d073be-a84b-e3f2-cb43-b87ffa60e497
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195178(v=office.15)
ms:contentKeyID: 48545330
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 66f122b7bdaa9069b839cd5884b5da5da48a15f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295788"
---
# <a name="connections-collection-dao"></a><span data-ttu-id="64b39-102">Коллекция Connections (DAO)</span><span class="sxs-lookup"><span data-stu-id="64b39-102">Connections collection (DAO)</span></span>

<span data-ttu-id="64b39-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64b39-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="64b39-104">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="64b39-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="64b39-105">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="64b39-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="64b39-106">Коллекция **Connections** содержит текущие объекты **подключения** объекта **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="64b39-106">A **Connections** collection contains the current **Connection** objects of a **Workspace** object.</span></span> <span data-ttu-id="64b39-107">(Только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="64b39-107">(ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="64b39-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="64b39-108">Remarks</span></span>

<span data-ttu-id="64b39-109">При открытии объекта **подключения** он автоматически добавляется в коллекцию **Connections** **рабочей области**.</span><span class="sxs-lookup"><span data-stu-id="64b39-109">When you open a **Connection** object, it is automatically appended to the **Connections** collection of the **Workspace**.</span></span> <span data-ttu-id="64b39-110">При закрытии объекта **Connection** с помощью метода **[Close](connection-close-method-dao.md)** он удаляется из коллекции **Connections** .</span><span class="sxs-lookup"><span data-stu-id="64b39-110">When you close a **Connection** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Connections** collection.</span></span> <span data-ttu-id="64b39-111">Прежде чем закрыть все открытые объекты **[Recordset](recordset-object-dao.md)** в **подключении** , необходимо закрыть их.</span><span class="sxs-lookup"><span data-stu-id="64b39-111">You should close all open **[Recordset](recordset-object-dao.md)** objects within the **Connection** before closing it.</span></span>

<span data-ttu-id="64b39-112">При открытии объекта **Connection** создается соответствующий объект **[базы данных](database-object-dao.md)** , который добавляется в коллекцию **[баз данных](databases-collection-dao.md)** в той же **рабочей области**и наоборот.</span><span class="sxs-lookup"><span data-stu-id="64b39-112">At the same time you open a **Connection** object, a corresponding **[Database](database-object-dao.md)** object is created and appended to the **[Databases](databases-collection-dao.md)** collection in the same **Workspace**, and vice versa.</span></span> <span data-ttu-id="64b39-113">Аналогично, когда вы закрываете **Подключение**, соответствующая **база данных** удаляется из коллекции **баз данных** и т. д.</span><span class="sxs-lookup"><span data-stu-id="64b39-113">Similarly, when you close the **Connection**, the corresponding **Database** is deleted from the **Databases** collection, and so on.</span></span>

<span data-ttu-id="64b39-114">Значение свойства **Name** для **подключения** — это строка, указывающая путь к файлу базы данных.</span><span class="sxs-lookup"><span data-stu-id="64b39-114">The **Name** property setting of a **Connection** is a string that specifies the path of the database file.</span></span> <span data-ttu-id="64b39-115">Чтобы сослаться на объект **Connection** в коллекции по его порядковому номеру или по значению свойства **Name** , используйте любую из следующих синтаксических форм:</span><span class="sxs-lookup"><span data-stu-id="64b39-115">To refer to a **Connection** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="64b39-116">**Подключения**(0)</span><span class="sxs-lookup"><span data-stu-id="64b39-116">**Connections**(0)</span></span>

- <span data-ttu-id="64b39-117">**Connections**("*Name*")</span><span class="sxs-lookup"><span data-stu-id="64b39-117">**Connections**("*name*")</span></span>

- <span data-ttu-id="64b39-118">**Connections**\!\[*Имя* подключений\]</span><span class="sxs-lookup"><span data-stu-id="64b39-118">**Connections**\!\[*name*\]</span></span>


> [!NOTE]
> <span data-ttu-id="64b39-119">Вы можете открыть один и тот же источник данных несколько раз, создав повторяющиеся имена в коллекции **Connections** .</span><span class="sxs-lookup"><span data-stu-id="64b39-119">You can open the same data source more than once, creating duplicate names in the **Connections** collection.</span></span> <span data-ttu-id="64b39-120">Необходимо назначить объекты **подключения** переменным объектов и ссылаться на них по имени переменной.</span><span class="sxs-lookup"><span data-stu-id="64b39-120">You should assign **Connection** objects to object variables and refer to them by variable name.</span></span>


## <a name="example"></a><span data-ttu-id="64b39-121">Пример</span><span class="sxs-lookup"><span data-stu-id="64b39-121">Example</span></span>

<span data-ttu-id="64b39-122">В этом примере демонстрируется объект **Connection** и коллекция **Connections** , открывая объект **базы данных** и два объекта **подключения** ODBCDirect и указывая свойства, доступные для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="64b39-122">This example demonstrates the **Connection** object and **Connections** collection by opening a **Database** object and two ODBCDirect **Connection** objects and listing the properties available to each object.</span></span>

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

<span data-ttu-id="64b39-123">В этом примере используется метод **OpenConnection** с другими параметрами для открытия трех различных объектов **Connection** .</span><span class="sxs-lookup"><span data-stu-id="64b39-123">This example uses the **OpenConnection** method with different parameters to open three different **Connection** objects.</span></span>

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

