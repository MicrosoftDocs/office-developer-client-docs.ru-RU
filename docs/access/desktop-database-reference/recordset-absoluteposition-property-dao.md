---
title: Свойство Recordset.AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 22284abf537f57d98d5f0416b58a9a2ac3c6ebe5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702506"
---
# <a name="recordsetabsoluteposition-property-dao"></a><span data-ttu-id="a1349-102">Свойство Recordset.AbsolutePosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="a1349-102">Recordset.AbsolutePosition Property (DAO)</span></span>

<span data-ttu-id="a1349-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1349-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1349-104">Задает или возвращает относительный номер записи объекта **Recordset** текущей записи.</span><span class="sxs-lookup"><span data-stu-id="a1349-104">Sets or returns the relative record number of a **Recordset** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1349-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1349-105">Syntax</span></span>

<span data-ttu-id="a1349-106">*expression* .AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="a1349-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="a1349-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a1349-107">*expression* A variable that represents a **FileDialog** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1349-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1349-108">Remarks</span></span>

<span data-ttu-id="a1349-109">Вы можете использовать свойство **AbsolutePosition**, чтобы расположить указатель текущей записи на определенной записи с учетом его порядкового положения в объекте **Recordset** типа dynaset или моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="a1349-109">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset** object.</span></span> <span data-ttu-id="a1349-110">Вы также можете определить текущий номер записи с помощью настройки свойства **AbsolutePosition**.</span><span class="sxs-lookup"><span data-stu-id="a1349-110">You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="a1349-111">Так как значение свойства **AbsolutePosition** опирается на ноль (то есть установка значения 0 указывает на первую запись объекта **Recordset**), вы не можете установить значение, которые больше или равно количеству заполненных записей, так как это вызывает перехватываемую ошибку.</span><span class="sxs-lookup"><span data-stu-id="a1349-111">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error.</span></span> <span data-ttu-id="a1349-112">Вы можете определить количество заполненных записей в объекте **Recordset** путем проверки настройки свойства **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="a1349-112">You can determine the number of populated records in the **Recordset** object by checking the **RecordCount** property setting.</span></span> <span data-ttu-id="a1349-113">Максимально допустимое значение для свойства **AbsolutePosition** –значение свойства **RecordCount** минус 1.</span><span class="sxs-lookup"><span data-stu-id="a1349-113">The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="a1349-114">При отсутствии текущей записи, например, когда в объекте **Recordset** нет записей, **AbsolutePosition** возвращает -1.</span><span class="sxs-lookup"><span data-stu-id="a1349-114">If there is no current record, as when there are no records in the **Recordset** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="a1349-115">При удалении текущей записи, значение свойства **AbsolutePosition** не определяется, а перехватываемая ошибка возникает, если сослаться на него.</span><span class="sxs-lookup"><span data-stu-id="a1349-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="a1349-116">Новые записи будут добавлены в конец последовательности.</span><span class="sxs-lookup"><span data-stu-id="a1349-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="a1349-117">Не следует использовать это свойство в качестве замены номеру записи.</span><span class="sxs-lookup"><span data-stu-id="a1349-117">You shouldn't use this property as a surrogate record number.</span></span> <span data-ttu-id="a1349-118">Закладки по-прежнему являются рекомендуемым методом сохранения и возврата к заданному положению и — единственным способом расположения текущей записи для всех типов объектов **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a1349-118">Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset** objects.</span></span> <span data-ttu-id="a1349-119">В частности положение запись изменяется при удалении одной или нескольких записей, расположенных перед ней.</span><span class="sxs-lookup"><span data-stu-id="a1349-119">In particular, the position of a record changes when one or more records preceding it are deleted.</span></span> <span data-ttu-id="a1349-120">Кроме того, нет гарантий, что запись будет иметь такое же абсолютное положение, если объект **Recordset** будет создан повторно, так как порядок отдельных записей в пределах объекта **Recordset** не гарантируется, если он не создан с помощью оператора SQL, который включает в себя предложение ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="a1349-120">There is also no assurance that a record will have the same absolute position if the **Recordset** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="a1349-121">Настройка свойства **AbsolutePosition** со значением больше нуля для только что открытого, но не заполненного объекта **Recordset** вызывает перехватываемую ошибку.</span><span class="sxs-lookup"><span data-stu-id="a1349-121">Setting the **AbsolutePosition** property to a value greater than zero on a newly opened but unpopulated **Recordset** object causes a trappable error.</span></span> <span data-ttu-id="a1349-122">Сначала заполните объект **Recordset** с помощью метода **MoveLast**.</span><span class="sxs-lookup"><span data-stu-id="a1349-122">Populate the **Recordset** object first with the **MoveLast** method.</span></span>
> - <span data-ttu-id="a1349-123">Свойство **AbsolutePosition** не поддерживается для объекта **Recordset** однонаправленного типа или для объектов **Recordset**, открытых через запрос к серверу для базы данных ODBC, подключенной к ядру СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a1349-123">The **AbsolutePosition** property isn't available on forward–only–type **Recordset** objects, or on **Recordset** objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span>

## <a name="example"></a><span data-ttu-id="a1349-124">Пример</span><span class="sxs-lookup"><span data-stu-id="a1349-124">Example</span></span>

<span data-ttu-id="a1349-125">В этом примере используется свойство **AbsolutePosition** для отслеживания хода выполнения цикла, который перечисляет все записи в **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a1349-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset**.</span></span>

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
