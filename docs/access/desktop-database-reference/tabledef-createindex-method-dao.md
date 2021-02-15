---
title: Метод TableDef.CreateIndex (DAO)
TOCTitle: CreateIndex Method
ms:assetid: 857b25c1-01fa-b926-0c74-7105e71b7505
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196791(v=office.15)
ms:contentKeyID: 48546062
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052970
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: baa82b659cc2260d4a003c644b2d03d6c897fd21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314373"
---
# <a name="tabledefcreateindex-method-dao"></a><span data-ttu-id="0ed77-102">Метод TableDef.CreateIndex (DAO)</span><span class="sxs-lookup"><span data-stu-id="0ed77-102">TableDef.CreateIndex method (DAO)</span></span>

<span data-ttu-id="0ed77-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ed77-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="0ed77-104">Создает новый объект **[Index](index-object-dao.md)** (только для рабочих пространств Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0ed77-104">Creates a new **[Index](index-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="0ed77-105">.</span><span class="sxs-lookup"><span data-stu-id="0ed77-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed77-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ed77-106">Syntax</span></span>

<span data-ttu-id="0ed77-107">*выражение .* CreateIndex(***Name***)</span><span class="sxs-lookup"><span data-stu-id="0ed77-107">*expression* .CreateIndex(***Name***)</span></span>

<span data-ttu-id="0ed77-108">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="0ed77-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ed77-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ed77-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ed77-110">Имя</span><span class="sxs-lookup"><span data-stu-id="0ed77-110">Name</span></span></p></th>
<th><p><span data-ttu-id="0ed77-111">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="0ed77-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="0ed77-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0ed77-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="0ed77-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0ed77-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ed77-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="0ed77-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="0ed77-115">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="0ed77-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="0ed77-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0ed77-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0ed77-117"><strong>Строка,</strong> однозначно именовав новый <strong>объект Index.</strong></span><span class="sxs-lookup"><span data-stu-id="0ed77-117">A <strong>String</strong> that uniquely names the new <strong>Index</strong> object.</span></span> <span data-ttu-id="0ed77-118">Сведения о <strong>допустимом</strong> имени индекса см. в свойстве <strong>Name.</strong></span><span class="sxs-lookup"><span data-stu-id="0ed77-118">See the <strong>Name</strong> property for details on valid <strong>Index</strong> names.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="0ed77-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ed77-119">Return value</span></span>

<span data-ttu-id="0ed77-120">Index</span><span class="sxs-lookup"><span data-stu-id="0ed77-120">Index</span></span>

## <a name="remarks"></a><span data-ttu-id="0ed77-121">Заметки</span><span class="sxs-lookup"><span data-stu-id="0ed77-121">Remarks</span></span>

<span data-ttu-id="0ed77-122">С помощью метода **CreateIndex** можно создать новый объект **Index** для **объекта TableDef.**</span><span class="sxs-lookup"><span data-stu-id="0ed77-122">You can use the **CreateIndex** method to create a new **Index** object for a **TableDef** object.</span></span> <span data-ttu-id="0ed77-123">Если опустить необязательные части имени при использовании **CreateIndex,** можно использовать соответствующий отчет о назначении, чтобы установить или сбросить свойство **Name** перед тем, как приместь новый объект в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="0ed77-123">If you omit the optional name part when you use **CreateIndex**, you can use an appropriate assignment statement to set or reset the **Name** property before you append the new object to a collection.</span></span> <span data-ttu-id="0ed77-124">После того как вы добавили объект, вы можете или не сможете установить его свойство **Name** в зависимости от типа объекта, который содержит **коллекцию Indexes.**</span><span class="sxs-lookup"><span data-stu-id="0ed77-124">After you append the object, you may or may not be able to set its **Name** property, depending on the type of object that contains the **Indexes** collection.</span></span> <span data-ttu-id="0ed77-125">Дополнительные **сведения см.** в разделе о свойстве Name.</span><span class="sxs-lookup"><span data-stu-id="0ed77-125">See the **Name** property topic for more details.</span></span>

<span data-ttu-id="0ed77-126">Если имя ссылается на объект, который уже является членом коллекции, при использовании метода **[Append](fields-append-method-dao.md)** возникает ошибка во время работы.</span><span class="sxs-lookup"><span data-stu-id="0ed77-126">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="0ed77-127">Чтобы удалить **объект Index** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="0ed77-127">To remove an **Index** object from a collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="0ed77-128">Пример</span><span class="sxs-lookup"><span data-stu-id="0ed77-128">Example</span></span>

<span data-ttu-id="0ed77-129">В этом примере метод **CreateIndex** используется для создания двух новых объектов **Index,** а затем их можно придать коллекции **Indexes** объекта Employees **TableDef.**</span><span class="sxs-lookup"><span data-stu-id="0ed77-129">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object.</span></span> <span data-ttu-id="0ed77-130">Затем он нумерирует коллекцию Indexes объекта **TableDef,** коллекцию **Fields** новых объектов **Index** и коллекцию свойств новых объектов **Index.**</span><span class="sxs-lookup"><span data-stu-id="0ed77-130">It then enumerates the Indexes collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects.</span></span> <span data-ttu-id="0ed77-131">Для запуска этой процедуры требуется функция CreateIndexOutput.</span><span class="sxs-lookup"><span data-stu-id="0ed77-131">The CreateIndexOutput function is required for this procedure to run.</span></span>

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
