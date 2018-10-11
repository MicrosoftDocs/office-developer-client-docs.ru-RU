---
title: TableDef.CreateIndex Method (DAO)
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
ms.openlocfilehash: eee732709c4c10c8e6399d34afafd1b27bf827c1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481853"
---
# <a name="tabledefcreateindex-method-dao"></a><span data-ttu-id="ad4e9-102">TableDef.CreateIndex Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="ad4e9-102">TableDef.CreateIndex Method (DAO)</span></span>


<span data-ttu-id="ad4e9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad4e9-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="ad4e9-104">Создает новый объект **[индекса](index-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="ad4e9-104">Creates a new **[Index](index-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="ad4e9-105">.</span><span class="sxs-lookup"><span data-stu-id="ad4e9-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="ad4e9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad4e9-106">Syntax</span></span>

<span data-ttu-id="ad4e9-107">*выражение* . CreateIndex (***имя***)</span><span class="sxs-lookup"><span data-stu-id="ad4e9-107">*expression* .CreateIndex(***Name***)</span></span>

<span data-ttu-id="ad4e9-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="ad4e9-108">*expression* A variable that represents a **TableDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="ad4e9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad4e9-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad4e9-110">Имя</span><span class="sxs-lookup"><span data-stu-id="ad4e9-110">Name</span></span></p></th>
<th><p><span data-ttu-id="ad4e9-111">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="ad4e9-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ad4e9-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ad4e9-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ad4e9-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ad4e9-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad4e9-114">Имя</span><span class="sxs-lookup"><span data-stu-id="ad4e9-114">Name</span></span></p></td>
<td><p><span data-ttu-id="ad4e9-115">Необязательный</span><span class="sxs-lookup"><span data-stu-id="ad4e9-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="ad4e9-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ad4e9-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ad4e9-117"><strong>Строка</strong> , уникальным образом новый объект <strong>индекса</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad4e9-117">A <strong>String</strong> that uniquely names the new <strong>Index</strong> object.</span></span> <span data-ttu-id="ad4e9-118">Свойство <strong>Name</strong> для получения дополнительных сведений см допустимые имена <strong>индекса</strong> .</span><span class="sxs-lookup"><span data-stu-id="ad4e9-118">See the <strong>Name</strong> property for details on valid <strong>Index</strong> names.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ad4e9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad4e9-119">Return Value</span></span>

<span data-ttu-id="ad4e9-120">Указатель</span><span class="sxs-lookup"><span data-stu-id="ad4e9-120">Index</span></span>

## <a name="remarks"></a><span data-ttu-id="ad4e9-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="ad4e9-121">Remarks</span></span>

<span data-ttu-id="ad4e9-122">Чтобы создать новый объект **индекса** для объекта **TableDef** можно использовать метод **CreateIndex** .</span><span class="sxs-lookup"><span data-stu-id="ad4e9-122">You can use the **CreateIndex** method to create a new **Index** object for a **TableDef** object.</span></span> <span data-ttu-id="ad4e9-123">Если опустить часть необязательное имя при использовании **CreateIndex**, можно использовать соответствующие присваивания установить или сбросить свойство **Name** , прежде чем добавить новый объект в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="ad4e9-123">If you omit the optional name part when you use **CreateIndex**, you can use an appropriate assignment statement to set or reset the **Name** property before you append the new object to a collection.</span></span> <span data-ttu-id="ad4e9-124">После добавления объекта, можно или не может иметь возможность задать его свойство **Name** , в зависимости от типа объекта, который содержит коллекцию **индексов** .</span><span class="sxs-lookup"><span data-stu-id="ad4e9-124">After you append the object, you may or may not be able to set its **Name** property, depending on the type of object that contains the **Indexes** collection.</span></span> <span data-ttu-id="ad4e9-125">В разделе **имя** свойства для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="ad4e9-125">See the **Name** property topic for more details.</span></span>

<span data-ttu-id="ad4e9-126">Если имя ссылается на объект, который уже входит в коллекции, то во время выполнения возникает ошибка при использовании метода **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="ad4e9-126">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="ad4e9-127">Чтобы удалить объект **индекса** из семейства сайтов, используйте метод **[Delete](fields-delete-method-dao.md)** в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="ad4e9-127">To remove an **Index** object from a collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="ad4e9-128">Пример</span><span class="sxs-lookup"><span data-stu-id="ad4e9-128">Example</span></span>

<span data-ttu-id="ad4e9-129">В этом примере используется метод **CreateIndex** для создания двух новых объектов **индекса** и добавляет их в коллекцию **индексов** сотрудников **TableDef** объекта.</span><span class="sxs-lookup"><span data-stu-id="ad4e9-129">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object.</span></span> <span data-ttu-id="ad4e9-130">Затем выполняется перечисление коллекции индексов объекта **TableDef** , коллекции **полей** новых объектов **индекса** и коллекции свойств новых объектов **индекса** .</span><span class="sxs-lookup"><span data-stu-id="ad4e9-130">It then enumerates the Indexes collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects.</span></span> <span data-ttu-id="ad4e9-131">Функция CreateIndexOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="ad4e9-131">The CreateIndexOutput function is required for this procedure to run.</span></span>

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
