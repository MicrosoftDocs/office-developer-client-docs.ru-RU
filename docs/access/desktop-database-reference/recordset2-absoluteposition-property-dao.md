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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307513"
---
# <a name="recordset2absoluteposition-property-dao"></a><span data-ttu-id="bcf80-102">Свойство Recordset2.AbsolutePosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="bcf80-102">Recordset2.AbsolutePosition property (DAO)</span></span>

<span data-ttu-id="bcf80-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bcf80-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bcf80-104">Задает или возвращает относительное рекордное число текущей записи объекта **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="bcf80-104">Sets or returns the relative record number of a **Recordset2** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcf80-105">Syntax</span></span>

<span data-ttu-id="bcf80-106">*expression* .AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="bcf80-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="bcf80-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="bcf80-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf80-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="bcf80-108">Remarks</span></span>

<span data-ttu-id="bcf80-109">Свойство **AbsolutePosition** можно использовать для расположения текущего указателя записи к определенной записи в зависимости от его расположения в объекте Recordset или типа снимков **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="bcf80-109">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset2** object.</span></span> <span data-ttu-id="bcf80-110">Вы также можете определить текущий номер записи с помощью настройки свойства **AbsolutePosition**.</span><span class="sxs-lookup"><span data-stu-id="bcf80-110">You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="bcf80-111">Так как значение **свойства AbsolutePosition** равно нулю (т. е. параметр 0 относится к первой записи объекта **Recordset2),** нельзя установить его значение, большее или равное количеству населенных записей; это приводит к ошибке, которая может быть заблокирована.</span><span class="sxs-lookup"><span data-stu-id="bcf80-111">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset2** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error.</span></span> <span data-ttu-id="bcf80-112">Количество населенных записей в объекте **Recordset2** можно определить, проверив параметр **свойства RecordCount.**</span><span class="sxs-lookup"><span data-stu-id="bcf80-112">You can determine the number of populated records in the **Recordset2** object by checking the **RecordCount** property setting.</span></span> <span data-ttu-id="bcf80-113">Максимально допустимое значение для свойства **AbsolutePosition** –значение свойства **RecordCount** минус 1.</span><span class="sxs-lookup"><span data-stu-id="bcf80-113">The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="bcf80-114">Если нет текущей записи, как если в объекте **Recordset2** нет записей, **AbsolutePosition** возвращается —1.</span><span class="sxs-lookup"><span data-stu-id="bcf80-114">If there is no current record, as when there are no records in the **Recordset2** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="bcf80-115">При удалении текущей записи, значение свойства **AbsolutePosition** не определяется, а перехватываемая ошибка возникает, если сослаться на него.</span><span class="sxs-lookup"><span data-stu-id="bcf80-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="bcf80-116">Новые записи будут добавлены в конец последовательности.</span><span class="sxs-lookup"><span data-stu-id="bcf80-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="bcf80-117">Не следует использовать это свойство в качестве замены номеру записи.</span><span class="sxs-lookup"><span data-stu-id="bcf80-117">You shouldn't use this property as a surrogate record number.</span></span> <span data-ttu-id="bcf80-118">Закладки по-прежнему являются рекомендуемой возможностью сохранения и возвращения в заданную позицию и единственным способом расположить текущую запись во всех типах объектов **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="bcf80-118">Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset2** objects.</span></span> <span data-ttu-id="bcf80-119">В частности положение запись изменяется при удалении одной или нескольких записей, расположенных перед ней.</span><span class="sxs-lookup"><span data-stu-id="bcf80-119">In particular, the position of a record changes when one or more records preceding it are deleted.</span></span> <span data-ttu-id="bcf80-120">Нет также уверенности в том, что запись будет иметь ту же абсолютную позицию, если объект **Recordset2** будет повторно создан, так как порядок отдельных записей в объекте **Recordset** не гарантируется, если он не создан с помощью SQL с помощью пункта ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="bcf80-120">There is also no assurance that a record will have the same absolute position if the **Recordset2** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="bcf80-121">Настройка свойства **AbsolutePosition** к значению больше нуля для недавно открытого, но незаселенного объекта **Recordset2** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="bcf80-121">Setting the **AbsolutePosition** property to a value greater than zero on a newly opened but unpopulated **Recordset2** object causes a trappable error.</span></span> <span data-ttu-id="bcf80-122">Сначала заполнять **объект Recordset2** методом **MoveLast.**</span><span class="sxs-lookup"><span data-stu-id="bcf80-122">Populate the **Recordset2** object first with the **MoveLast** method.</span></span>
> - <span data-ttu-id="bcf80-123">Свойство **AbsolutePosition** не доступно для объектов **Recordset2** только для форвардного типа или для объектов **Recordset2,** открытых из сквозных запросов в базах данных базы данных Microsoft Access, подключенных к базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="bcf80-123">The **AbsolutePosition** property isn't available on forward–only–type **Recordset2** objects, or on **Recordset2** objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span>

## <a name="example"></a><span data-ttu-id="bcf80-124">Пример</span><span class="sxs-lookup"><span data-stu-id="bcf80-124">Example</span></span>

<span data-ttu-id="bcf80-125">В этом примере свойство **AbsolutePosition** используется для отслеживания хода цикла, который регистрирует все записи **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="bcf80-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset2**.</span></span>

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
