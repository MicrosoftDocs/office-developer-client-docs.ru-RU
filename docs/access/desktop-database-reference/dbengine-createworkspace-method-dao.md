---
title: Метод DBEngine.CreateWorkspace (DAO)
TOCTitle: CreateWorkspace Method
ms:assetid: a7d73771-9420-0448-99e6-d6c4aa78683a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821374(v=office.15)
ms:contentKeyID: 48546888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052966
f1_categories:
- Office.Version=v15
ms.openlocfilehash: df63dfb8351da910a6f735722ef33e8ddc347150
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937815"
---
# <a name="dbenginecreateworkspace-method-dao"></a><span data-ttu-id="ee566-102">Метод DBEngine.CreateWorkspace (DAO)</span><span class="sxs-lookup"><span data-stu-id="ee566-102">DBEngine.CreateWorkspace method (DAO)</span></span>


<span data-ttu-id="ee566-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee566-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ee566-104">Создает новый объект **[рабочей области](workspace-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="ee566-104">Creates a new **[Workspace](workspace-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee566-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee566-105">Syntax</span></span>

<span data-ttu-id="ee566-106">*выражение* . CreateWorkspace (***имя***, ***имя пользователя***, ***пароль***, ***UseType***)</span><span class="sxs-lookup"><span data-stu-id="ee566-106">*expression* .CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span></span>

<span data-ttu-id="ee566-107">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="ee566-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="ee566-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee566-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee566-109">Имя</span><span class="sxs-lookup"><span data-stu-id="ee566-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ee566-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="ee566-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ee566-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ee566-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ee566-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ee566-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee566-113">Имя</span><span class="sxs-lookup"><span data-stu-id="ee566-113">Name</span></span></p></td>
<td><p><span data-ttu-id="ee566-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee566-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ee566-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="ee566-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ee566-116"><strong>Строка</strong> , уникальным образом новый объект <strong>рабочей области</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee566-116">A <strong>String</strong> that uniquely names the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="ee566-117">Свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения дополнительных сведений см допустимые имена <strong>рабочей области</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee566-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Workspace</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee566-118">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="ee566-118">UserName</span></span></p></td>
<td><p><span data-ttu-id="ee566-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee566-119">Required</span></span></p></td>
<td><p><span data-ttu-id="ee566-120"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="ee566-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ee566-121"><strong>Строка</strong> , идентифицирующая владелец новый объект <strong>рабочей области</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee566-121">A <strong>String</strong> that identifies the owner of the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="ee566-122">Свойству <strong>имя пользователя</strong> для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="ee566-122">See the <strong>UserName</strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee566-123">Пароль</span><span class="sxs-lookup"><span data-stu-id="ee566-123">Password</span></span></p></td>
<td><p><span data-ttu-id="ee566-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee566-124">Required</span></span></p></td>
<td><p><span data-ttu-id="ee566-125"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="ee566-125"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ee566-126"><strong>Строка</strong> , содержащая пароль для нового объекта <strong>рабочей области</strong> .</span><span class="sxs-lookup"><span data-stu-id="ee566-126">A <strong>String</strong> containing the password for the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="ee566-127">Пароль может иметь длину до 20 символов и может содержать все символы, за исключением символа ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ee566-127">The password can be up to 20 characters long and can include any characters except ASCII character 0 (null).</span></span></p>
<td><p><span data-ttu-id="ee566-128"><strong>Примечание</strong>: используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы.</span><span class="sxs-lookup"><span data-stu-id="ee566-128"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="ee566-129">Ненадежные пароли не смешивайте этих элементов.</span><span class="sxs-lookup"><span data-stu-id="ee566-129">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="ee566-130">Надежный пароль: Y6dh! et5.</span><span class="sxs-lookup"><span data-stu-id="ee566-130">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="ee566-131">Ненадежный пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="ee566-131">Weak password: House27.</span></span> <span data-ttu-id="ee566-132">Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.</span><span class="sxs-lookup"><span data-stu-id="ee566-132">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee566-133">UseType</span><span class="sxs-lookup"><span data-stu-id="ee566-133">UseType</span></span></p></td>
<td><p><span data-ttu-id="ee566-134">Необязательный</span><span class="sxs-lookup"><span data-stu-id="ee566-134">Optional</span></span></p></td>
<td><p><span data-ttu-id="ee566-135"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ee566-135"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ee566-136">Одно из значений <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="ee566-136">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="ee566-137"><strong>Примечание</strong>: технология ODBCDirect рабочие области, не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="ee566-137"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="ee566-138">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ee566-138">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ee566-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee566-139">Return value</span></span>

<span data-ttu-id="ee566-140">Рабочая область</span><span class="sxs-lookup"><span data-stu-id="ee566-140">Workspace</span></span>

## <a name="remarks"></a><span data-ttu-id="ee566-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee566-141">Remarks</span></span>

<span data-ttu-id="ee566-142">После использовать метод **CreateWorkspace** для создания нового объекта **рабочей области** , запуске сеанса **рабочей области** и может ссылаться на объект **рабочей области** в приложении.</span><span class="sxs-lookup"><span data-stu-id="ee566-142">Once you use the **CreateWorkspace** method to create a new **Workspace** object, a **Workspace** session is started, and you can refer to the **Workspace** object in your application.</span></span>

<span data-ttu-id="ee566-143">**Рабочая область для** объектов, не сохраняются и не могут сохранять их на диск.</span><span class="sxs-lookup"><span data-stu-id="ee566-143">**Workspace** objects aren't permanent, and you can't save them to disk.</span></span> <span data-ttu-id="ee566-144">После создания **рабочей области для** объекта невозможно изменить любые параметры его свойства, за исключением **имени** свойства, которое можно изменить перед добавлением объекта **рабочей области** для семейства сайтов **[рабочих областей](workspaces-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="ee566-144">Once you create a **Workspace** object, you can't alter any of its property settings, except for the **Name** property, which you can modify before appending the **Workspace** object to the **[Workspaces](workspaces-collection-dao.md)** collection.</span></span>

<span data-ttu-id="ee566-145">Добавьте новый объект **рабочей области** в семейство сайтов, прежде чем использовать его не нужно.</span><span class="sxs-lookup"><span data-stu-id="ee566-145">You don't have to append the new **Workspace** object to a collection before you can use it.</span></span> <span data-ttu-id="ee566-146">Можно добавить только что созданный объект **рабочей области** только в том случае, если необходимо сослаться на него через коллекцию **рабочих областей** .</span><span class="sxs-lookup"><span data-stu-id="ee566-146">You append a newly created **Workspace** object only if you need to refer to it through the **Workspaces** collection.</span></span>

<span data-ttu-id="ee566-147">Чтобы удалить объект **рабочей области** из коллекции **рабочих областей** , закройте все открытые баз данных и подключения к и затем использовать метод **[Close](connection-close-method-dao.md)** объекта **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="ee566-147">To remove a **Workspace** object from the **Workspaces** collection, close all open databases and connections and then use the **[Close](connection-close-method-dao.md)** method on the **Workspace** object.</span></span>

## <a name="example"></a><span data-ttu-id="ee566-148">Пример</span><span class="sxs-lookup"><span data-stu-id="ee566-148">Example</span></span>

<span data-ttu-id="ee566-149">В этом примере используется метод **CreateWorkspace** в рабочей области для доступа к createMicrosoft.</span><span class="sxs-lookup"><span data-stu-id="ee566-149">This example uses the **CreateWorkspace** method to createMicrosoft Access workspace.</span></span> <span data-ttu-id="ee566-150">Затем список свойств рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ee566-150">It then lists the properties of the workspace.</span></span>

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
 
```

