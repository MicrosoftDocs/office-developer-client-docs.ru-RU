---
title: Коллекция TableDefs (DAO)
TOCTitle: TableDefs Collection
ms:assetid: a2986b02-0437-d6ac-7bbb-c43f5225c3fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820997(v=office.15)
ms:contentKeyID: 48546766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b265063d1912b81aa852505b756e58e7a643d4ae
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922946"
---
# <a name="tabledefs-collection-dao"></a><span data-ttu-id="86d47-102">Коллекция TableDefs (DAO)</span><span class="sxs-lookup"><span data-stu-id="86d47-102">TableDefs collection (DAO)</span></span>

<span data-ttu-id="86d47-103">**Применимо к:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="86d47-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="86d47-104">Коллекция **TableDefs** содержит все хранимые **TableDef** объектов базы данных (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="86d47-104">A **TableDefs** collection contains all stored **TableDef** objects in a database (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="86d47-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="86d47-105">Remarks</span></span>

<span data-ttu-id="86d47-106">Работа с помощью объекта **TableDef** и его методы и свойства определения таблицы.</span><span class="sxs-lookup"><span data-stu-id="86d47-106">You manipulate a table definition using a **TableDef** object and its methods and properties.</span></span>

<span data-ttu-id="86d47-107">Коллекцию объектов **базы данных** по умолчанию — коллекция **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="86d47-107">The default collection of a **Database** object is the **TableDefs** collection.</span></span>

<span data-ttu-id="86d47-108">Для ссылки на объект **TableDef** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="86d47-108">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="86d47-109">**TableDefs** (0)</span><span class="sxs-lookup"><span data-stu-id="86d47-109">**TableDefs**(0)</span></span>

<span data-ttu-id="86d47-110">**TableDefs** («имя»)</span><span class="sxs-lookup"><span data-stu-id="86d47-110">**TableDefs**("name")</span></span>

<span data-ttu-id="86d47-111">**TableDefs**\!\[имя\]</span><span class="sxs-lookup"><span data-stu-id="86d47-111">**TableDefs**\!\[name\]</span></span>

<span data-ttu-id="86d47-112">**Автор ссылки** [UtterAccess](https://www.utteraccess.com) сообщества.</span><span class="sxs-lookup"><span data-stu-id="86d47-112">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="86d47-113">UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="86d47-113">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

  - [<span data-ttu-id="86d47-114">Повторное компоновщика Multi-серверных системах</span><span class="sxs-lookup"><span data-stu-id="86d47-114">Re-Linker Multi-Backends</span></span>](https://www.utteraccess.com/wiki/index.php/re-linker_multi-backends)

  - [<span data-ttu-id="86d47-115">Файл подкачки и повторно связать между LIVE, тестирования и ЛОКАЛЬНЫХ данных</span><span class="sxs-lookup"><span data-stu-id="86d47-115">Swap/Relink Between LIVE, TEST and LOCAL Data</span></span>](https://www.utteraccess.com/forum/swap-relink-live-test-t1328573.html)

## <a name="example"></a><span data-ttu-id="86d47-116">Пример</span><span class="sxs-lookup"><span data-stu-id="86d47-116">Example</span></span>

<span data-ttu-id="86d47-117">В этом примере создается новый объект **TableDef** и добавляет его в коллекцию **TableDefs** объекта базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="86d47-117">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object.</span></span> <span data-ttu-id="86d47-118">Затем выполняется перечисление коллекции **TableDefs** и коллекции **свойств** нового **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="86d47-118">It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

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

<span data-ttu-id="86d47-119">В этом примере создается новый объект **TableDef** базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="86d47-119">This example creates a new **TableDef** object in the Northwind database.</span></span>

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



