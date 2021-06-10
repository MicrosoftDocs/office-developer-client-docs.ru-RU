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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294647"
---
# <a name="databases-collection-dao"></a><span data-ttu-id="bd61e-102">Коллекция баз данных (DAO)</span><span class="sxs-lookup"><span data-stu-id="bd61e-102">Databases collection (DAO)</span></span>

<span data-ttu-id="bd61e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd61e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd61e-104">Коллекция **баз данных** содержит все открытые объекты **базы** данных, открытые или созданные в **объекте Workspace.**</span><span class="sxs-lookup"><span data-stu-id="bd61e-104">A **Databases** collection contains all open **Database** objects opened or created in a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd61e-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd61e-105">Remarks</span></span>

<span data-ttu-id="bd61e-106">При открывлении существующего объекта **Базы** данных или создании нового из рабочей области он автоматически примыкает к коллекции **Баз данных.**</span><span class="sxs-lookup"><span data-stu-id="bd61e-106">When you open an existing **Database** object or create a new one from a **Workspace**, it is automatically appended to the **Databases** collection.</span></span> <span data-ttu-id="bd61e-107">Когда объект **базы данных** закрывается методом **[Close,](connection-close-method-dao.md)** он удаляется из коллекции **Баз** данных, но не удаляется с диска.</span><span class="sxs-lookup"><span data-stu-id="bd61e-107">When you close a **Database** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Databases** collection but not deleted from disk.</span></span> <span data-ttu-id="bd61e-108">Перед закрытием объекта Database необходимо закрыть все открытые **объекты** **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="bd61e-108">You should close all open **Recordset** objects before closing a **Database** object.</span></span>

<span data-ttu-id="bd61e-109">В рабочей области Microsoft Access параметр **свойства Name** базы данных — это строка, которая указывает путь файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="bd61e-109">In a Microsoft Access workspace, the **Name** property setting of a database is a string that specifies the path of the database file.</span></span>

<span data-ttu-id="bd61e-110">Чтобы сослаться на объект **Database** в коллекции по его порядковому номеру или по параметру свойства **Name,** используйте любую из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="bd61e-110">To refer to a **Database** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="bd61e-111">**Базы данных**(0)</span><span class="sxs-lookup"><span data-stu-id="bd61e-111">**Databases**(0)</span></span>

- <span data-ttu-id="bd61e-112">\**Базы данных\*\*\*("имя")*</span><span class="sxs-lookup"><span data-stu-id="bd61e-112">**Databases**("*name*")</span></span>

- <span data-ttu-id="bd61e-113">**Базы данных** \! \[ *имя*\]</span><span class="sxs-lookup"><span data-stu-id="bd61e-113">**Databases**\!\[*name*\]</span></span>

> [!NOTE]
> <span data-ttu-id="bd61e-114">Вы можете открывать один источник данных или базу данных несколько раз, создавая дублирующие имена в коллекции **Databases**.</span><span class="sxs-lookup"><span data-stu-id="bd61e-114">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection.</span></span> <span data-ttu-id="bd61e-115">Вы должны назначить объекты **Database** для переменных объекта и ссылаться на них по имени переменной.</span><span class="sxs-lookup"><span data-stu-id="bd61e-115">You should assign **Database** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="bd61e-116">Пример</span><span class="sxs-lookup"><span data-stu-id="bd61e-116">Example</span></span>

<span data-ttu-id="bd61e-117">В этом примере создается новый объект **Database** и открывается существующий объект **Database** в объекте **Workspace**, используемом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bd61e-117">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object.</span></span> <span data-ttu-id="bd61e-118">Затем выполняется перечисление коллекции **Database** и коллекции **Properties** каждого объекта **Database**.</span><span class="sxs-lookup"><span data-stu-id="bd61e-118">Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

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

<span data-ttu-id="bd61e-119">В этом примере используется метод **CreateDatabase** для создания нового зашифрованного объекта **Database**.</span><span class="sxs-lookup"><span data-stu-id="bd61e-119">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
