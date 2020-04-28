---
title: Метод DBEngine. CreateWorkspace (DAO)
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
# <a name="dbenginecreateworkspace-method-dao"></a>Метод DBEngine. CreateWorkspace (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект **[Workspace](workspace-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*Expression* . CreateWorkspace (***имя***, ***имя пользователя***, ***пароль***, ***усетипе***)

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
<td><p><strong>Строка</strong> , которая уникальным образом присваивает новый объект <strong>Workspace</strong> . Сведения о допустимых именах <strong>рабочих областей</strong> приведены в свойстве <strong><a href="connection-name-property-dao.md">Name</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><em>UserName</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>Строка</strong> , определяющая владельца нового объекта <strong>Workspace</strong> . Для получения дополнительных сведений ознакомьтесь со статьей свойство <strong>username</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><em>Password</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>Строка</strong> , содержащая пароль для нового объекта <strong>Workspace</strong> . Пароль может содержать до 20 символов и может содержать любые символы, кроме символов ASCII (null).</p>
<p><strong>Note</strong>: Используйте надежные пароли, объединяющие прописные и строчные буквы, цифры и символы. В ненадежных паролях не используются сочетания таких элементов. Надежный пароль: Y6dh!et5. Слабый пароль: House27. Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.</p>
</td>
</tr>
<tr class="even">
<td><p><em>усетипе</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Одно из значений <strong><a href="workspacetypeenum-enumeration-dao.md">воркспацетипинум</a></strong> .</p>
<p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Workspace

## <a name="remarks"></a>Примечания

Когда вы используете метод **CreateWorkspace** , чтобы создать новый объект **Workspace** , запускается сеанс **рабочей области** , и вы можете ссылаться на объект **Workspace** в своем приложении.

Объекты **рабочей области** не являются постоянными и не могут быть сохранены на диске. После создания объекта **Workspace** невозможно изменить какие-либо параметры его свойств, кроме свойства **Name** , которое можно изменить перед добавлением объекта **Workspace** в коллекцию **[workspaces](workspaces-collection-dao.md)** .

Не нужно добавлять новый объект **Workspace** в коллекцию, прежде чем его можно будет использовать. Только что созданный объект **Workspace** добавляется только в том случае, если необходимо сослаться на него через коллекцию **workspaces** .

Чтобы удалить объект **Workspace** из коллекции **workspaces** , закройте все открытые базы данных и подключения, а затем используйте метод **[Close](connection-close-method-dao.md)** для объекта **Workspace** .

## <a name="example"></a>Пример

В этом примере используется метод **CreateWorkspace** для рабочей области Креатемикрософт доступа к данным. Затем выводится список свойств рабочей области.

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

