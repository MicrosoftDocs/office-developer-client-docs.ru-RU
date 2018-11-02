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
ms.openlocfilehash: b07717a209fdb0152964bcd33d228d17cecd4eec
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922351"
---
# <a name="recordsetaddnew-method-dao"></a><span data-ttu-id="789f4-102">Метод Recordset.AddNew (DAO)</span><span class="sxs-lookup"><span data-stu-id="789f4-102">Recordset.AddNew method (DAO)</span></span>


<span data-ttu-id="789f4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="789f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="789f4-104">Создает новую запись для обновляемых объекта **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="789f4-104">Creates a new record for an updatable **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="789f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="789f4-105">Syntax</span></span>

<span data-ttu-id="789f4-106">*выражение* . AddNew</span><span class="sxs-lookup"><span data-stu-id="789f4-106">*expression* .AddNew</span></span>

<span data-ttu-id="789f4-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="789f4-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="789f4-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="789f4-108">Remarks</span></span>

<span data-ttu-id="789f4-109">Используйте метод **AddNew** для создания и добавления новой записи в объекте **набора записей** с именем, набора записей.</span><span class="sxs-lookup"><span data-stu-id="789f4-109">Use the **AddNew** method to create and add a new record in the **Recordset** object named by recordset.</span></span> <span data-ttu-id="789f4-110">Этого метода можно задать полей значения по умолчанию, и если нет значения по умолчанию не заданы, задает поля значение Null (значения по умолчанию, заданные для табличного типа **записей**).</span><span class="sxs-lookup"><span data-stu-id="789f4-110">This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset**).</span></span>

<span data-ttu-id="789f4-111">После изменения новую запись, используйте метод **[Update](recordset-update-method-dao.md)** чтобы сохранить изменения и добавления записи **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="789f4-111">After you modify the new record, use the **[Update](recordset-update-method-dao.md)** method to save the changes and add the record to the **Recordset**.</span></span> <span data-ttu-id="789f4-112">Без изменений в базе данных только при вызове метода **Update** .</span><span class="sxs-lookup"><span data-stu-id="789f4-112">No changes occur in the database until you use the **Update** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="789f4-113">Если выдача <STRONG>AddNew</STRONG> и затем выполнять любые операции, перемещает к другой записи, но без использования <STRONG>обновления</STRONG>, изменения не сохраняются без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="789f4-113">If you issue an <STRONG>AddNew</STRONG> and then perform any operation that moves to another record, but without using <STRONG>Update</STRONG>, your changes are lost without warning.</span></span> <span data-ttu-id="789f4-114">Кроме того при закрытии <STRONG>набора записей</STRONG> или закончить процедуру, которая объявляет <STRONG>записей</STRONG> или объект <STRONG><A href="database-object-dao.md">базы данных</A></STRONG> новую запись удаляется без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="789f4-114">In addition, if you close the <STRONG>Recordset</STRONG> or end the procedure that declares the <STRONG>Recordset</STRONG> or its <STRONG><A href="database-object-dao.md">Database</A></STRONG> object, the new record is discarded without warning.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="789f4-115">При использовании <STRONG>AddNew</STRONG> в рабочей области Microsoft Access и имеет ядро базы данных для создания новой страницы для хранения текущей записи, блокировка страницы жесткой.</span><span class="sxs-lookup"><span data-stu-id="789f4-115">When you use <STRONG>AddNew</STRONG> in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic.</span></span> <span data-ttu-id="789f4-116">Если новую запись помещается в существующей страницы, страницы блокировки оптимистичный.</span><span class="sxs-lookup"><span data-stu-id="789f4-116">If the new record fits in an existing page, page locking is optimistic.</span></span></P>



<span data-ttu-id="789f4-117">Если еще не к последнему перемещен записи из набора **записей**, записи, добавленные базовые таблицы для других процессов могут быть включены, если они размещены за пределы текущей записи.</span><span class="sxs-lookup"><span data-stu-id="789f4-117">If you haven't moved to the last record of your **Recordset**, records added to base tables by other processes may be included if they are positioned beyond the current record.</span></span> <span data-ttu-id="789f4-118">При добавлении записи для собственных **записей**тем не менее, запись будет отображаться в **набор записей** и включенных в базовой таблице, где он становится видимым для всех новых объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="789f4-118">If you add a record to your own **Recordset**, however, the record is visible in the **Recordset** and included in the underlying table where it becomes visible to any new **Recordset** objects.</span></span>

<span data-ttu-id="789f4-119">Положение новую запись зависит от типа **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="789f4-119">The position of the new record depends on the type of **Recordset**:</span></span>

  - <span data-ttu-id="789f4-120">В объект **набора записей** добавляющий записи вставляются в конце **набора записей**, независимо от того, сортировки или упорядочивания правил, которые использовались при открытии **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="789f4-120">In a dynaset-type **Recordset** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

  - <span data-ttu-id="789f4-121">В объекте **набора записей** тип таблицы, чьи свойства **[индекса](recordset-index-property-dao.md)** возвращаются записи в их местом в порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="789f4-121">In a table-type **Recordset** object whose **[Index](recordset-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order.</span></span> <span data-ttu-id="789f4-122">Если вы еще не настроили свойство **Index** , новые записи возвращаются в конце **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="789f4-122">If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="789f4-123">Записи, которая была текущей, прежде чем использовать **AddNew** остается текущей.</span><span class="sxs-lookup"><span data-stu-id="789f4-123">The record that was current before you used **AddNew** remains current.</span></span> <span data-ttu-id="789f4-124">Если вы хотите сделать новую запись текущей, можно задать свойства **[Bookmark](recordset-bookmark-property-dao.md)** закладку, определяемую средством настройки свойства **[LastModified](recordset-lastmodified-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="789f4-124">If you want to make the new record current, you can set the **[Bookmark](recordset-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset-lastmodified-property-dao.md)** property setting.</span></span>


> [!NOTE]
> <P><span data-ttu-id="789f4-125">Чтобы добавить, изменить или удалить записи, должен существовать уникальный индекс на запись в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="789f4-125">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="789f4-126">В противном случае ошибку «Отказано в доступе» произойдет на вызов метода <STRONG>AddNew</STRONG>, <STRONG>Удаление</STRONG>или <STRONG>Изменение</STRONG> в рабочей области Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="789f4-126">If not, a "Permission denied" error will occur on the <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG>, or <STRONG>Edit</STRONG> method call in a Microsoft Access workspace.</span></span></P>



## <a name="example"></a><span data-ttu-id="789f4-127">Пример</span><span class="sxs-lookup"><span data-stu-id="789f4-127">Example</span></span>

<span data-ttu-id="789f4-128">В этом примере используется метод **AddNew** , чтобы создать новую запись с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="789f4-128">This example uses the **AddNew** method to create a new record with the specified name.</span></span> <span data-ttu-id="789f4-129">Функция AddName является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="789f4-129">The AddName function is required for this procedure to run.</span></span>

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
