---
<span data-ttu-id="5db84-101"><<<<<<< Название HEAD: доступ к строк в иерархической TOCTitle записей: доступ к строк в иерархической записей ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 09/18 / 2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="5db84-101"><<<<<<< HEAD title: Accessing Rows in a Hierarchical Recordset TOCTitle: Accessing Rows in a Hierarchical Recordset ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="5db84-102">Accessing Rows in a Hierarchical Recordset</span><span class="sxs-lookup"><span data-stu-id="5db84-102">Accessing Rows in a Hierarchical Recordset</span></span>

<span data-ttu-id="5db84-103">=== Название: доступ к строк в иерархической TOCTitle записей: доступ к строк в иерархической ms:assetid записей: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 10/17/2018 mtps_version: v = Office.15</span><span class="sxs-lookup"><span data-stu-id="5db84-103">======= title: Accessing rows in a hierarchical Recordset TOCTitle: Accessing rows in a hierarchical Recordset ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="5db84-104">Доступ к строк в иерархической записей</span><span class="sxs-lookup"><span data-stu-id="5db84-104">Accessing rows in a hierarchical Recordset</span></span>
>>>>>>> <span data-ttu-id="5db84-105">master</span><span class="sxs-lookup"><span data-stu-id="5db84-105">master</span></span>

<span data-ttu-id="5db84-106">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5db84-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5db84-107">В следующем примере показано действия, необходимые для доступа к строк в иерархической [набора записей](recordset-object-ado.md):</span><span class="sxs-lookup"><span data-stu-id="5db84-107">The following example shows the steps necessary to access rows in a hierarchical [Recordset](recordset-object-ado.md):</span></span>

<span data-ttu-id="5db84-108"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="5db84-108"><<<<<<< HEAD</span></span>
1.  <span data-ttu-id="5db84-109">Объекты **набора записей** из авторов и titleauthor таблицы связаны с идентификатором автора.</span><span class="sxs-lookup"><span data-stu-id="5db84-109">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2.  <span data-ttu-id="5db84-110">Внешний цикл отображается имя и фамилию, состояние и идентификации каждого автора.</span><span class="sxs-lookup"><span data-stu-id="5db84-110">The outer loop displays each author's first and last name, state, and identification.</span></span>

3.  <span data-ttu-id="5db84-111">Добавленный **набора записей** для каждой строки извлекается из коллекции **полей** и назначается *rstTitleAuthor*.</span><span class="sxs-lookup"><span data-stu-id="5db84-111">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4.  <span data-ttu-id="5db84-112">Внутренний цикл отображаются четыре поля из каждой строки в присоединенной **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="5db84-112">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

<a name="the-stayinsyncstayinsync-property-adomd-property-is-set-to-false-for-purposes-of-illustration--so-you-can-see-the-chapter-change-explicitly-in-each-iteration-of-the-outer-loop-however-the-example-will-be-more-efficient-if-the-assignment-in-step-3-is-moved-before-the-first-line-in-step-2-so-that-the-assignment-is-performed-only-once-then-set-the-stayinsync-property-to-true-so-that-rsttitleauthor-will-implicitly-and-automatically-change-to-the-corresponding-chapter-whenever-rst-moves-to-a-new-row"></a><span data-ttu-id="5db84-113">(Свойство [StayInSync](stayinsync-property-ado.md) задано значение FALSE для наглядности, чтобы увидеть, главы явным образом изменить в каждой итерации внешнего цикла.</span><span class="sxs-lookup"><span data-stu-id="5db84-113">(The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration — so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="5db84-114">Тем не менее пример будет более эффективным, если назначение на шаге 3 перемещается перед первой строки на шаге 2, поэтому назначения выполняется только один раз.</span><span class="sxs-lookup"><span data-stu-id="5db84-114">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="5db84-115">Задайте свойство **StayInSync** имеет значение TRUE, таким образом, чтобы *rstTitleAuthor* неявно и автоматически изменится на соответствующий главы каждый раз, когда *rst* перемещает на новую строку.)</span><span class="sxs-lookup"><span data-stu-id="5db84-115">Then set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.)</span></span>
=======
1. <span data-ttu-id="5db84-116">Объекты **набора записей** из авторов и titleauthor таблицы связаны с идентификатором автора.</span><span class="sxs-lookup"><span data-stu-id="5db84-116">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2. <span data-ttu-id="5db84-117">Внешний цикл отображается имя и фамилию, состояние и идентификации каждого автора.</span><span class="sxs-lookup"><span data-stu-id="5db84-117">The outer loop displays each author's first and last name, state, and identification.</span></span>

3. <span data-ttu-id="5db84-118">Добавленный **набора записей** для каждой строки извлекается из коллекции **полей** и назначается *rstTitleAuthor*.</span><span class="sxs-lookup"><span data-stu-id="5db84-118">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4. <span data-ttu-id="5db84-119">Внутренний цикл отображаются четыре поля из каждой строки в присоединенной **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="5db84-119">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

> [!NOTE] 
> <span data-ttu-id="5db84-120">Свойство [StayInSync](stayinsync-property-ado.md) присвоено значение FALSE для наглядности, чтобы увидеть, главы явным образом изменить в каждой итерации внешнего цикла.</span><span class="sxs-lookup"><span data-stu-id="5db84-120">The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration, so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="5db84-121">Тем не менее пример будет более эффективным, если назначение на шаге 3 перемещается перед первой строки на шаге 2, поэтому назначения выполняется только один раз.</span><span class="sxs-lookup"><span data-stu-id="5db84-121">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="5db84-122">Присвойте свойству **StayInSync** значение TRUE, поэтому *rstTitleAuthor* неявно и автоматически изменится на соответствующий главы каждый раз, когда *rst* перемещает на новую строку.</span><span class="sxs-lookup"><span data-stu-id="5db84-122">Set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.</span></span>
>>>>>>> <span data-ttu-id="5db84-123">master</span><span class="sxs-lookup"><span data-stu-id="5db84-123">master</span></span>

<span data-ttu-id="5db84-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="5db84-124">**Example**</span></span>

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

