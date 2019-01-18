---
title: Свойство Recordset2.AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: 91ca203f-0c80-67f4-e180-415b6af05030
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197637(v=office.15)
ms:contentKeyID: 48546358
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053074
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4de869866e2aeb28032553be78bee7af16f60402
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716700"
---
# <a name="recordset2absoluteposition-property-dao"></a><span data-ttu-id="6fca1-102">Свойство Recordset2.AbsolutePosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="6fca1-102">Recordset2.AbsolutePosition property (DAO)</span></span>

<span data-ttu-id="6fca1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fca1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6fca1-104">Задает или возвращает относительный номер записи текущего объекта **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="6fca1-104">Sets or returns the relative record number of a **Recordset2** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fca1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fca1-105">Syntax</span></span>

<span data-ttu-id="6fca1-106">*выражение* . AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="6fca1-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="6fca1-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="6fca1-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fca1-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="6fca1-108">Remarks</span></span>

<span data-ttu-id="6fca1-109">Свойство **AbsolutePosition** наведите указатель текущей записи на основании его порядковый номер в объект **Recordset2** добавляющий или моментальный снимок определенную запись.</span><span class="sxs-lookup"><span data-stu-id="6fca1-109">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset2** object.</span></span> <span data-ttu-id="6fca1-110">Также можно определить текущий номер записи, проверив значение свойства **AbsolutePosition** .</span><span class="sxs-lookup"><span data-stu-id="6fca1-110">You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="6fca1-111">Так как значение свойства **AbsolutePosition** с отсчетом от нуля (то есть, значение 0 относится к первой записи в объекте **Recordset2** ), вы не может задать значение больше или равно числу заполненной записей; Благодаря этому перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="6fca1-111">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset2** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error.</span></span> <span data-ttu-id="6fca1-112">Можно определить число заполненной записей в объекте **Recordset2** , проверьте настройки свойства **RecordCount** .</span><span class="sxs-lookup"><span data-stu-id="6fca1-112">You can determine the number of populated records in the **Recordset2** object by checking the **RecordCount** property setting.</span></span> <span data-ttu-id="6fca1-113">Максимальное допустимое свойство **AbsolutePosition** — значение свойства **RecordCount** минус 1.</span><span class="sxs-lookup"><span data-stu-id="6fca1-113">The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="6fca1-114">Если нет текущей записи как при нет записей в объекте **Recordset2** , **AbsolutePosition** возвращает значение – 1.</span><span class="sxs-lookup"><span data-stu-id="6fca1-114">If there is no current record, as when there are no records in the **Recordset2** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="6fca1-115">При удалении текущей записи, значение свойства **AbsolutePosition** не определена и перехватываемые ошибка возникает, если ссылки на него.</span><span class="sxs-lookup"><span data-stu-id="6fca1-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="6fca1-116">Новые записи добавляются в конец последовательности.</span><span class="sxs-lookup"><span data-stu-id="6fca1-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="6fca1-117">Это свойство не следует использовать как номер записи заменяющего.</span><span class="sxs-lookup"><span data-stu-id="6fca1-117">You shouldn't use this property as a surrogate record number.</span></span> <span data-ttu-id="6fca1-118">Закладки будут по-прежнему рекомендуемый способ сохранения и возврата в заданной позиции и являются единственным способом для размещения текущей записи для всех типов объектов **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="6fca1-118">Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset2** objects.</span></span> <span data-ttu-id="6fca1-119">В частности при удалении одной или нескольких записей, перед изменение положения записи.</span><span class="sxs-lookup"><span data-stu-id="6fca1-119">In particular, the position of a record changes when one or more records preceding it are deleted.</span></span> <span data-ttu-id="6fca1-120">Нет также никакой гарантий, что запись будет же абсолютного положения, если повторно объект **Recordset2** создается еще раз, так как порядок отдельных записей в объекте **набора записей** не гарантируется, если он создается с помощью SQL оператор с помощью предложение ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="6fca1-120">There is also no assurance that a record will have the same absolute position if the **Recordset2** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="6fca1-121">Для свойства **AbsolutePosition** значение значение больше нуля в объекте **Recordset2** недавно открытых, но пустые возникает перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="6fca1-121">Setting the **AbsolutePosition** property to a value greater than zero on a newly opened but unpopulated **Recordset2** object causes a trappable error.</span></span> <span data-ttu-id="6fca1-122">Объект **Recordset2** сначала заполняется с помощью метода **MoveLast** .</span><span class="sxs-lookup"><span data-stu-id="6fca1-122">Populate the **Recordset2** object first with the **MoveLast** method.</span></span>
> - <span data-ttu-id="6fca1-123">Свойство **AbsolutePosition** недоступно **Recordset2** прямого — только — тип объектов или объектов **Recordset2** открывается из Транзитные запросы к базам данных ODBC engine подключенной базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6fca1-123">The **AbsolutePosition** property isn't available on forward–only–type **Recordset2** objects, or on **Recordset2** objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span>

## <a name="example"></a><span data-ttu-id="6fca1-124">Пример</span><span class="sxs-lookup"><span data-stu-id="6fca1-124">Example</span></span>

<span data-ttu-id="6fca1-125">В этом примере используется свойство **AbsolutePosition** для отслеживания хода выполнения цикла, который перечисляет все записи **Recordset2**.</span><span class="sxs-lookup"><span data-stu-id="6fca1-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset2**.</span></span>

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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
