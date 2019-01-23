---
title: Метод Recordset.AddNew (DAO)
TOCTitle: AddNew Method
ms:assetid: 18cb35f6-8652-fb20-2460-3d13fae39d23
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845624(v=office.15)
ms:contentKeyID: 48543483
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052883
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 79c8691fcea7cf04bac7d6cd05711730b510e215
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703946"
---
# <a name="recordsetaddnew-method-dao"></a><span data-ttu-id="9e6f7-102">Метод Recordset.AddNew (DAO)</span><span class="sxs-lookup"><span data-stu-id="9e6f7-102">Recordset.AddNew Method (DAO)</span></span>

<span data-ttu-id="9e6f7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e6f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e6f7-104">Создает новую запись для обновляемого объекта **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-104">Creates a new record for an updatable **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e6f7-105">Syntax</span></span>

<span data-ttu-id="9e6f7-106">*expression* .AddNew</span><span class="sxs-lookup"><span data-stu-id="9e6f7-106">*expression* .AddNew</span></span>

<span data-ttu-id="9e6f7-107">*expression* — переменная, которая представляет объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-107">*expression* A variable that represents a **FileDialog** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e6f7-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e6f7-108">Remarks</span></span>

<span data-ttu-id="9e6f7-109">Метод **AddNew** используется для создания и добавления новой записи в объекте **Recordset** с именем набора записей.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-109">Use the **AddNew** method to create and add a new record in the **Recordset** object named by recordset.</span></span> <span data-ttu-id="9e6f7-110">Этот метод задает значения по умолчанию для полей, а если значения по умолчанию не указаны, он задает для полей значение Null (значения по умолчанию, указанные для **Recordset** табличного типа).</span><span class="sxs-lookup"><span data-stu-id="9e6f7-110">This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset**).</span></span>

<span data-ttu-id="9e6f7-111">Изменив новую запись, используйте метод **[Update](recordset-update-method-dao.md)**, чтобы сохранить изменения и добавить запись в объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-111">After you modify the new record, use the **[Update](recordset-update-method-dao.md)** method to save the changes and add the record to the **Recordset**.</span></span> <span data-ttu-id="9e6f7-112">В базу данных не будут внесены никакие изменения, пока вы не вызовете метод **Update**.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-112">No changes occur in the database until you use the **Update** method.</span></span>

> [!NOTE]
> <span data-ttu-id="9e6f7-113">Если вызвать метод **AddNew**, а затем выполнить какую-либо операцию, переходящую к другой записи, но без использования метода **Update**, то изменения будут потеряны без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-113">If you issue an **AddNew** and then perform any operation that moves to another record, but without using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="9e6f7-114">Кроме того, если закрыть объект **Recordset** или завершить процедуру, которая объявляет объект **Recordset** или его объект **[Database](database-object-dao.md)**, то новая запись удаляется без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-114">In addition, if you close the **Recordset** or end the procedure that declares the **Recordset** or its **[Database](database-object-dao.md)** object, the new record is discarded without warning.</span></span>

> [!NOTE]
> <span data-ttu-id="9e6f7-115">Если вы используете метод **AddNew** в рабочей области Microsoft Access, а ядру СУБД нужно создать новую страницу для хранения текущей записи, то используется пессимистическая блокировка страницы.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-115">When you use **AddNew** in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic.</span></span> <span data-ttu-id="9e6f7-116">Если новую запись можно разместить на имеющейся странице, то используется оптимистическая блокировка.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-116">If the new record fits in an existing page, page locking is optimistic.</span></span>

<span data-ttu-id="9e6f7-117">Если вы не перешли к последней записи в объекте **Recordset**, то записи, добавленные к базовым таблицам другими процессами, могут быть включены, если они находятся за пределами текущей записи.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-117">If you haven't moved to the last record of your **Recordset**, records added to base tables by other processes may be included if they are positioned beyond the current record.</span></span> <span data-ttu-id="9e6f7-118">Однако если добавить запись к собственному объекту **Recordset**, то запись будет видна в объекте **Recordset** и включена в базовую таблицу, где она становится видна всем новым объектам **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-118">If you add a record to your own **Recordset**, however, the record is visible in the **Recordset** and included in the underlying table where it becomes visible to any new **Recordset** objects.</span></span>

<span data-ttu-id="9e6f7-119">Расположение новой записи зависит от типа объекта **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="9e6f7-119">The position of the new record depends on the type of **Recordset**:</span></span>

- <span data-ttu-id="9e6f7-120">Если объект **Recordset** является динамическим подмножеством данных, то записи вставляются в конце объекта **Recordset** независимо от правил сортировки и упорядочения, которые действовали во время открытия объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-120">In a dynaset-type **Recordset** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

- <span data-ttu-id="9e6f7-121">В табличном объекте **Recordset**, для которого задано свойство **[Index](recordset-index-property-dao.md)**, записи возвращаются в надлежащем месте в порядке сортировки.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-121">In a table-type **Recordset** object whose **[Index](recordset-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order.</span></span> <span data-ttu-id="9e6f7-122">Если свойство **Index** не задано, новые записи возвращаются в конце объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-122">If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="9e6f7-123">Запись, которая была текущей до использования метода **AddNew**, остается текущей.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-123">The record that was current before you used **AddNew** remains current.</span></span> <span data-ttu-id="9e6f7-124">Если вам нужно сделать новую запись текущей, вы можете указать в свойстве **[Bookmark](recordset-bookmark-property-dao.md)** закладку, определяемую значением свойства **[LastModified](recordset-lastmodified-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-124">If you want to make the new record current, you can set the **[Bookmark](recordset-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset-lastmodified-property-dao.md)** property setting.</span></span>

> [!NOTE]
> <span data-ttu-id="9e6f7-125">Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-125">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="9e6f7-126">Если это не так, при вызове метода **AddNew**, **Delete** или **Edit** возникнет ошибка "Отказано в разрешении" в рабочей области Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-126">If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="9e6f7-127">Пример</span><span class="sxs-lookup"><span data-stu-id="9e6f7-127">Example</span></span>

<span data-ttu-id="9e6f7-128">В этом примере используется метод **AddNew**, чтобы создать запись с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-128">This example uses the **AddNew** method to create a new record with the specified name.</span></span> <span data-ttu-id="9e6f7-129">Функция AddName необходима для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-129">The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
