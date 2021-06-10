---
title: The Fields Collection
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce08ac5952151471ce74afd9a8a49600d8e8f633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314135"
---
# <a name="fields-collection"></a>Коллекция Fields


**Область применения**: Access 2013, Office 2013

Коллекция **Fields** — это одна из внутренних коллекций ADO. Коллекция — это упорядоченный набор элементов, которые можно называть единицей.

Коллекция **Fields** содержит объект **Field** для каждого поля (столбца) в **Наборе записей.** Как и все коллекции ADO, он имеет свойства **Count** и **Item,** а также методы **приложения** и **обновления.** Он также имеет **методы CancelUpdate,** **Delete,** **Resync** и **Update,** которые недоступны для других коллекций ADO.

## <a name="examining-the-fields-collection"></a>Изучение коллекции Полей

Рассмотрим **коллекцию Полей** примера **Recordset,** представленную в этой главе. Пример **Recordset был** получен из SQL.

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

Таким образом, вы должны обнаружить, что коллекция **Полей Recordset** **содержит** три поля.

```vb 
 
'BeginWalkFields 
 Dim objFields As ADODB.Fields 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText 
 
 Set objFields = objRs.Fields 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 Next 
'EndWalkFields 
```

Этот код просто определяет количество объектов **Field** в коллекции **Fields** с помощью свойства **Count** и циклов через коллекцию, возвращая значение свойства **Name** для каждого объекта **Field.** Для получения сведений **о** поле можно использовать гораздо больше свойств field. Дополнительные сведения об запросе **поля** см. в поле [Object](the-field-object.md).

## <a name="counting-columns"></a>Подсчет столбцов

Как и ожидается, свойство **Count** возвращает фактическое количество объектов **Field** в коллекции **Fields.** Так как нуминг для членов коллекции начинается с нуля, всегда следует использовать циклы кода, начиная с нулевого члена и заканчивая значением свойства **Count** минус 1. Если вы используете microsoft Visual Basic и хотите проциклить членов коллекции без проверки свойства **Count,** используйте **для каждого...** **Следующая** команда.

Если свойство **Count** нулевое, в коллекции нет объектов.

## <a name="getting-to-the-field"></a>Как добраться до поля

Как и в любой коллекции ADO, **свойство Item** является свойством коллекции по умолчанию. Он возвращает отдельный **объект Field,** указанный именем или индексом, переданным ему. Таким образом, для примера Recordset эквивалентны следующие **утверждения:**

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

Если эти методы эквивалентны, что лучше всего? У всех по-разному. Использование индекса для получения **поля** из коллекции выполняется  быстрее, так как оно напрямую выполняет просмотр поля без выполнения строки. С другой стороны, необходимо  знать порядок полей в коллекции, и если  порядок изменяется, ссылку на индекс Поля необходимо изменить везде, где это происходит. Хотя немного медленнее, использование имени **Поля** является более гибким, так как оно не зависит от порядка **полей** в коллекции.

## <a name="using-the-refresh-method"></a>Использование метода обновления

В отличие от некоторых других коллекций ADO, использование метода **Обновления** в коллекции **Fields** не оказывает видимого эффекта. Чтобы получить изменения из основной структуры базы данных, необходимо использовать метод **Requery** или если объект **Recordset** не поддерживает закладки, метод **MoveFirst,** который приведет к повторному выполнению команды в отношении поставщика.

## <a name="adding-fields-to-a-recordset"></a>Добавление полей в набор recordset

Метод **Append** используется для добавления полей в **Набор записей.**

Метод **Append** можно использовать для того, чтобы программным образом издать **набор записей,** не открывая подключения к источнику данных. Ошибка при запуске произойдет, если метод **Append** вызван в  коллекцию **Полей** открытого набора записей или в наборе записей, где задано свойство  **ActiveConnection.** Поля можно примедить только к **набору записей,** который еще не открыт и еще не подключен к источнику данных. Однако, чтобы указать значения для недавно добавленных полей, сначала необходимо открыть **Набор** записей.

Разработчикам часто требуется место для временного хранения некоторых данных или требуется, чтобы некоторые данные действовали так, как будто они поступили с сервера, чтобы они могли участвовать в привязке данных в пользовательском интерфейсе. ADO (совместно с службой [Microsoft Cursor для OLE DB)](microsoft-cursor-service-for-ole-db-ado-service-component.md)позволяет разработчику создать пустой объект **Recordset,** указав сведения о столбцах и позвонив **в Open.** В следующем примере к новому объекту **Recordset** примыкают три новых поля. Затем **открывается Набор** записей, добавляются две новые записи, и **запись** сохраняется в файле. (Дополнительные сведения о **сохраняемости Recordset** см. в главе [5: Обновление и сохранение данных.)](chapter-5-updating-and-persisting-data.md)

```vb 
 
 'BeginFabricate 
 Dim objRs As New ADODB.Recordset 
 
 With objRs.Fields 
 .Append "StudentID", adChar, 11, adFldUpdatable 
 .Append "FullName", adVarChar, 50, adFldUpdatable 
 .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable 
 End With 
 
 With objRs 
 .Open 
 
 .AddNew 
 .Fields(0) = "123-45-6789" 
 .Fields(1) = "John Doe" 
 .Fields(2) = "(425) 555-5555" 
 .Update 
 
 .AddNew 
 .Fields(0) = "123-45-6780" 
 .Fields(1) = "Jane Doe" 
 .Fields(2) = "(615) 555-1212" 
 .Update 
 End With 
 
 objRs.Save App.Path & "\FabriTest.adtg", adPersistADTG 
 
 objRs.Close 
 'EndFabricate 
```

Использование метода **приложения Fields** **отличается** между объектом **Recordset** и **объектом Record.** Дополнительные сведения об объекте **Запись** см. [в главе 10: Записи и Потоки.](chapter-10-records-and-streams.md)

