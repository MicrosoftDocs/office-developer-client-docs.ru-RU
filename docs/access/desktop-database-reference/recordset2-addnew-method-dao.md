---
title: Recordset2.AddNew Method (DAO)
TOCTitle: AddNew Method
ms:assetid: 25c7d207-185c-943b-405e-b138ffb8b3e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191874(v=office.15)
ms:contentKeyID: 48543792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e8123fc67d8b41b892f92b19605a26384af68b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481307"
---
# <a name="recordset2addnew-method-dao"></a><span data-ttu-id="a7b0a-102">Recordset2.AddNew Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a7b0a-102">Recordset2.AddNew Method (DAO)</span></span>


<span data-ttu-id="a7b0a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7b0a-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="a7b0a-104">Создает новую запись для объекта обновляемых **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="a7b0a-104">Creates a new record for an updatable **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7b0a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7b0a-105">Syntax</span></span>

<span data-ttu-id="a7b0a-106">*выражение* . AddNew</span><span class="sxs-lookup"><span data-stu-id="a7b0a-106">*expression* .AddNew</span></span>

<span data-ttu-id="a7b0a-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="a7b0a-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7b0a-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="a7b0a-108">Remarks</span></span>

<span data-ttu-id="a7b0a-109">Используйте метод **AddNew** создает и добавляет новую запись в объекте **Recordset2** с именем, набора записей.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-109">Use the **AddNew** method to create and add a new record in the **Recordset2** object named by recordset.</span></span> <span data-ttu-id="a7b0a-110">Этого метода можно задать полей значения по умолчанию, и если нет значения по умолчанию не заданы, задает поля значение Null (значения по умолчанию для типа таблицы **Recordset2**).</span><span class="sxs-lookup"><span data-stu-id="a7b0a-110">This method sets the fields to default values, and if no default values are specified, it sets the fields to Null (the default values specified for a table-type **Recordset2**).</span></span>

<span data-ttu-id="a7b0a-111">После изменения новую запись, используйте метод **[Update](recordset2-update-method-dao.md)** чтобы сохранить изменения и добавления записи **Recordset2**.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-111">After you modify the new record, use the **[Update](recordset2-update-method-dao.md)** method to save the changes and add the record to the **Recordset2**.</span></span> <span data-ttu-id="a7b0a-112">Без изменений в базе данных только при вызове метода **Update** .</span><span class="sxs-lookup"><span data-stu-id="a7b0a-112">No changes occur in the database until you use the **Update** method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a7b0a-113">Если выдача <STRONG>AddNew</STRONG> и затем выполнять любые операции, перемещает к другой записи, но без использования <STRONG>обновления</STRONG>, изменения не сохраняются без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-113">If you issue an <STRONG>AddNew</STRONG> and then perform any operation that moves to another record, but without using <STRONG>Update</STRONG>, your changes are lost without warning.</span></span> <span data-ttu-id="a7b0a-114">Кроме того Если закрыть <STRONG>Recordset2</STRONG> или закончить процедуру, которая объявляет <STRONG>Recordset2</STRONG> или объект <STRONG><A href="database-object-dao.md">базы данных</A></STRONG> , новую запись удаляется без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-114">In addition, if you close the <STRONG>Recordset2</STRONG> or end the procedure that declares the <STRONG>Recordset2</STRONG> or its <STRONG><A href="database-object-dao.md">Database</A></STRONG> object, the new record is discarded without warning.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="a7b0a-115">При использовании <STRONG>AddNew</STRONG> в рабочей области Microsoft Access и имеет ядро базы данных для создания новой страницы для хранения текущей записи, блокировка страницы жесткой.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-115">When you use <STRONG>AddNew</STRONG> in a Microsoft Access workspace and the database engine has to create a new page to hold the current record, page locking is pessimistic.</span></span> <span data-ttu-id="a7b0a-116">Если новую запись помещается в существующей страницы, страницы блокировки оптимистичный.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-116">If the new record fits in an existing page, page locking is optimistic.</span></span></P>



<span data-ttu-id="a7b0a-117">Если запись вашего **Recordset2**еще не перемещен к последнему, записи, добавленные базовые таблицы для других процессов могут быть включены, если они размещены за пределы текущей записи.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-117">If you haven't moved to the last record of your **Recordset2**, records added to base tables by other processes may be included if they are positioned beyond the current record.</span></span> <span data-ttu-id="a7b0a-118">При добавлении записи для собственного **Recordset2**тем не менее, запись будет отображаться в **Recordset2** и включенных в базовой таблице, где он становится видимым для всех новых объектов **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="a7b0a-118">If you add a record to your own **Recordset2**, however, the record is visible in the **Recordset2** and included in the underlying table where it becomes visible to any new **Recordset2** objects.</span></span>

<span data-ttu-id="a7b0a-119">Положение новую запись зависит от типа **Recordset2**.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-119">The position of the new record depends on the type of **Recordset2**:</span></span>

  - <span data-ttu-id="a7b0a-120">В объекте **Recordset2** добавляющий записи вставляется в конце **набора записей**, независимо от того, сортировки или упорядочивания правил, которые использовались при открытии **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a7b0a-120">In a dynaset-type **Recordset2** object, records are inserted at the end of the **Recordset**, regardless of any sorting or ordering rules that were in effect when the **Recordset** was opened.</span></span>

  - <span data-ttu-id="a7b0a-121">В объекте **Recordset2** тип таблицы, чьи свойства **[индекса](recordset2-index-property-dao.md)** возвращаются записи в их местом в порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-121">In a table-type **Recordset2** object whose **[Index](recordset2-index-property-dao.md)** property has been set, records are returned in their proper place in the sort order.</span></span> <span data-ttu-id="a7b0a-122">Если вы еще не настроили свойство **Index** , новые записи возвращаются в конце **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-122">If you haven't set the **Index** property, new records are returned at the end of the **Recordset**.</span></span>

<span data-ttu-id="a7b0a-123">Записи, которая была текущей, прежде чем использовать **AddNew** остается текущей.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-123">The record that was current before you used **AddNew** remains current.</span></span> <span data-ttu-id="a7b0a-124">Если вы хотите сделать новую запись текущей, можно задать свойства **[Bookmark](recordset2-bookmark-property-dao.md)** закладку, определяемую средством настройки свойства **[LastModified](recordset2-lastmodified-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="a7b0a-124">If you want to make the new record current, you can set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to the bookmark identified by the **[LastModified](recordset2-lastmodified-property-dao.md)** property setting.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a7b0a-125">Чтобы добавить, изменить или удалить записи, должен существовать уникальный индекс на запись в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-125">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="a7b0a-126">В противном случае ошибку «Отказано в доступе» произойдет на вызов метода <STRONG>AddNew</STRONG>, <STRONG>Удаление</STRONG>или <STRONG>Изменение</STRONG> в рабочей области Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-126">If not, a "Permission denied" error will occur on the <STRONG>AddNew</STRONG>, <STRONG>Delete</STRONG>, or <STRONG>Edit</STRONG> method call in a Microsoft Access workspace.</span></span></P>



## <a name="example"></a><span data-ttu-id="a7b0a-127">Пример</span><span class="sxs-lookup"><span data-stu-id="a7b0a-127">Example</span></span>

<span data-ttu-id="a7b0a-128">В этом примере используется метод **AddNew** , чтобы создать новую запись с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-128">This example uses the **AddNew** method to create a new record with the specified name.</span></span> <span data-ttu-id="a7b0a-129">Функция AddName является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="a7b0a-129">The AddName function is required for this procedure to run.</span></span>

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
