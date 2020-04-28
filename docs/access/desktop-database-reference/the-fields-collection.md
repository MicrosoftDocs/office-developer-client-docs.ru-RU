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

Коллекция **Fields** является одной из встроенных коллекций ADO. Коллекция — это упорядоченный набор элементов, на которые можно ссылаться как на единое целое.

Коллекция **Fields** содержит объект **field** для каждого поля (столбца) в **наборе записей**. Как и в случае со всеми коллекциями ADO, у него есть свойства **Count** и **Item** , а также методы **append** и **Refresh** . Кроме того, у него есть методы **CancelUpdate**, **Delete**, **Resync**и **Update** , недоступные другим коллекциям ADO.

## <a name="examining-the-fields-collection"></a>Анализ коллекции Fields

Рассмотрим коллекцию **Fields** примера **Recordset** , представленную в этой главе. Пример **набора записей** получен из оператора SQL

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

Таким образом, коллекция **Fields** **набора записей** содержит три поля.

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

Этот код просто определяет количество объектов **field** в коллекции **Fields** с помощью свойства **Count** и выполняет циклы по коллекции, возвращая значение свойства **Name** для каждого объекта **field** . Вы можете использовать множество дополнительных свойств **полей** для получения сведений о поле. Более подробную информацию о запросе **поля**можно узнать [в объекте Field](the-field-object.md).

## <a name="counting-columns"></a>Подсчет столбцов

Как можно ожидать, свойство **Count** возвращает фактическое число объектов **field** в коллекции **Fields** . Так как нумерация элементов коллекции начинается с нуля, всегда следует всегда кодировать циклы, начиная с нулевого элемента и заканчивая значением свойства **Count** минус 1. Если вы используете Microsoft Visual Basic и хотите перебрать элементы коллекции, не проверяя свойство **Count** , используйте оператор **for** **Each... Следующая** команда.

Если свойство **Count** равно нулю, в коллекции отсутствуют объекты.

## <a name="getting-to-the-field"></a>Обращение к полю

Как и в случае с любой коллекцией ADO, свойство **Item** является свойством по умолчанию для коллекции. Он возвращает отдельный объект **field** , заданный именем или индексом, переданным ему. Таким образом, следующие операторы эквивалентны для примера **Recordset**:

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

Если эти методы являются эквивалентными, что лучше? У всех по-разному. Использование индекса для извлечения **поля** из коллекции выполняется быстрее, так как он получает доступ к **полю** напрямую без необходимости выполнять поиск строки. С другой стороны, порядок **полей** в коллекции должен быть известен, и если порядок изменяется, то ссылка на индекс **поля** будет изменяться везде, где это происходит. Хотя несколько медленнее, использование имени **поля** является более гибким, так как оно не зависит от порядка **полей** в коллекции.

## <a name="using-the-refresh-method"></a>Использование метода Refresh

В отличие от других коллекций ADO, использование метода **Refresh** в коллекции **Fields** не оказывает никакого действия. Чтобы получить изменения из базовой структуры базы данных, необходимо использовать метод **Requery** или, если объект **Recordset** не поддерживает закладки, метод **MoveFirst** , который будет приводить к повторному выполнению команды для поставщика.

## <a name="adding-fields-to-a-recordset"></a>Добавление полей в набор записей

Метод **append** используется для добавления полей в **набор записей**.

Метод **append** можно использовать для программного собственного **набора записей** без открытия подключения к источнику данных. При вызове метода **append** для коллекции **Fields** открытого **набора записей** или для объекта **Recordset** , где было задано свойство **ActiveConnection** , возникает ошибка времени выполнения. Вы можете добавлять поля только к **набору записей** , который не открыт и еще не подключен к источнику данных. Тем не менее, чтобы указать значения для вновь добавленных **полей**, сначала необходимо открыть **набор записей** .

Разработчикам часто требуется место для временного хранения некоторых данных или необходимо, чтобы некоторые данные действовали так, как если бы они поступили с сервера, чтобы он мог участвовать в привязке данных в пользовательском интерфейсе. ADO (в сочетании со [службой Microsoft Cursor Cursor for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) позволяет разработчику создать пустой объект **Recordset** , указав сведения о столбцах и вызове **Open**. В следующем примере три новых поля добавляются к новому объекту **Recordset** . Затем открывается **набор записей** , добавляются две новые записи, а **набор записей** сохраняется в файл. (Дополнительные сведения о сохранении **наборов записей** содержатся в [главе 5: обновление и сохранение данных](chapter-5-updating-and-persisting-data.md).)

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

Использование метода **append** в **полях** зависит от объекта **Recordset** и объекта **Record** . Дополнительные сведения об объекте **Record** содержатся в [главе 10: записи и потоки](chapter-10-records-and-streams.md).

