---
<<<<<<< Название HEAD: TOCTitle тип свойства (ADO): тип свойства (ADO) === название: введите свойство (ADO) TOCTitle: введите свойство (ADO)
>>>>>>> главные ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID: 48543397 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="type-property-ado"></a>Type Property (ADO)
=======
# <a name="type-property-ado"></a>Свойство Type (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает тип действующие или тип данных [параметра](parameter-object-ado.md), [поля](field-object-ado.md)или [Свойства](property-object-ado.md) объекта.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Задает или возвращает значение [DataTypeEnum](datatypeenum.md) .

## <a name="remarks"></a>Замечания

Для **параметра** объектов свойство **Type** — чтение и запись. Для нового **поля** объектов, к коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md) **Тип** — чтение и запись только после того, как указано [значение](value-property-ado.md) свойства для **поля** и поставщик данных имеет успешно добавлено новое **поле** , вызвав метод [Update](update-method-ado.md) коллекции **полей** .

Для всех других объектов свойство **Type** — только для чтения.

