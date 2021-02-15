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
localization_priority: Normal
ms.openlocfilehash: 9cd84b6b5441edda2042ce0a63ae25b2cf399bd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294352"
---
# <a name="dbenginecreateworkspace-method-dao"></a><span data-ttu-id="f568b-102">Метод DBEngine.CreateWorkspace (DAO)</span><span class="sxs-lookup"><span data-stu-id="f568b-102">DBEngine.CreateWorkspace method (DAO)</span></span>

<span data-ttu-id="f568b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f568b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f568b-104">Создает новый объект **[Workspace.](workspace-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="f568b-104">Creates a new **[Workspace](workspace-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f568b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f568b-105">Syntax</span></span>

<span data-ttu-id="f568b-106">*выражение .* CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span><span class="sxs-lookup"><span data-stu-id="f568b-106">*expression* .CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span></span>

<span data-ttu-id="f568b-107">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="f568b-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f568b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f568b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f568b-109">Имя</span><span class="sxs-lookup"><span data-stu-id="f568b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f568b-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="f568b-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f568b-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f568b-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="f568b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f568b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f568b-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="f568b-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="f568b-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f568b-114">Required</span></span></p></td>
<td><p><span data-ttu-id="f568b-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="f568b-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f568b-116"><strong>Строка,</strong> однозначно именовав новый <strong>объект Workspace.</strong></span><span class="sxs-lookup"><span data-stu-id="f568b-116">A <strong>String</strong> that uniquely names the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="f568b-117">Сведения о <strong><a href="connection-name-property-dao.md">допустимом</a></strong> имени рабочей области см. в <strong>свойстве Name.</strong></span><span class="sxs-lookup"><span data-stu-id="f568b-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Workspace</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f568b-118"><em>UserName</em></span><span class="sxs-lookup"><span data-stu-id="f568b-118"><em>UserName</em></span></span></p></td>
<td><p><span data-ttu-id="f568b-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="f568b-119">Required</span></span></p></td>
<td><p><span data-ttu-id="f568b-120"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="f568b-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f568b-121"><strong>Строка,</strong> идентифицирует владельца нового объекта <strong>Workspace.</strong></span><span class="sxs-lookup"><span data-stu-id="f568b-121">A <strong>String</strong> that identifies the owner of the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="f568b-122">Дополнительные сведения см. в свойстве <strong>UserName.</strong></span><span class="sxs-lookup"><span data-stu-id="f568b-122">See the <strong>UserName</strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f568b-123"><em>Password</em></span><span class="sxs-lookup"><span data-stu-id="f568b-123"><em>Password</em></span></span></p></td>
<td><p><span data-ttu-id="f568b-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="f568b-124">Required</span></span></p></td>
<td><p><span data-ttu-id="f568b-125"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="f568b-125"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f568b-126"><strong>Строка,</strong> содержащая пароль для нового <strong>объекта Workspace.</strong></span><span class="sxs-lookup"><span data-stu-id="f568b-126">A <strong>String</strong> containing the password for the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="f568b-127">Пароль может иметь длину до 20 символов и включать любые символы, кроме символа ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f568b-127">The password can be up to 20 characters long and can include any characters except ASCII character 0 (null).</span></span></p>
<p><span data-ttu-id="f568b-128"><strong>ПРИМЕЧАНИЕ.</strong>Используйте надежные пароли, сочетая в себе буквы верхнего и нижнего регистра, цифры и символы.</span><span class="sxs-lookup"><span data-stu-id="f568b-128"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="f568b-129">В ненадежных паролях не используются сочетания таких элементов.</span><span class="sxs-lookup"><span data-stu-id="f568b-129">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="f568b-130">Надежный пароль: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="f568b-130">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="f568b-131">Слабый пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="f568b-131">Weak password: House27.</span></span> <span data-ttu-id="f568b-132">Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.</span><span class="sxs-lookup"><span data-stu-id="f568b-132">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f568b-133"><em>UseType</em></span><span class="sxs-lookup"><span data-stu-id="f568b-133"><em>UseType</em></span></span></p></td>
<td><p><span data-ttu-id="f568b-134">Необязательный</span><span class="sxs-lookup"><span data-stu-id="f568b-134">Optional</span></span></p></td>
<td><p><span data-ttu-id="f568b-135"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f568b-135"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f568b-136">Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></span><span class="sxs-lookup"><span data-stu-id="f568b-136">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<p><span data-ttu-id="f568b-137"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="f568b-137"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="f568b-138">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f568b-138">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="f568b-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f568b-139">Return value</span></span>

<span data-ttu-id="f568b-140">Рабочая группа</span><span class="sxs-lookup"><span data-stu-id="f568b-140">Workspace</span></span>

## <a name="remarks"></a><span data-ttu-id="f568b-141">Заметки</span><span class="sxs-lookup"><span data-stu-id="f568b-141">Remarks</span></span>

<span data-ttu-id="f568b-142">После использования метода **CreateWorkspace** для создания нового объекта **Рабочей** области начинается сеанс **Рабочей** области, и вы можете сослаться на объект **Workspace** в приложении.</span><span class="sxs-lookup"><span data-stu-id="f568b-142">Once you use the **CreateWorkspace** method to create a new **Workspace** object, a **Workspace** session is started, and you can refer to the **Workspace** object in your application.</span></span>

<span data-ttu-id="f568b-143">**Объекты** рабочей области не являются постоянными, и их нельзя сохранить на диск.</span><span class="sxs-lookup"><span data-stu-id="f568b-143">**Workspace** objects aren't permanent, and you can't save them to disk.</span></span> <span data-ttu-id="f568b-144">После создания объекта **Workspace** нельзя изменить какие-либо параметры его свойства, за исключением свойства **Name,** которое можно изменить перед тем, как применить объект **Workspace** к коллекции **[Workspaces.](workspaces-collection-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="f568b-144">Once you create a **Workspace** object, you can't alter any of its property settings, except for the **Name** property, which you can modify before appending the **Workspace** object to the **[Workspaces](workspaces-collection-dao.md)** collection.</span></span>

<span data-ttu-id="f568b-145">Для использования нового объекта **Workspace** в коллекцию не нужно.</span><span class="sxs-lookup"><span data-stu-id="f568b-145">You don't have to append the new **Workspace** object to a collection before you can use it.</span></span> <span data-ttu-id="f568b-146">Только что созданный **объект Workspace** следует при необходимости сослаться на него через коллекцию **Workspaces.**</span><span class="sxs-lookup"><span data-stu-id="f568b-146">You append a newly created **Workspace** object only if you need to refer to it through the **Workspaces** collection.</span></span>

<span data-ttu-id="f568b-147">Чтобы удалить **объект Workspace** из коллекции **Workspaces,** закроете все открытые базы данных и подключения, а затем используйте метод **[Close](connection-close-method-dao.md)** для объекта **Workspace.**</span><span class="sxs-lookup"><span data-stu-id="f568b-147">To remove a **Workspace** object from the **Workspaces** collection, close all open databases and connections and then use the **[Close](connection-close-method-dao.md)** method on the **Workspace** object.</span></span>

## <a name="example"></a><span data-ttu-id="f568b-148">Пример</span><span class="sxs-lookup"><span data-stu-id="f568b-148">Example</span></span>

<span data-ttu-id="f568b-149">В этом примере используется метод **CreateWorkspace** для создания рабочей областиMicrosoft Access.</span><span class="sxs-lookup"><span data-stu-id="f568b-149">This example uses the **CreateWorkspace** method to createMicrosoft Access workspace.</span></span> <span data-ttu-id="f568b-150">Затем в нем перечислены свойства рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f568b-150">It then lists the properties of the workspace.</span></span>

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

