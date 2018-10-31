---
title: DBEngine.CreateWorkspace Method (DAO)
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
ms.openlocfilehash: f76cb57345b7ec653092517d72fa3355a29de6cd
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862564"
---
# <a name="dbenginecreateworkspace-method-dao"></a>DBEngine.CreateWorkspace Method (DAO)


**Применимо к**: Access 2013 | Office 2013


Создает новый объект **[рабочей области](workspace-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . CreateWorkspace (***имя***, ***имя пользователя***, ***пароль***, ***UseType***)

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Имя</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p><strong>Строка</strong> , уникальным образом новый объект <strong>рабочей области</strong> . Свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения дополнительных сведений см допустимые имена <strong>рабочей области</strong> .</p></td>
</tr>
<tr class="even">
<td><p>Имя пользователя</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p><strong>Строка</strong> , идентифицирующая владелец новый объект <strong>рабочей области</strong> . Свойству <strong>имя пользователя</strong> для получения дополнительных сведений см.</p></td>
</tr>
<tr class="odd">
<td><p>Пароль</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p><strong>Строка</strong> , содержащая пароль для нового объекта <strong>рабочей области</strong> . Пароль может иметь длину до 20 символов и может содержать все символы, за исключением символа ASCII 0 (null).</p>

> [!NOTE]
> Используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы. Ненадежные пароли не смешивайте этих элементов. Надежный пароль: Y6dh! et5. Ненадежный пароль: House27. Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.


</td>
</tr>
<tr class="even">
<td><p>UseType</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Одно из значений <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</p>

> [!NOTE]
> Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Установка для аргумента типа **dbUseODBC** приведет к ошибке времени выполнения. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.


</td>
</tr>
</tbody>
</table>


<<<<<<< HEAD
### <a name="return-value"></a>Возвращаемое значение
=======
### <a name="return-value"></a>Возвращаемое значение
>>>>>>> образец

Рабочая область

## <a name="remarks"></a>Замечания

После использовать метод **CreateWorkspace** для создания нового объекта **рабочей области** , запуске сеанса **рабочей области** и может ссылаться на объект **рабочей области** в приложении.

**Рабочая область для** объектов, не сохраняются и не могут сохранять их на диск. После создания **рабочей области для** объекта невозможно изменить любые параметры его свойства, за исключением **имени** свойства, которое можно изменить перед добавлением объекта **рабочей области** для семейства сайтов **[рабочих областей](workspaces-collection-dao.md)** .

Добавьте новый объект **рабочей области** в семейство сайтов, прежде чем использовать его не нужно. Можно добавить только что созданный объект **рабочей области** только в том случае, если необходимо сослаться на него через коллекцию **рабочих областей** .

Чтобы удалить объект **рабочей области** из коллекции **рабочих областей** , закройте все открытые баз данных и подключения к и затем использовать метод **[Close](connection-close-method-dao.md)** объекта **рабочей области** .

## <a name="example"></a>Пример

В этом примере используется метод **CreateWorkspace** в рабочей области для доступа к createMicrosoft. Затем список свойств рабочей области.

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

