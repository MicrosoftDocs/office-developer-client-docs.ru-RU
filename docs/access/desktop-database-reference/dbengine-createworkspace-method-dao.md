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
# <a name="dbenginecreateworkspace-method-dao"></a>Метод DBEngine.CreateWorkspace (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый **[объект Workspace.](workspace-object-dao.md)**

## <a name="syntax"></a>Синтаксис

*выражения* . CreateWorkspace ***(Имя,*** ***Имя пользователя,*** ***Пароль***, ***UseType***)

*expression*: переменная, представляющая объект **DBEngine**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>Строка,</strong> которая однозначно называет новый <strong>объект Workspace.</strong> Сведения о <strong><a href="connection-name-property-dao.md">действительных</a></strong> именах рабочей области см. в свойстве <strong>Name.</strong></p></td>
</tr>
<tr class="even">
<td><p><em>UserName</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>Строка,</strong> определяемая владельцем нового объекта <strong>Workspace.</strong> Дополнительные сведения см. в свойстве <strong>UserName.</strong></p></td>
</tr>
<tr class="odd">
<td><p><em>Password</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>Строка,</strong> содержащая пароль для нового <strong>объекта Workspace.</strong> Пароль может быть длиной до 20 символов и может включать любые символы, кроме символа ASCII 0 (null).</p>
<p><strong>ПРИМЕЧАНИЕ.</strong>Используйте надежные пароли, сочетая в себе буквы, цифры и символы верхнего и нижнего регистров. В ненадежных паролях не используются сочетания таких элементов. Надежный пароль: Y6dh!et5. Слабый пароль: House27. Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.</p>
</td>
</tr>
<tr class="even">
<td><p><em>UseType</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></p>
<p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Workspace

## <a name="remarks"></a>Примечания

После использования метода **CreateWorkspace** для создания нового объекта  **Рабочей** области начинается сеанс Рабочей области, и вы можете обратиться к объекту **Workspace** в приложении.

**Объекты рабочей** области не являются постоянными, и их нельзя сохранить на диске. Создав объект **Workspace,** вы не сможете изменить его параметры свойств, за исключением свойства **Name,** которое можно изменить перед тем, как примять объект Workspace к коллекции **[Workspaces.](workspaces-collection-dao.md)** 

Вам не нужно привяжать новый **объект Workspace** к коллекции, прежде чем использовать его. Только что созданный **объект Workspace** можно примедить только в том случае, если вам потребуется ссылаться на него через коллекцию **Workspaces.**

Чтобы удалить **объект Workspace** из коллекции **Workspaces,** закрой все открытые базы данных и подключения, а затем используйте метод **[Close](connection-close-method-dao.md)** на **объекте Workspace.**

## <a name="example"></a>Пример

В этом примере используется **метод CreateWorkspace** для создания рабочего пространстваMicrosoft Access. Затем в нем перечислены свойства рабочего пространства.

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

