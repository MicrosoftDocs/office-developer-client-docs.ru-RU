---
title: Метод Database. CreateProperty (DAO)
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
# <a name="databasecreateproperty-method-dao"></a><span data-ttu-id="4a97a-102">Метод Database. CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="4a97a-102">Database.CreateProperty method (DAO)</span></span>

<span data-ttu-id="4a97a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a97a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a97a-104">Создает новый объект определяемого пользователем **[Свойства](property-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4a97a-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="4a97a-105">.</span><span class="sxs-lookup"><span data-stu-id="4a97a-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a97a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a97a-106">Syntax</span></span>

<span data-ttu-id="4a97a-107">*Expression* . CreateProperty (***имя***, ***Тип***, ***значение***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="4a97a-107">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="4a97a-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="4a97a-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a97a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a97a-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4a97a-110">Имя</span><span class="sxs-lookup"><span data-stu-id="4a97a-110">Name</span></span></p></th>
<th><p><span data-ttu-id="4a97a-111">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="4a97a-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="4a97a-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4a97a-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="4a97a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4a97a-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a97a-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="4a97a-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="4a97a-115">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="4a97a-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="4a97a-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4a97a-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4a97a-117"><strong>Строка</strong> , которая уникально названа нового объекта <strong>Property</strong> .</span><span class="sxs-lookup"><span data-stu-id="4a97a-117">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="4a97a-118">Сведения о допустимых именах <strong>свойств</strong> приведены в свойстве <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="4a97a-118">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a97a-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="4a97a-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="4a97a-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4a97a-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="4a97a-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4a97a-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4a97a-122">Константа, определяющая тип данных нового объекта <strong>Property</strong> .</span><span class="sxs-lookup"><span data-stu-id="4a97a-122">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="4a97a-123">Допустимые типы данных см. в свойстве <strong><a href="field-type-property-dao.md">Type</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="4a97a-123">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a97a-124"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="4a97a-124"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="4a97a-125">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4a97a-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="4a97a-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4a97a-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4a97a-127"><strong>Переменная Variant</strong> , содержащая начальное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="4a97a-127">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="4a97a-128">Для получения подробных сведений просмотрите свойство <strong><a href="field-value-property-dao.md">value</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="4a97a-128">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a97a-129"><em>DLL</em></span><span class="sxs-lookup"><span data-stu-id="4a97a-129"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="4a97a-130">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4a97a-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="4a97a-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4a97a-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4a97a-132"><strong>Variant</strong> (<strong>логический</strong> подтип), указывающий, является ли <strong>свойство</strong> объектом DDL.</span><span class="sxs-lookup"><span data-stu-id="4a97a-132">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="4a97a-133">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="4a97a-133">The default is False.</span></span> <span data-ttu-id="4a97a-134">Если DDL имеет значение true, пользователи не могут изменить или удалить этот объект <strong>Property</strong> , если у них нет разрешения дбсеквритедеф.</span><span class="sxs-lookup"><span data-stu-id="4a97a-134">If DDL is True, users can't change or delete this <strong>Property</strong> object unless they have dbSecWriteDef permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="4a97a-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a97a-135">Return value</span></span>

<span data-ttu-id="4a97a-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="4a97a-136">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="4a97a-137">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a97a-137">Remarks</span></span>

<span data-ttu-id="4a97a-138">Пользовательский объект **Свойства** можно создать только в коллекции **[свойств](properties-collection-dao.md)** сохраняемого объекта.</span><span class="sxs-lookup"><span data-stu-id="4a97a-138">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="4a97a-139">Если опустить одну или несколько дополнительных частей при использовании **CreateProperty**, можно использовать соответствующий оператор присвоения для установки или сброса соответствующего свойства перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="4a97a-139">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="4a97a-140">После добавления объекта можно изменить не все параметры его свойств.</span><span class="sxs-lookup"><span data-stu-id="4a97a-140">After you append the object, you can alter some but not all of its property settings.</span></span> <span data-ttu-id="4a97a-141">Для получения дополнительных сведений ознакомьтесь с разделами свойства " **имя**", " **Тип**" и " **значение** ".</span><span class="sxs-lookup"><span data-stu-id="4a97a-141">See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="4a97a-142">Если имя ссылается на объект, который уже является членом коллекции, при использовании метода **[append](fields-append-method-dao.md)** возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="4a97a-142">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="4a97a-143">Чтобы удалить объект определяемого пользователем **Свойства** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции **свойств** .</span><span class="sxs-lookup"><span data-stu-id="4a97a-143">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection.</span></span> <span data-ttu-id="4a97a-144">Невозможно удалить встроенные свойства.</span><span class="sxs-lookup"><span data-stu-id="4a97a-144">You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="4a97a-145">Если опустить аргумент DDL, по умолчанию используется значение false (не для DDL).</span><span class="sxs-lookup"><span data-stu-id="4a97a-145">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="4a97a-146">Так как соответствующее свойство DDL не предоставлено, необходимо удалить и повторно создать объект **Свойства** , который нужно изменить с DDL на non-DDL.</span><span class="sxs-lookup"><span data-stu-id="4a97a-146">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


## <a name="example"></a><span data-ttu-id="4a97a-147">Пример</span><span class="sxs-lookup"><span data-stu-id="4a97a-147">Example</span></span>

<span data-ttu-id="4a97a-148">В этом примере предпринимается попытка задать значение определяемого пользователем свойства.</span><span class="sxs-lookup"><span data-stu-id="4a97a-148">This example tries to set the value of a user-defined property.</span></span> <span data-ttu-id="4a97a-149">Если свойство не существует, оно использует метод **CreateProperty** , чтобы создать и задать значение нового свойства.</span><span class="sxs-lookup"><span data-stu-id="4a97a-149">If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property.</span></span> <span data-ttu-id="4a97a-150">Для выполнения этой процедуры требуется процедура SetProperty.</span><span class="sxs-lookup"><span data-stu-id="4a97a-150">The SetProperty procedure is required for this procedure to run.</span></span>

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
