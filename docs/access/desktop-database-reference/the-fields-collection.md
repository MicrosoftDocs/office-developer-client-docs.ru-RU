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

Коллекция **Fields** — это одна из внутренних коллекций ADO. Коллекция — это упорядоченный набор элементов, который можно называть единицей.

Коллекция **Fields** содержит объект **Field** для каждого поля (столбца) в **наборе записей.** Как и все коллекции ADO, он имеет свойства **Count** и **Item,** а также методы **Append** и **Refresh.** Он также имеет **методы CancelUpdate,** **Delete,** **Resync** и **Update,** которые недоступны другим коллекциям ADO.

## <a name="examining-the-fields-collection"></a>Изучение коллекции fields

Рассмотрим **коллекцию Fields** образца **recordset,** представленного в этой главе. Пример **recordset был** получен из SQL

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

Таким образом, вы должны обнаружить, что коллекция **полей наборов**  записей содержит три поля.

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

Этот код просто определяет количество объектов **Field** в коллекции **Fields** с помощью свойства **Count** и циклы по коллекции, возвращая значение свойства **Name** для каждого **объекта Field.** Для получения сведений о поле можно использовать гораздо больше свойств Поля.  Дополнительные сведения о запросе **поля** см. в [поле "Объект поля".](the-field-object.md)

## <a name="counting-columns"></a>Подсчет столбцов

Как можно ожидать, свойство **Count** возвращает фактическое число объектов **Field** в коллекции **Fields.** Так как нуминг для членов коллекции начинается с нуля, всегда следует кодировать циклы, начиная с нулевого члена и заканчивая значением свойства **Count** минус 1. Если вы используете Microsoft Visual Basic и хотите перенабывать члены коллекции, не проверяя свойство **Count,** используйте свойство **For** **Each... Следующая** команда.

Если свойство **Count** имеет нулевое значение, в коллекции нет объектов.

## <a name="getting-to-the-field"></a>Начало работы с полем

Как и любая коллекция ADO, **свойство Item** является свойством коллекции по умолчанию. Он возвращает отдельный **объект Field,** указанный именем или индексом, переданным ему. Таким образом, следующие утверждения эквивалентны примеру **recordset:**

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

Если эти методы эквивалентны, что лучше? У всех по-разному. Использование индекса для извлечения **поля** из коллекции выполняется быстрее, так как оно напрямую выполняет доступ к полю без выполнения строки подыска.  С другой стороны, порядок полей в коллекции должен быть известен, и  если порядок изменяется, ссылку на индекс поля необходимо изменить везде, где это происходит.  Хотя это немного медленнее,  использование имени поля является более гибким, так как оно не зависит от порядка **полей** в коллекции.

## <a name="using-the-refresh-method"></a>Использование метода Refresh

В отличие от некоторых других коллекций ADO, использование метода **Refresh** для коллекции **Fields** не оказывает видимого эффекта. Чтобы получить изменения из структуры баз данных, необходимо использовать либо метод **Requery,** либо если объект **Recordset** не поддерживает закладки, метод **MoveFirst,** который приведет к повторному выполнению команды для поставщика.

## <a name="adding-fields-to-a-recordset"></a>Добавление полей в набор записей

Метод **Append** используется для добавления полей в **набор записей.**

С помощью метода **Append** можно программным способом сфакторировать **набор записей,** не открывая подключение к источнику данных. Ошибка во время работы возникает, если метод **Append** вызван в  коллекции **Fields** открытого набора записей или в наборе **записей,** где задано свойство **ActiveConnection.** Поля можно примедить только к набору **записей,** который еще не открыт и еще не подключен к источнику данных. Однако чтобы указать значения для новых добавленных  полей, сначала необходимо открыть набор записей.

Разработчикам часто требуется место для временного хранения определенных данных или требуется, чтобы некоторые данные велись так, как если бы они поступили с сервера, чтобы они могли участвовать в привязке данных в пользовательском интерфейсе. ADO (в сочетании со службой курсора Майкрософт для [OLE DB)](microsoft-cursor-service-for-ole-db-ado-service-component.md)позволяет разработчику создать пустой объект **Recordset,** указав сведения о столбце и вызывая **Open.** В следующем примере к новому объекту **Recordset** будут приданы три новых поля. Затем открывается **набор записей,** добавляются две новые записи, и **набор записей** сохраняется в файле. (Дополнительные сведения о **сохраняемости наборов** записей см. в главе [5" "Обновление и сохранение данных".](chapter-5-updating-and-persisting-data.md)

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

Использование метода **Fields** **Append** отличается в разных **объектах Recordset** и **Record.** Дополнительные сведения об объекте **Record** см. в главе [10 "Записи и потоки".](chapter-10-records-and-streams.md)

