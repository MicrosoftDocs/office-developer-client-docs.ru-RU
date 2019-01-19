---
title: Коллекция TableDefs (DAO)
TOCTitle: TableDefs Collection
ms:assetid: a2986b02-0437-d6ac-7bbb-c43f5225c3fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820997(v=office.15)
ms:contentKeyID: 48546766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f16f44b57a690aa58efdff9b00341df5023c293f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702882"
---
# <a name="tabledefs-collection-dao"></a><span data-ttu-id="fc99d-102">Коллекция TableDefs (DAO)</span><span class="sxs-lookup"><span data-stu-id="fc99d-102">TableDefs Collection (DAO)</span></span>

<span data-ttu-id="fc99d-103">**Область применения**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc99d-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="fc99d-104">Коллекция **TableDefs** содержит все сохраненные объекты **TableDef** в базе данных (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fc99d-104">A **TableDefs** collection contains all stored **TableDef** objects in a database (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc99d-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc99d-105">Remarks</span></span>

<span data-ttu-id="fc99d-106">Работа с определением таблицы выполняется с помощью объекта **TableDef** и его методов и свойств.</span><span class="sxs-lookup"><span data-stu-id="fc99d-106">You manipulate a table definition using a **TableDef** object and its methods and properties.</span></span>

<span data-ttu-id="fc99d-107">По умолчанию коллекция объекта **Database** – коллекция **TableDefs**</span><span class="sxs-lookup"><span data-stu-id="fc99d-107">The default collection of a **Database** object is the **TableDefs** collection.</span></span>

<span data-ttu-id="fc99d-108">Чтобы сослаться на объект **TableDef** в коллекции по его порядковому номеру или по его свойству**Name**, используйте любую из указанных ниже синтаксических форм.</span><span class="sxs-lookup"><span data-stu-id="fc99d-108">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="fc99d-109">**TableDefs**(0)</span><span class="sxs-lookup"><span data-stu-id="fc99d-109">**TableDefs**(0)</span></span>

<span data-ttu-id="fc99d-110">**TableDefs**("name")</span><span class="sxs-lookup"><span data-stu-id="fc99d-110">**TableDefs**("name")</span></span>

<span data-ttu-id="fc99d-111">**TableDefs**\!\[name\]</span><span class="sxs-lookup"><span data-stu-id="fc99d-111">**TableDefs**\!\[name\]</span></span>

<span data-ttu-id="fc99d-112">**Ссылки, предоставляемые** сообщества [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="fc99d-112">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="fc99d-113">UtterAccess — это премиальный wiki-портал и форум, посвященный Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fc99d-113">UtterAccess is the premier Microsoft Access wiki and help forum. Click here to join.
</span></span>

  - [<span data-ttu-id="fc99d-114">Инструмент повторной компоновки с множественной обработкой на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="fc99d-114">Re-Linker Multi-Backends</span></span>](https://www.utteraccess.com/wiki/index.php/re-linker_multi-backends)

  - [<span data-ttu-id="fc99d-115">Переключение/перекомпоновка между данными LIVE, TEST и LOCAL</span><span class="sxs-lookup"><span data-stu-id="fc99d-115">Swap/Relink Between LIVE, TEST and LOCAL Data</span></span>](https://www.utteraccess.com/forum/swap-relink-live-test-t1328573.html)

## <a name="example"></a><span data-ttu-id="fc99d-116">Пример</span><span class="sxs-lookup"><span data-stu-id="fc99d-116">Example</span></span>

<span data-ttu-id="fc99d-117">В этом примере создается новый объект **TableDef**, который добавляется в коллекцию **TableDefs** объекта базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="fc99d-117">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object.</span></span> <span data-ttu-id="fc99d-118">Затем перечисляются коллекции **TableDefs** и **Properties** нового объекта **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="fc99d-118">It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="fc99d-119">В этом примере создается новый объект **TableDef** в базе данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="fc99d-119">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
 
```



