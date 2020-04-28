---
title: Метод Recordset2. AddNew (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 49a69b5e8603e72faaba480ea9069d3668bd6de1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307499"
---
# <a name="recordset2addnew-method-dao"></a><span data-ttu-id="0e309-102">Метод Recordset2. AddNew (DAO)</span><span class="sxs-lookup"><span data-stu-id="0e309-102">Recordset2.AddNew method (DAO)</span></span>

<span data-ttu-id="0e309-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e309-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="0e309-104">Создает новую запись для обновляемого объекта **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="0e309-104">Creates a new record for an updatable **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e309-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e309-105">Syntax</span></span>

<span data-ttu-id="0e309-106">*expression* .AddNew</span><span class="sxs-lookup"><span data-stu-id="0e309-106">*expression* .AddNew</span></span>

<span data-ttu-id="0e309-107">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="0e309-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e309-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e309-108">Remarks</span></span>

<span data-ttu-id="0e309-109">Используйте метод **AddNew** для создания и добавления новой записи в объект **Recordset2** с именем Recordset.</span><span class="sxs-lookup"><span data-stu-id="0e309-109">Use the **AddNew** method to create and add a new record in the **Recordset2** object named by recordset.</span></span> <span data-ttu-id="0e309-110">Этот метод задает для полей значения по умолчанию, а если значения по умолчанию не указаны, то для полей задаются значения NULL (значения по умолчанию, указанные для параметра table-Type **Recordset2**).</span><span class="sxs-lookup"><span data-stu-id="0e309-110">This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset2**).</span></span>

<span data-ttu-id="0e309-111">После изменения новой записи используйте метод **[Update](recordset2-update-method-dao.md)** , чтобы сохранить изменения и добавить запись в **Recordset2**.</span><span class="sxs-lookup"><span data-stu-id="0e309-111">After you modify the new record, use the **[Update](recordset2-update-method-dao.md)** method to save the changes and add the record to the **Recordset2**.</span></span> <span data-ttu-id="0e309-112">В базу данных не будут внесены никакие изменения, пока вы не вызовете метод **Update**.</span><span class="sxs-lookup"><span data-stu-id="0e309-112">No changes occur in the database until you use the **Update** method.</span></span>

> [!NOTE]
> <span data-ttu-id="0e309-113">Если вызвать метод **AddNew**, а затем выполнить какую-либо операцию, переходящую к другой записи, но без использования метода **Update**, то изменения будут потеряны без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="0e309-113">If you issue an **AddNew** and then perform any operation that moves to another record, but without using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="0e309-114">Кроме того, если закрыть **Recordset2** или завершить процедуру, которая объявляет **Recordset2** , или ее объект **[Database](database-object-dao.md)** , Новая запись отбрасывается без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="0e309-114">In addition, if you close the **Recordset2** or end the procedure that declares the **Recordset2** or its **[Database](database-object-dao.md)** object, the new record is discarded without warning.</span></span>

> [!NOTE]
> <span data-ttu-id="0e309-115">Если вы используете метод **AddNew** в рабочей области Microsoft Access, а ядру СУБД нужно создать новую страницу для хранения текущей записи, то используется пессимистическая блокировка страницы.</span><span class="sxs-lookup"><span data-stu-id="0e309-115">When you use **AddNew** in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic.</span></span> <span data-ttu-id="0e309-116">Если новую запись можно разместить на имеющейся странице, то используется оптимистическая блокировка.</span><span class="sxs-lookup"><span data-stu-id="0e309-116">If the new record fits in an existing page, page locking is optimistic.</span></span>

<span data-ttu-id="0e309-117">Если вы еще не переместили в последнюю запись **Recordset2**, то записи, добавленные в базовые таблицы другими процессами, могут быть включены, если они расположены за пределами текущей записи.</span><span class="sxs-lookup"><span data-stu-id="0e309-117">If you haven't moved to the last record of your **Recordset2**, records added to base tables by other processes may be included if they are positioned beyond the current record.</span></span> <span data-ttu-id="0e309-118">Однако при добавлении записи в собственный **Recordset2**запись отображается в **Recordset2** и включается в базовую таблицу, где она становится видимой для всех новых объектов **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="0e309-118">If you add a record to your own **Recordset2**, however, the record is visible in the **Recordset2** and included in the underlying table where it becomes visible to any new **Recordset2** objects.</span></span>

<span data-ttu-id="0e309-119">Положение новой записи зависит от типа **Recordset2**:</span><span class="sxs-lookup"><span data-stu-id="0e309-119">The position of the new record depends on the type of **Recordset2**:</span></span>

- <span data-ttu-id="0e309-120">В объекте динамического подмножества **Recordset2** записи вставляются в конец **набора записей**независимо от правил сортировки или сортировки, которые действовали при открытии **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="0e309-120">In a dynaset-type **Recordset2** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

- <span data-ttu-id="0e309-121">В объекте табличного типа **Recordset2** , свойство **[index](recordset2-index-property-dao.md)** которого было задано, записи возвращаются в надлежащем месте в порядке сортировки.</span><span class="sxs-lookup"><span data-stu-id="0e309-121">In a table-type **Recordset2** object whose **[Index](recordset2-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order.</span></span> <span data-ttu-id="0e309-122">Если свойство **Index** не задано, новые записи возвращаются в конце объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0e309-122">If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="0e309-123">Запись, которая была текущей до использования метода **AddNew**, остается текущей.</span><span class="sxs-lookup"><span data-stu-id="0e309-123">The record that was current before you used **AddNew** remains current.</span></span> <span data-ttu-id="0e309-124">Если вам нужно сделать новую запись текущей, вы можете указать в свойстве **[Bookmark](recordset2-bookmark-property-dao.md)** закладку, определяемую значением свойства **[LastModified](recordset2-lastmodified-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="0e309-124">If you want to make the new record current, you can set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset2-lastmodified-property-dao.md)** property setting.</span></span>

> [!NOTE]
> <span data-ttu-id="0e309-125">Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс.</span><span class="sxs-lookup"><span data-stu-id="0e309-125">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="0e309-126">Если это не так, при вызове метода **AddNew**, **Delete** или **Edit** возникнет ошибка "Отказано в разрешении" в рабочей области Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0e309-126">If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="0e309-127">Пример</span><span class="sxs-lookup"><span data-stu-id="0e309-127">Example</span></span>

<span data-ttu-id="0e309-128">В этом примере используется метод **AddNew**, чтобы создать запись с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="0e309-128">This example uses the **AddNew** method to create a new record with the specified name.</span></span> <span data-ttu-id="0e309-129">Функция AddName необходима для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="0e309-129">The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
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
     
    Function AddName(rstTemp As Recordset2, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a recordset using the data passed 
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
