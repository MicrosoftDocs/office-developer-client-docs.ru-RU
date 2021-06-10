---
title: Метод Database.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: f2039be9-5fd8-f673-dfbf-0a71540cdc98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836607(v=office.15)
ms:contentKeyID: 48548638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f966e041a6d2aff773f6c3849c0846ef362d1142
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294976"
---
# <a name="databasecreateproperty-method-dao"></a><span data-ttu-id="20b31-102">Метод Database.CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="20b31-102">Database.CreateProperty method (DAO)</span></span>

<span data-ttu-id="20b31-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20b31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20b31-104">Создает новый объект Свойства, определенный **[пользователем](property-object-dao.md)** (только рабочие пространства Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="20b31-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="20b31-105">.</span><span class="sxs-lookup"><span data-stu-id="20b31-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b31-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20b31-106">Syntax</span></span>

<span data-ttu-id="20b31-107">*выражения* . CreateProperty(Имя , ***Тип***, ***Значение***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="20b31-107">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="20b31-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="20b31-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="20b31-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="20b31-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20b31-110">Имя</span><span class="sxs-lookup"><span data-stu-id="20b31-110">Name</span></span></p></th>
<th><p><span data-ttu-id="20b31-111">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="20b31-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="20b31-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="20b31-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="20b31-113">Описание</span><span class="sxs-lookup"><span data-stu-id="20b31-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20b31-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="20b31-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="20b31-115">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="20b31-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="20b31-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="20b31-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="20b31-117"><strong>Строка,</strong> уникально именуемая новым <strong>объектом Свойства.</strong></span><span class="sxs-lookup"><span data-stu-id="20b31-117">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="20b31-118">Сведения о <strong>допустимом</strong> имени свойства см. в свойстве <strong>Name.</strong></span><span class="sxs-lookup"><span data-stu-id="20b31-118">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20b31-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="20b31-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="20b31-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="20b31-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="20b31-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="20b31-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="20b31-122">Константа, определяемая типом данных нового объекта <strong>Property.</strong></span><span class="sxs-lookup"><span data-stu-id="20b31-122">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="20b31-123">Допустимые типы данных см. в свойстве <strong><a href="field-type-property-dao.md">Type</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="20b31-123">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20b31-124"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="20b31-124"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="20b31-125">Необязательный</span><span class="sxs-lookup"><span data-stu-id="20b31-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="20b31-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="20b31-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="20b31-127"><strong>Вариант,</strong> содержащий начальное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="20b31-127">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="20b31-128">Сведения <strong><a href="field-value-property-dao.md">см.</a></strong> в свойстве Value.</span><span class="sxs-lookup"><span data-stu-id="20b31-128">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20b31-129"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="20b31-129"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="20b31-130">Необязательный</span><span class="sxs-lookup"><span data-stu-id="20b31-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="20b31-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="20b31-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="20b31-132"><strong>Подтип</strong> <strong>Variant (Boolean),</strong> который указывает, является ли <strong>свойство</strong> объектом DDL.</span><span class="sxs-lookup"><span data-stu-id="20b31-132">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="20b31-133">Значение по умолчанию - false.</span><span class="sxs-lookup"><span data-stu-id="20b31-133">The default is False.</span></span> <span data-ttu-id="20b31-134">Если DDL является true, пользователи не могут изменить или удалить этот объект <strong>Property,</strong> если у них нет разрешения dbSecWriteDef.</span><span class="sxs-lookup"><span data-stu-id="20b31-134">If DDL is True, users can't change or delete this <strong>Property</strong> object unless they have dbSecWriteDef permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="20b31-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20b31-135">Return value</span></span>

<span data-ttu-id="20b31-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="20b31-136">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="20b31-137">Примечания</span><span class="sxs-lookup"><span data-stu-id="20b31-137">Remarks</span></span>

<span data-ttu-id="20b31-138">Вы можете создать объект **Свойства,** определенный пользователем, только в коллекции **[Свойств](properties-collection-dao.md)** сохраняемого объекта.</span><span class="sxs-lookup"><span data-stu-id="20b31-138">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="20b31-139">Если при использовании **CreateProperty** вы опустить одну или несколько необязательных частей, можно использовать соответствующее заявление о назначении, чтобы задать или сбросить соответствующее свойство, прежде чем примкнуть новый объект к коллекции.</span><span class="sxs-lookup"><span data-stu-id="20b31-139">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="20b31-140">После приложения объекта можно изменить некоторые параметры свойств, но не все.</span><span class="sxs-lookup"><span data-stu-id="20b31-140">After you append the object, you can alter some but not all of its property settings.</span></span> <span data-ttu-id="20b31-141">Дополнительные сведения см. в разделы **Имя,** **Тип** и **Значение** свойств.</span><span class="sxs-lookup"><span data-stu-id="20b31-141">See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="20b31-142">Если имя относится к объекту, который уже входит в коллекцию, при использовании метода **[Append](fields-append-method-dao.md)** возникает ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="20b31-142">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="20b31-143">Чтобы удалить определенный пользователем **объект Property** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции **Свойств.**</span><span class="sxs-lookup"><span data-stu-id="20b31-143">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection.</span></span> <span data-ttu-id="20b31-144">Вы не можете удалить встроенные свойства.</span><span class="sxs-lookup"><span data-stu-id="20b31-144">You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="20b31-145">Если упустить аргумент DDL, он по умолчанию будет ложным (не-DDL).</span><span class="sxs-lookup"><span data-stu-id="20b31-145">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="20b31-146">Поскольку соответствующее свойство DDL не подвергается воздействию, необходимо удалить и повторно создать объект **Property,** который необходимо изменить с DDL на non-DDL.</span><span class="sxs-lookup"><span data-stu-id="20b31-146">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


## <a name="example"></a><span data-ttu-id="20b31-147">Пример</span><span class="sxs-lookup"><span data-stu-id="20b31-147">Example</span></span>

<span data-ttu-id="20b31-148">В этом примере попытается задать значение свойства, определяемого пользователем.</span><span class="sxs-lookup"><span data-stu-id="20b31-148">This example tries to set the value of a user-defined property.</span></span> <span data-ttu-id="20b31-149">Если свойство не существует, он использует метод **CreateProperty** для создания и набора значения нового свойства.</span><span class="sxs-lookup"><span data-stu-id="20b31-149">If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property.</span></span> <span data-ttu-id="20b31-150">Для запуска этой процедуры требуется процедура SetProperty.</span><span class="sxs-lookup"><span data-stu-id="20b31-150">The SetProperty procedure is required for this procedure to run.</span></span>

```vb
    Sub CreatePropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Set the Archive property to True. 
       SetProperty dbsNorthwind, "Archive", True 
        
       With dbsNorthwind 
          Debug.Print "Properties of " & .Name 
           
          ' Enumerate Properties collection of the Northwind  
          ' database. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
     
          ' Delete the new property since this is a  
          ' demonstration. 
          .Properties.Delete "Archive" 
     
          .Close 
       End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
       booTemp As Boolean) 
     
       Dim prpNew As Property 
       Dim errLoop As Error 
     
       ' Attempt to set the specified property. 
       On Error GoTo Err_Property 
       dbsTemp.Properties("strName") = booTemp 
       On Error GoTo 0 
     
       Exit Sub 
     
    Err_Property: 
     
       ' Error 3270 means that the property was not found. 
       If DBEngine.Errors(0).Number = 3270 Then 
          ' Create property, set its value, and append it to the  
          ' Properties collection. 
          Set prpNew = dbsTemp.CreateProperty(strName, _ 
             dbBoolean, booTemp) 
          dbsTemp.Properties.Append prpNew 
          Resume Next 
       Else 
          ' If different error has occurred, display message. 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
          End 
       End If 
     
    End Sub
```
