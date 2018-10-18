---
<<<<<<< Название HEAD: TOCTitle свойство AbsolutePage (ADO): ms:assetid свойство AbsolutePage (ADO): b6e5daac-cc21-0aa6-9119-a973595762bb ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15) ms:contentKeyID: 48547288 ms.date: 09/18/2015 mtps_version: v = Office.15
---

# <a name="absolutepage-property-ado"></a>AbsolutePage Property (ADO)

=== Название: свойство AbsolutePage (ADO) TOCTitle: свойство (ADO) ms:assetid AbsolutePage: b6e5daac-cc21-0aa6-9119-a973595762bb ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15) ms:contentKeyID: 48547288 ms.date: 10/17/2018 mtps_version: v=office.15
---

# <a name="absolutepage-property-ado"></a>Свойство AbsolutePage (ADO)
>>>>>>> master

**Применимо к**: Access 2013 | Office 2013

Указывает, на какую страницу находится текущей записи.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

<a name="sets-or-returns-a-long-value-from-1-to-the-number-of-pages-in-the-recordsetrecordset-object-adomd-object--pagecountpagecount-property-adomd--or-returns-one-of-the-positionenumpositionenummd-values"></a>Задает или возвращает значение типа **Long** от 1 число страниц в объекте [набора записей](recordset-object-ado.md) ( [PageCount](pagecount-property-ado.md) ) либо одно из значений [PositionEnum](positionenum.md) .
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **Long** от 1 число страниц в объекте [набора записей](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)) либо одно из значений [PositionEnum](positionenum.md) .
>>>>>>> master

## <a name="remarks"></a>Замечания

Это свойство можно использовать для идентификации номер страницы, на котором расположена текущая запись. Он использует свойство [PageSize](pagesize-property-ado.md) логическое разделение строк общее число объекта **набора записей** в набор страниц, каждый из которых содержит число записей, равное **PageSize** (за исключением на последней странице, которая может быть меньше записей). Поставщик должен поддерживать соответствующие функциональные возможности для этого свойства, чтобы оно было доступно.

После получения и установки свойства **AbsolutePage** , ADO используется свойство [AbsolutePosition](absoluteposition-property-ado.md) и свойство [PageSize](pagesize-property-ado.md) вместе следующим образом:

<<<<<<< HEAD
  - Для получения **AbsolutePage**ADO сначала получает **AbsolutePosition**и затем делит их **PageSize**.

  - Чтобы задать **AbsolutePage**, ADO перемещает **AbsolutePosition** , как показано ниже: его умножает **PageSize** на новое значение **AbsolutePage** и затем добавляет значение 1. В результате будет текущую позицию в **наборе записей** после успешной установки **AbsolutePage** первой записи в эту страницу.
=======
- Для получения **AbsolutePage**ADO сначала получает **AbsolutePosition**и затем делит их **PageSize**.

- Чтобы задать **AbsolutePage**, ADO перемещает **AbsolutePosition** , как показано ниже: его умножает **PageSize** на новое значение **AbsolutePage** и затем добавляет значение 1. В результате текущую позицию в **наборе записей** после успешной установки **AbsolutePage** является первой записи в эту страницу.
>>>>>>> master

Как и свойство **AbsolutePosition** **AbsolutePage** на основе 1 и имеет значение 1, если текущая запись является первой записи в **набор записей**. Задайте это свойство, чтобы перейти к первой записи определенной страницы. Получите общее число страниц из свойства **PageCount** .

