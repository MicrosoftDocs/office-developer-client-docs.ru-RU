---
title: Коллекция баз данных (DAO)
TOCTitle: Databases Collection
ms:assetid: 988ae6f5-ec15-cd1c-191d-f295624425f4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197944(v=office.15)
ms:contentKeyID: 48546493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbaa0fe7aaa50c8aec582e2f03cd2849268816b9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715552"
---
# <a name="databases-collection-dao"></a><span data-ttu-id="3a20f-102">Коллекция баз данных (DAO)</span><span class="sxs-lookup"><span data-stu-id="3a20f-102">Databases collection (DAO)</span></span>

<span data-ttu-id="3a20f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a20f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a20f-104">Коллекция **баз данных** содержит все открытые объекты **базы данных** открывается или созданы в **рабочей области для** объекта.</span><span class="sxs-lookup"><span data-stu-id="3a20f-104">A **Databases** collection contains all open **Database** objects opened or created in a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a20f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="3a20f-105">Remarks</span></span>

<span data-ttu-id="3a20f-106">При открытии существующего объекта **базы данных** или создайте новый из **рабочей области**, автоматически добавляется в коллекцию **баз данных** .</span><span class="sxs-lookup"><span data-stu-id="3a20f-106">When you open an existing **Database** object or create a new one from a **Workspace**, it is automatically appended to the **Databases** collection.</span></span> <span data-ttu-id="3a20f-107">При закрытии объекта **базы данных** с помощью метода **[закрытия](connection-close-method-dao.md)** , удалены из коллекции **баз данных** , но не удаляется с диска.</span><span class="sxs-lookup"><span data-stu-id="3a20f-107">When you close a **Database** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Databases** collection but not deleted from disk.</span></span> <span data-ttu-id="3a20f-108">Закройте все открытые объекты **набора записей** перед закрытием объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="3a20f-108">You should close all open **Recordset** objects before closing a **Database** object.</span></span>

<span data-ttu-id="3a20f-109">В рабочей области Microsoft Access **свойства Name базы данных** — это строка, которая указывает путь к файлу базы данных.</span><span class="sxs-lookup"><span data-stu-id="3a20f-109">In a Microsoft Access workspace, the **Name** property setting of a database is a string that specifies the path of the database file.</span></span>

<span data-ttu-id="3a20f-110">Для ссылки на объект **базы данных** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="3a20f-110">To refer to a **Database** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="3a20f-111">**Базы данных** (0)</span><span class="sxs-lookup"><span data-stu-id="3a20f-111">**Databases**(0)</span></span>

- <span data-ttu-id="3a20f-112">**Базы данных** («*имя*»)</span><span class="sxs-lookup"><span data-stu-id="3a20f-112">**Databases**("*name*")</span></span>

- <span data-ttu-id="3a20f-113">**Базы данных**\!\[*имя*\]</span><span class="sxs-lookup"><span data-stu-id="3a20f-113">**Databases**\!\[*name*\]</span></span>

> [!NOTE]
> <span data-ttu-id="3a20f-114">Можно открыть один и тот же источник данных или базы данных более одного раза, Создание повторяющихся имен в семействе **баз данных** .</span><span class="sxs-lookup"><span data-stu-id="3a20f-114">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection.</span></span> <span data-ttu-id="3a20f-115">Следует назначать объектных переменных объектов **базы данных** и обращаться к ним с именем переменной.</span><span class="sxs-lookup"><span data-stu-id="3a20f-115">You should assign **Database** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="3a20f-116">Пример</span><span class="sxs-lookup"><span data-stu-id="3a20f-116">Example</span></span>

<span data-ttu-id="3a20f-117">В этом примере создается новый объект **базы данных** и открывает существующий объект **базы данных** в объекте **рабочей области** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3a20f-117">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object.</span></span> <span data-ttu-id="3a20f-118">Затем перечисляет набор **баз данных** и коллекции **свойств** каждого объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="3a20f-118">Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccWorkspace", "admin", _ 
 "", dbUseJet) 
 
 ' Make sure there isn't already a file with the name of 
 ' the new database. 
 If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
 
 ' Create a new database with the specified 
 ' collating order. 
 Set dbsNew = wrkAcc.CreateDatabase("NewDB.mdb", _ 
 dbLangGeneral) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 With dbsLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of each 
 ' Database object. 
 For Each prpLoop In .Properties 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 End With 
 Next dbsLoop 
 
 dbsNew.Close 
 dbsNorthwind.Close 
 wrkAcc.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="3a20f-119">В этом примере используется **CreateDatabase** для создания нового, зашифрованные объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="3a20f-119">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
     Dim wrkDefault As Workspace 
     Dim dbsNew As DATABASE 
     Dim prpLoop As Property 
     
     ' Get default Workspace. 
     Set wrkDefault = DBEngine.Workspaces(0) 
     
     ' Make sure there isn't already a file with the name of 
     ' the new database. 
     If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
     ' Create a new encrypted database with the specified 
     ' collating order. 
     Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
     dbLangGeneral, dbEncrypt) 
     
     With dbsNew 
     Debug.Print "Properties of " & .Name 
     ' Enumerate the Properties collection of the new 
     ' Database object. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     End With 
     
     dbsNew.Close 
     
    End Sub
```
