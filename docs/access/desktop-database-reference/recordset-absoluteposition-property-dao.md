---
title: Recordset.AbsolutePosition Property (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c13dc234fc70d8cf5e9b14958b5336c39a6a4d7a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886510"
---
# <a name="recordsetabsoluteposition-property-dao"></a><span data-ttu-id="98352-102">Recordset.AbsolutePosition Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="98352-102">Recordset.AbsolutePosition Property (DAO)</span></span>

<span data-ttu-id="98352-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98352-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98352-104">Задает или возвращает относительный номер записи текущего объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="98352-104">Sets or returns the relative record number of a **Recordset** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="98352-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98352-105">Syntax</span></span>

<span data-ttu-id="98352-106">*выражение* . AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="98352-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="98352-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="98352-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="98352-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="98352-108">Remarks</span></span>

<span data-ttu-id="98352-109">Свойство **AbsolutePosition** наведите указатель текущей записи для конкретных записей по его порядковый номер в объект **набора записей** добавляющий или моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="98352-109">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset** object.</span></span> <span data-ttu-id="98352-110">Также можно определить текущий номер записи, проверив значение свойства **AbsolutePosition** .</span><span class="sxs-lookup"><span data-stu-id="98352-110">You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="98352-111">Так как значение свойства **AbsolutePosition** с отсчетом от нуля (то есть, значение 0 относится к первой записи в объекте **набора записей** ), вы не может задать значение больше или равно числу заполненной записей; Благодаря этому перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="98352-111">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error.</span></span> <span data-ttu-id="98352-112">Можно определить число заполненной записей в объекте **набора записей** , проверьте настройки свойства **RecordCount** .</span><span class="sxs-lookup"><span data-stu-id="98352-112">You can determine the number of populated records in the **Recordset** object by checking the **RecordCount** property setting.</span></span> <span data-ttu-id="98352-113">Максимальное допустимое свойство **AbsolutePosition** — значение свойства **RecordCount** минус 1.</span><span class="sxs-lookup"><span data-stu-id="98352-113">The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="98352-114">Если нет текущей записи как при нет записей в объекте **набора записей** , **AbsolutePosition** возвращает значение – 1.</span><span class="sxs-lookup"><span data-stu-id="98352-114">If there is no current record, as when there are no records in the **Recordset** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="98352-115">При удалении текущей записи, значение свойства **AbsolutePosition** не определена и перехватываемые ошибка возникает, если ссылки на него.</span><span class="sxs-lookup"><span data-stu-id="98352-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="98352-116">Новые записи добавляются в конец последовательности.</span><span class="sxs-lookup"><span data-stu-id="98352-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="98352-117">Это свойство не следует использовать как номер записи заменяющего.</span><span class="sxs-lookup"><span data-stu-id="98352-117">You shouldn't use this property as a surrogate record number.</span></span> <span data-ttu-id="98352-118">Закладки будут по-прежнему рекомендуемый способ сохранения и возврата в заданной позиции и являются единственным способом для размещения текущей записи для всех типов объектов **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="98352-118">Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset** objects.</span></span> <span data-ttu-id="98352-119">В частности при удалении одной или нескольких записей, перед изменение положения записи.</span><span class="sxs-lookup"><span data-stu-id="98352-119">In particular, the position of a record changes when one or more records preceding it are deleted.</span></span> <span data-ttu-id="98352-120">Нет также никакой гарантий, что запись будет же абсолютного положения, если повторно объекта **набора записей** создается еще раз, так как порядок отдельных записей в объекте **набора записей** не гарантируется, если он создается с помощью инструкции SQL с помощью предложение ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="98352-120">There is also no assurance that a record will have the same absolute position if the **Recordset** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="98352-121">Для свойства **AbsolutePosition** значение значение больше нуля на вновь открыт, но пустые объекта **набора записей** происходит перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="98352-121">Setting the **AbsolutePosition** property to a value greater than zero on a newly opened but unpopulated **Recordset** object causes a trappable error.</span></span> <span data-ttu-id="98352-122">Сначала заполнения объекта **набора записей** с помощью метода **MoveLast** .</span><span class="sxs-lookup"><span data-stu-id="98352-122">Populate the **Recordset** object first with the **MoveLast** method.</span></span>
> - <span data-ttu-id="98352-123">Свойство **AbsolutePosition** недоступно прямого — только — тип объектов **наборов записей** , либо на объекты **набора записей** из Транзитные запросы к базам данных ODBC engine подключенной базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="98352-123">The **AbsolutePosition** property isn't available on forward–only–type **Recordset** objects, or on **Recordset** objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span>

## <a name="example"></a><span data-ttu-id="98352-124">Пример</span><span class="sxs-lookup"><span data-stu-id="98352-124">Example</span></span>

<span data-ttu-id="98352-125">В этом примере используется свойство **AbsolutePosition** для отслеживания хода выполнения цикла, который перечисляет все записи из **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="98352-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset**.</span></span>

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
