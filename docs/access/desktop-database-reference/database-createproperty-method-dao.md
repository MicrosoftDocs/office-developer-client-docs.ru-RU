---
title: Database.CreateProperty Method (DAO)
TOCTitle: CreateProperty Method
ms:assetid: f2039be9-5fd8-f673-dfbf-0a71540cdc98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836607(v=office.15)
ms:contentKeyID: 48548638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2f7e405410f19178a7f4845cf95fcb6e980adeb9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479804"
---
# <a name="databasecreateproperty-method-dao"></a><span data-ttu-id="62a2a-102">Database.CreateProperty Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="62a2a-102">Database.CreateProperty Method (DAO)</span></span>


<span data-ttu-id="62a2a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="62a2a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="62a2a-104">Создание пользовательских **[свойств](property-object-dao.md)** объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="62a2a-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="62a2a-105">.</span><span class="sxs-lookup"><span data-stu-id="62a2a-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="62a2a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62a2a-106">Syntax</span></span>

<span data-ttu-id="62a2a-107">*выражение* . CreateProperty (***имя***, ***Тип***, ***значение***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="62a2a-107">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="62a2a-108">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="62a2a-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="62a2a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="62a2a-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="62a2a-110">Имя</span><span class="sxs-lookup"><span data-stu-id="62a2a-110">Name</span></span></p></th>
<th><p><span data-ttu-id="62a2a-111">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="62a2a-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="62a2a-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="62a2a-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="62a2a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="62a2a-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62a2a-114">Имя</span><span class="sxs-lookup"><span data-stu-id="62a2a-114">Name</span></span></p></td>
<td><p><span data-ttu-id="62a2a-115">Необязательный</span><span class="sxs-lookup"><span data-stu-id="62a2a-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="62a2a-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="62a2a-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="62a2a-117"><strong>Строка</strong> , уникальным образом новый объект <strong>свойство</strong> .</span><span class="sxs-lookup"><span data-stu-id="62a2a-117">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="62a2a-118">Свойство <strong>Name</strong> для получения дополнительных сведений см на допустимый имена <strong>свойств</strong> .</span><span class="sxs-lookup"><span data-stu-id="62a2a-118">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a2a-119">Тип</span><span class="sxs-lookup"><span data-stu-id="62a2a-119">Type</span></span></p></td>
<td><p><span data-ttu-id="62a2a-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="62a2a-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="62a2a-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="62a2a-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="62a2a-122">Константа, которая определяет тип данных нового <strong>Свойства</strong> объекта.</span><span class="sxs-lookup"><span data-stu-id="62a2a-122">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="62a2a-123">В разделе свойства <strong><a href="field-type-property-dao.md">Type</a></strong> для типов данных.</span><span class="sxs-lookup"><span data-stu-id="62a2a-123">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62a2a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="62a2a-124">Value</span></span></p></td>
<td><p><span data-ttu-id="62a2a-125">Необязательный</span><span class="sxs-lookup"><span data-stu-id="62a2a-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="62a2a-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="62a2a-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="62a2a-127"><strong>Variant</strong> содержащий исходное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="62a2a-127">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="62a2a-128">Свойство <strong><a href="field-value-property-dao.md">Value</a></strong> для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="62a2a-128">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62a2a-129">DDL</span><span class="sxs-lookup"><span data-stu-id="62a2a-129">DDL</span></span></p></td>
<td><p><span data-ttu-id="62a2a-130">Необязательный</span><span class="sxs-lookup"><span data-stu-id="62a2a-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="62a2a-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="62a2a-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="62a2a-132"><strong>Variant</strong> (<strong>логическое</strong> подтип), которое указывает, является ли <strong>свойство</strong> объектом DDL.</span><span class="sxs-lookup"><span data-stu-id="62a2a-132">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="62a2a-133">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="62a2a-133">The default is False.</span></span> <span data-ttu-id="62a2a-134">Если DDL имеет значение True, пользователи не могут изменить и удалить этот объект <strong>Свойства</strong> , если у них есть разрешение dbSecWriteDef.</span><span class="sxs-lookup"><span data-stu-id="62a2a-134">If DDL is True, users can't change or delete this <strong>Property</strong> object unless they have dbSecWriteDef permission.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="62a2a-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62a2a-135">Return Value</span></span>

<span data-ttu-id="62a2a-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="62a2a-136">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="62a2a-137">Замечания</span><span class="sxs-lookup"><span data-stu-id="62a2a-137">Remarks</span></span>

<span data-ttu-id="62a2a-138">Объект пользовательских **свойств** можно создать только в коллекции **[свойств](properties-collection-dao.md)** объекта, который является постоянным.</span><span class="sxs-lookup"><span data-stu-id="62a2a-138">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="62a2a-139">Если при использовании **CreateProperty**опустить одно или несколько частей необязательно, можно использовать соответствующие присваивания установить или сбросить соответствующего свойства перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="62a2a-139">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="62a2a-140">После добавления объекта, можно изменить некоторые, но не для всех параметров его свойств.</span><span class="sxs-lookup"><span data-stu-id="62a2a-140">After you append the object, you can alter some but not all of its property settings.</span></span> <span data-ttu-id="62a2a-141">Обратитесь к соответствующим разделам **имя**, **Тип**и **значение** свойства для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="62a2a-141">See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="62a2a-142">Если имя ссылается на объект, который уже входит в коллекции, то во время выполнения возникает ошибка при использовании метода **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="62a2a-142">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="62a2a-143">Чтобы удалить объект пользовательских **свойств** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** на **Properties** collection.</span><span class="sxs-lookup"><span data-stu-id="62a2a-143">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection.</span></span> <span data-ttu-id="62a2a-144">Не удается удалить встроенные свойства.</span><span class="sxs-lookup"><span data-stu-id="62a2a-144">You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="62a2a-145">Если опустить аргумент DDL по умолчанию используется значение False (не являющиеся DDL).</span><span class="sxs-lookup"><span data-stu-id="62a2a-145">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="62a2a-146">Так как не соответствующее свойство DDL предоставляется, необходимо удалить и повторно создать объект **свойств** , чтобы перейти с DDL не DDL.</span><span class="sxs-lookup"><span data-stu-id="62a2a-146">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


## <a name="example"></a><span data-ttu-id="62a2a-147">Пример</span><span class="sxs-lookup"><span data-stu-id="62a2a-147">Example</span></span>

<span data-ttu-id="62a2a-148">В этом примере предпринимается попытка задать значение свойства пользовательских.</span><span class="sxs-lookup"><span data-stu-id="62a2a-148">This example tries to set the value of a user-defined property.</span></span> <span data-ttu-id="62a2a-149">Если свойство не существует, метод **CreateProperty** используется для создания и установите значение нового свойства.</span><span class="sxs-lookup"><span data-stu-id="62a2a-149">If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property.</span></span> <span data-ttu-id="62a2a-150">Процедура SetProperty является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="62a2a-150">The SetProperty procedure is required for this procedure to run.</span></span>

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
