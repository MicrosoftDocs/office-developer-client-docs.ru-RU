---
title: Fields.Refresh Method (DAO)
TOCTitle: Refresh Method
ms:assetid: d08597d8-bad6-523b-a083-d824f85b64bc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834723(v=office.15)
ms:contentKeyID: 48547844
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1804585f3c3bc4a796da00dfede5a482d65a82a1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889618"
---
# <a name="fieldsrefresh-method-dao"></a><span data-ttu-id="8bd19-102">Fields.Refresh Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="8bd19-102">Fields.Refresh Method (DAO)</span></span>


<span data-ttu-id="8bd19-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bd19-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="8bd19-104">Обновляет объекты в указанном включающий в соответствии с текущей схеме базы данных.</span><span class="sxs-lookup"><span data-stu-id="8bd19-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bd19-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bd19-105">Syntax</span></span>

<span data-ttu-id="8bd19-106">*выражение* . Обновление</span><span class="sxs-lookup"><span data-stu-id="8bd19-106">*expression* .Refresh</span></span>

<span data-ttu-id="8bd19-107">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="8bd19-107">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bd19-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="8bd19-108">Remarks</span></span>

<span data-ttu-id="8bd19-109">Чтобы определить позицию, ядро базы данных Microsoft Access с помощью **поля** объектов в коллекции **полей** **QueryDef**, **набора записей**или **TableDef** объекта, используйте свойство **OrdinalPosition** Каждый объект **поля** .</span><span class="sxs-lookup"><span data-stu-id="8bd19-109">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object.</span></span> <span data-ttu-id="8bd19-110">Изменение свойства **OrdinalPosition** объекта **поля** могут не изменить порядок **полей** объектов в коллекции только при вызове метода **обновления на**</span><span class="sxs-lookup"><span data-stu-id="8bd19-110">Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="8bd19-111">Используйте метод **Refresh** в многопользовательских средах, в которых другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="8bd19-111">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="8bd19-112">Кроме того, может потребоваться использовать на всех коллекций, которые косвенно затронуты изменениями в базе данных.</span><span class="sxs-lookup"><span data-stu-id="8bd19-112">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="8bd19-113">Например при изменении коллекции **пользователей** может потребоваться обновить коллекцию **групп** перед использованием семейства сайтов **групп** .</span><span class="sxs-lookup"><span data-stu-id="8bd19-113">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="8bd19-114">Объекты в первый раз оно используется для ссылки и не отражает изменения, которые другие пользователи автоматически заполняется коллекцию.</span><span class="sxs-lookup"><span data-stu-id="8bd19-114">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="8bd19-115">Если это скорее всего, что другой пользователь был изменен коллекцию, используйте метод Refresh в семействе сайтов непосредственно перед выполнению любой из задач в приложения, которые предполагается наличие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="8bd19-115">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="8bd19-116">Это гарантирует, что коллекции с самым последним обновлением.</span><span class="sxs-lookup"><span data-stu-id="8bd19-116">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="8bd19-117">С другой стороны с помощью обновления без необходимости может снизить производительность.</span><span class="sxs-lookup"><span data-stu-id="8bd19-117">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

## <a name="example"></a><span data-ttu-id="8bd19-118">Пример</span><span class="sxs-lookup"><span data-stu-id="8bd19-118">Example</span></span>

<span data-ttu-id="8bd19-119">В этом примере используется метод **Refresh** для обновления коллекции **полей** на основании изменений в данные **OrdinalPosition** таблицы категорий.</span><span class="sxs-lookup"><span data-stu-id="8bd19-119">This example uses the **Refresh** method to update the **Fields** collection of the Categories table based on changes to the **OrdinalPosition** data.</span></span> <span data-ttu-id="8bd19-120">Порядок **полей** в коллекции изменения только после используется метод **Refresh** .</span><span class="sxs-lookup"><span data-stu-id="8bd19-120">The order of the **Fields** in the collection changes only after the **Refresh** method is used.</span></span>

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
