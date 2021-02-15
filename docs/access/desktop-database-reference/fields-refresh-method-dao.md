---
title: Метод Fields.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: d08597d8-bad6-523b-a083-d824f85b64bc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834723(v=office.15)
ms:contentKeyID: 48547844
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09218fae470646ab04ecfb5427004e56183e46ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292512"
---
# <a name="fieldsrefresh-method-dao"></a><span data-ttu-id="ffa7c-102">Метод Fields.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="ffa7c-102">Fields.Refresh method (DAO)</span></span>


<span data-ttu-id="ffa7c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffa7c-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ffa7c-104">Обновляет объекты в указанном уровне, чтобы отразить текущую схему базы данных.</span><span class="sxs-lookup"><span data-stu-id="ffa7c-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa7c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffa7c-105">Syntax</span></span>

<span data-ttu-id="ffa7c-106">*выражение .* Обновление</span><span class="sxs-lookup"><span data-stu-id="ffa7c-106">*expression* .Refresh</span></span>

<span data-ttu-id="ffa7c-107">*выражение*: переменная, представляющая объект **Fields**.</span><span class="sxs-lookup"><span data-stu-id="ffa7c-107">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffa7c-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="ffa7c-108">Remarks</span></span>

<span data-ttu-id="ffa7c-109">Чтобы определить позицию, используемую ядром базы данных Microsoft Access для объектов **Field** в коллекции **Fields** объекта **QueryDef,** **Recordset** или **TableDef,** используйте свойство **OrdinalPosition** каждого объекта **Field.**</span><span class="sxs-lookup"><span data-stu-id="ffa7c-109">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object.</span></span> <span data-ttu-id="ffa7c-110">Изменение свойства **OrdinalPosition** объекта **Field** может не изменять порядок объектов **Field** в коллекции, пока не будет применяться метод **Refresh.**</span><span class="sxs-lookup"><span data-stu-id="ffa7c-110">Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="ffa7c-111">Используйте метод **Refresh** в многомерных средах, в которых другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="ffa7c-111">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="ffa7c-112">Кроме того, может потребоваться использовать его в любых коллекциях, на которые косвенно влияют изменения базы данных.</span><span class="sxs-lookup"><span data-stu-id="ffa7c-112">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="ffa7c-113">Например, при изменении коллекции **Users** может потребоваться обновить коллекцию **Groups** перед ее **использованием.**</span><span class="sxs-lookup"><span data-stu-id="ffa7c-113">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="ffa7c-114">Коллекция заполняется объектами при первом ссылке и не отражает автоматически последующие изменения, внесенные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="ffa7c-114">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="ffa7c-115">Если, скорее всего, другой пользователь изменил коллекцию, используйте метод Refresh в коллекции непосредственно перед тем, как выполнять любую задачу в приложении, предполагая наличие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ffa7c-115">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="ffa7c-116">Это гарантирует, что коллекция будет как можно более новой.</span><span class="sxs-lookup"><span data-stu-id="ffa7c-116">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="ffa7c-117">С другой стороны, использование refresh может привести к излишнему замедлению производительности.</span><span class="sxs-lookup"><span data-stu-id="ffa7c-117">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

## <a name="example"></a><span data-ttu-id="ffa7c-118">Пример</span><span class="sxs-lookup"><span data-stu-id="ffa7c-118">Example</span></span>

<span data-ttu-id="ffa7c-119">В этом примере метод **Refresh** используется для обновления коллекции **Fields** таблицы Categories на основе изменений **данных OrdinalPosition.**</span><span class="sxs-lookup"><span data-stu-id="ffa7c-119">This example uses the **Refresh** method to update the **Fields** collection of the Categories table based on changes to the **OrdinalPosition** data.</span></span> <span data-ttu-id="ffa7c-120">Порядок **полей** в коллекции изменяется только после использования метода **Refresh.**</span><span class="sxs-lookup"><span data-stu-id="ffa7c-120">The order of the **Fields** in the collection changes only after the **Refresh** method is used.</span></span>

```vb
    Sub RefreshX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Categories") 
     
     With tdfEmployees 
     ' Display original OrdinalPosition data and store it 
     ' in an array. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldLoop In .Fields 
     fldLoop.OrdinalPosition = _ 
     100 - fldLoop.OrdinalPosition 
     Next fldLoop 
     Set fldLoop = Nothing 
     
     ' Print new data. 
     Debug.Print "New OrdinalPosition data before Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     .Fields.Refresh 
     
     ' Print new data, showing how the field order has been 
     ' changed. 
     Debug.Print "New OrdinalPosition data after Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     ' Restore original OrdinalPosition data. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
